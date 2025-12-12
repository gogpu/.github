<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/gogpu/.github/main/assets/logo.png">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/gogpu/.github/main/assets/logo.png">
    <img src="https://raw.githubusercontent.com/gogpu/.github/main/assets/logo.png" alt="GoGPU Logo" width="180" />
  </picture>
</p>

<h1 align="center">GoGPU</h1>

<p align="center">
  <strong>Pure Go GPU Computing Ecosystem</strong><br>
  GPU power, Go simplicity. Zero CGO.
</p>

<p align="center">
  <a href="https://github.com/gogpu/gogpu"><img src="https://img.shields.io/badge/Go-1.25+-00ADD8?style=flat&logo=go" alt="Go Version"></a>
  <a href="https://github.com/gogpu/gogpu/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License"></a>
  <a href="https://github.com/gogpu"><img src="https://img.shields.io/github/stars/gogpu?style=social" alt="Stars"></a>
</p>

---

## Why GoGPU?

Inspired by [this discussion on r/golang](https://www.reddit.com/r/golang/comments/1pdw9i7/go_deserves_more_support_in_gui_development/), we're building the GPU computing ecosystem that Go deserves — from low-level graphics to high-level GUI, all with **zero CGO**.

---

## Projects

| Repository | Description | Status |
|:-----------|:------------|:------:|
| **[gogpu](https://github.com/gogpu/gogpu)** | Graphics framework — GPU abstraction, windowing, input | v0.3.0 |
| **[wgpu](https://github.com/gogpu/wgpu)** | Pure Go WebGPU implementation (types, core, HAL) | v0.4.0 |
| **[naga](https://github.com/gogpu/naga)** | Pure Go shader compiler — WGSL → SPIR-V | **v0.4.0** |
| **[gg](https://github.com/gogpu/gg)** | Simple 2D graphics library | **v0.1.0** |
| **[ui](https://github.com/gogpu/ui)** | GUI widget toolkit | Planned |

---

## Architecture

```
┌─────────────────────────────────────────────────────────────┐
│              Your Application                               │
├─────────────────────────────────────────────────────────────┤
│   gogpu/ui (GUI)   │   born-ml/born   │   Your Framework    │
├─────────────────────────────────────────────────────────────┤
│              gogpu/gg (2D Graphics)                         │
├─────────────────────────────────────────────────────────────┤
│              gogpu/gogpu (Graphics Framework)               │
│         GPU abstraction, windowing, input, math             │
├─────────────────────────────────────────────────────────────┤
│   go-webgpu/webgpu (FFI)    →    gogpu/wgpu (Pure Go)       │
├─────────────────────────────────────────────────────────────┤
│              Vulkan  │  Metal  │  DX12  │  OpenGL           │
└─────────────────────────────────────────────────────────────┘
```

---

## Key Features

| Feature | Description |
|:--------|:------------|
| **Zero CGO** | No C compiler required, simple `go build` |
| **WebGPU API** | Modern, portable GPU abstraction |
| **Layered Design** | Use only what you need |
| **Pure Go Goal** | Gradually replacing FFI with native Go |

---

## Quick Start

```go
package main

import "github.com/gogpu/gogpu"

func main() {
    app := gogpu.NewApp(gogpu.Config{
        Title:  "Hello GoGPU",
        Width:  800,
        Height: 600,
    })

    app.OnDraw(func(ctx *gogpu.Context) {
        ctx.Clear(gogpu.Black)
        ctx.DrawTriangle(/* ... */)
    })

    app.Run()
}
```

> **Note:** API is in active development and will change.

---

## Ecosystem

| Project | Organization | Description |
|:--------|:-------------|:------------|
| [webgpu](https://github.com/go-webgpu/webgpu) | go-webgpu | Zero-CGO WebGPU bindings |
| [goffi](https://github.com/go-webgpu/goffi) | go-webgpu | Pure Go FFI library |
| [born](https://github.com/born-ml/born) | born-ml | Pure Go ML framework |

---

## Roadmap

### Foundation ✅
- [x] Zero-CGO WebGPU bindings (go-webgpu/webgpu)
- [x] Pure Go FFI (go-webgpu/goffi)

### Phase 1 — Graphics ✅
- [x] Graphics framework (gogpu/gogpu) — Triangle, Textures, Dual Backend
- [x] Shader compiler (gogpu/naga) — **WGSL → SPIR-V + compute shaders (~17K LOC)**

### Phase 2 — Pure Go WebGPU ✅
- [x] WebGPU types package (gogpu/wgpu/types)
- [x] Core validation & state (gogpu/wgpu/core)
- [x] HAL abstraction layer (gogpu/wgpu/hal)
- [x] OpenGL ES backend (gogpu/wgpu/hal/gles) — ~7.5K LOC, Windows + Linux
- [x] **Vulkan backend (gogpu/wgpu/hal/vulkan) — ~27K LOC, cross-platform!**
- [x] **Software backend (gogpu/wgpu/hal/software) — ~1K LOC, headless rendering!**

### Phase 3 — 2D Graphics ✅
- [x] 2D graphics library (gogpu/gg) — **v0.1.0, software renderer!**
- [ ] Text rendering, image loading (v0.2.0)
- [ ] GPU acceleration (v0.4.0)

### Phase 4 — GUI
- [ ] Widget toolkit (gogpu/ui)
- [ ] Layouts, styling, themes

---

## Contributing

We welcome contributions! See individual repository CONTRIBUTING.md files.

**Areas where we need help:**
- Pure Go GPU backends (Metal, DX12)
- WebGPU examples and tutorials
- Documentation
- Software rasterization (Phase 2 of software backend)

---

## License

All projects are licensed under the **MIT License**.

---

<p align="center">
  <sub>Building the GPU computing ecosystem Go deserves</sub><br>
  <a href="https://github.com/gogpu">github.com/gogpu</a>
</p>
