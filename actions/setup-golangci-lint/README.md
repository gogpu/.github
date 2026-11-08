# setup-golangci-lint

Installs a pinned golangci-lint release for CI. Every lint job in the gogpu and go-webgpu repos uses it.

`golangci/golangci-lint-action` downloads the binary from GitHub Releases on every job, and the runner images don't
ship golangci-lint. One unavailable release asset is then enough to fail every lint job. On 2026-11-08 the
v2.15.0 linux-amd64 archive returned HTTP 504 for at least 15 minutes while other assets of the same release
downloaded fine.

This action removes that dependency:

- **Cache first.** The release archive is kept in the Actions cache, keyed by version, platform and sha256. A cache
  hit makes no network request.
- **sha256 on every run.** The archive is checked against the hash pinned here on every run, on a cache hit too, so
  a corrupted or poisoned cache entry never reaches `PATH`.
- **Provenance on download.** On a cache miss the archive is downloaded and checked with
  `gh attestation verify --repo golangci/golangci-lint`. That is the SLSA build provenance golangci-lint publishes
  for each release asset. Each of 4 attempts tries the API asset route (`gh release download`) first, then the
  `releases/download` URL. On 2026-11-08 the URL returned 504 for anonymous requests for over an hour, while the API
  route served the same file.
- Linux and macOS runners, amd64 and arm64. Lint other targets on a Linux runner with `GOOS`/`GOARCH` set.

## Usage

```yaml
- uses: gogpu/.github/actions/setup-golangci-lint@<commit sha> # main, <date>
- uses: golangci/golangci-lint-action@<commit sha> # v9.x.y
  with:
    install-mode: none
    args: --timeout=5m
```

Pin the action by commit SHA, as every action in our workflows is pinned (a tag can be moved).

## Bumping golangci-lint

One PR to this repo:

1. Change the default `version` in `action.yml`.
2. Replace the sha256 table with the new release's values. Take them from the release's `checksums.txt`, or
   `gh api repos/golangci/golangci-lint/releases/tags/<version> --jq '.assets[] | "\(.name) \(.digest)"'`.
3. The test workflow downloads and verifies each platform on a cold cache.

Then each repo moves its pin to the new commit.

## Tests

`.github/workflows/test-setup-golangci-lint.yml` runs on every change to the action:

- **cold:** a cold cache on linux amd64, linux arm64 and macOS;
- **warm:** a warm cache with the download host unreachable, which must pass;
- **poisoned:** a poisoned cache entry with the host unreachable, which must fail with nothing on `PATH`.
