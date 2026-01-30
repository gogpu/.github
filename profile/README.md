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
  <a href="https://github.com/gogpu"><img src="https://img.shields.io/badge/Pure_Go-Zero_CGO-brightgreen?style=flat" alt="Pure Go"></a>
  <a href="https://github.com/gogpu/gogpu/discussions"><img src="https://img.shields.io/github/discussions/gogpu/gogpu?style=flat&labelColor=555&color=blue" alt="Discussions"></a>
</p>

---

## Why GoGPU?

Inspired by [this discussion on r/golang](https://www.reddit.com/r/golang/comments/1pdw9i7/go_deserves_more_support_in_gui_development/), we're building the GPU computing ecosystem that Go deserves — from low-level graphics to high-level GUI, all with **zero CGO**.

---

## Ecosystem

| Library | Purpose | Version | Stars | Issues | PRs |
|:--------|:--------|:-------:|:-----:|:------:|:---:|
| **[gg](https://github.com/gogpu/gg)** | 2D graphics, Canvas API, GPU compute | [![](https://img.shields.io/github/v/release/gogpu/gg?style=flat-square&label=)](https://github.com/gogpu/gg/releases) | [![](https://img.shields.io/github/stars/gogpu/gg?style=flat-square&label=)](https://github.com/gogpu/gg) | [![](https://img.shields.io/github/issues/gogpu/gg?style=flat-square&label=)](https://github.com/gogpu/gg/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/gg?style=flat-square&label=)](https://github.com/gogpu/gg/pulls) |
| **[wgpu](https://github.com/gogpu/wgpu)** | Pure Go WebGPU (Vulkan/Metal/GLES/DX12) | [![](https://img.shields.io/github/v/release/gogpu/wgpu?style=flat-square&label=)](https://github.com/gogpu/wgpu/releases) | [![](https://img.shields.io/github/stars/gogpu/wgpu?style=flat-square&label=)](https://github.com/gogpu/wgpu) | [![](https://img.shields.io/github/issues/gogpu/wgpu?style=flat-square&label=)](https://github.com/gogpu/wgpu/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/wgpu?style=flat-square&label=)](https://github.com/gogpu/wgpu/pulls) |
| **[naga](https://github.com/gogpu/naga)** | WGSL → SPIR-V/MSL/GLSL/HLSL compiler | [![](https://img.shields.io/github/v/release/gogpu/naga?style=flat-square&label=)](https://github.com/gogpu/naga/releases) | [![](https://img.shields.io/github/stars/gogpu/naga?style=flat-square&label=)](https://github.com/gogpu/naga) | [![](https://img.shields.io/github/issues/gogpu/naga?style=flat-square&label=)](https://github.com/gogpu/naga/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/naga?style=flat-square&label=)](https://github.com/gogpu/naga/pulls) |
| **[gogpu](https://github.com/gogpu/gogpu)** | Graphics framework, windowing | [![](https://img.shields.io/github/v/release/gogpu/gogpu?style=flat-square&label=)](https://github.com/gogpu/gogpu/releases) | [![](https://img.shields.io/github/stars/gogpu/gogpu?style=flat-square&label=)](https://github.com/gogpu/gogpu) | [![](https://img.shields.io/github/issues/gogpu/gogpu?style=flat-square&label=)](https://github.com/gogpu/gogpu/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/gogpu?style=flat-square&label=)](https://github.com/gogpu/gogpu/pulls) |
| **[gpucontext](https://github.com/gogpu/gpucontext)** | Shared interfaces (DeviceProvider, EventSource) | [![](https://img.shields.io/github/v/release/gogpu/gpucontext?style=flat-square&label=)](https://github.com/gogpu/gpucontext/releases) | [![](https://img.shields.io/github/stars/gogpu/gpucontext?style=flat-square&label=)](https://github.com/gogpu/gpucontext) | [![](https://img.shields.io/github/issues/gogpu/gpucontext?style=flat-square&label=)](https://github.com/gogpu/gpucontext/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/gpucontext?style=flat-square&label=)](https://github.com/gogpu/gpucontext/pulls) |
| **[gputypes](https://github.com/gogpu/gputypes)** | WebGPU types (webgpu.h spec compliant) | [![](https://img.shields.io/github/v/release/gogpu/gputypes?style=flat-square&label=)](https://github.com/gogpu/gputypes/releases) | [![](https://img.shields.io/github/stars/gogpu/gputypes?style=flat-square&label=)](https://github.com/gogpu/gputypes) | [![](https://img.shields.io/github/issues/gogpu/gputypes?style=flat-square&label=)](https://github.com/gogpu/gputypes/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/gputypes?style=flat-square&label=)](https://github.com/gogpu/gputypes/pulls) |
| **[ui](https://github.com/gogpu/ui)** | GUI toolkit *(planning)* | — | [![](https://img.shields.io/github/stars/gogpu/ui?style=flat-square&label=)](https://github.com/gogpu/ui) | [![](https://img.shields.io/github/issues/gogpu/ui?style=flat-square&label=)](https://github.com/gogpu/ui/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/ui?style=flat-square&label=)](https://github.com/gogpu/ui/pulls) |

**Pure Go** | Zero CGO | Cross-platform

---

## Architecture

```
┌─────────────────────────────────────────────────────────────┐
│              Your Application                               │
├─────────────────────────────────────────────────────────────┤
│   gogpu/ui (GUI)   │   born-ml/born   │   Your Framework    │
├─────────────────────────────────────────────────────────────┤
│              gogpu/gg (2D Graphics + ggcanvas)              │
├─────────────────────────────────────────────────────────────┤
│              gogpu/gogpu (Graphics Framework)               │
│         GPU abstraction, windowing, input, math             │
├─────────────────────────────────────────────────────────────┤
│    gogpu/gpucontext (Shared Interfaces)                     │
│       DeviceProvider, EventSource, Registry                 │
├─────────────────────────────────────────────────────────────┤
│    gogpu/gputypes (WebGPU Types, webgpu.h compliant)        │
│       TextureFormat, BufferUsage, PresentMode, etc.         │
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
| **webgpu.h Compliant** | Binary-compatible with wgpu-native |

---

## Quick Start

```go
package main

import (
    "github.com/gogpu/gogpu"
    "github.com/gogpu/gogpu/gmath"
)

func main() {
    app := gogpu.NewApp(gogpu.DefaultConfig().
        WithTitle("Hello GoGPU").
        WithSize(800, 600))

    app.OnDraw(func(dc *gogpu.Context) {
        dc.DrawTriangleColor(gmath.DarkGray)
    })

    app.Run()
}
```

**Result:** A window with a rendered triangle in ~20 lines of code.

---

## gg + gogpu Integration

Use 2D graphics from **gg** directly in **gogpu** windows:

```go
import "github.com/gogpu/gg/integration/ggcanvas"

canvas, _ := ggcanvas.New(app.GPUContextProvider(), 800, 600)
defer canvas.Close()

cc := canvas.Context()
cc.SetRGB(1, 0, 0)
cc.DrawCircle(400, 300, 100)
cc.Fill()

canvas.RenderTo(dc) // Draw to gogpu window
```

---

## Related Projects

| Project | Organization | Purpose | Version | Stars | Issues | PRs |
|:--------|:-------------|:--------|:-------:|:-----:|:------:|:---:|
| **[webgpu](https://github.com/go-webgpu/webgpu)** | go-webgpu | Zero-CGO WebGPU bindings (wgpu-native FFI) | [![](https://img.shields.io/github/v/release/go-webgpu/webgpu?style=flat-square&label=)](https://github.com/go-webgpu/webgpu/releases) | [![](https://img.shields.io/github/stars/go-webgpu/webgpu?style=flat-square&label=)](https://github.com/go-webgpu/webgpu) | [![](https://img.shields.io/github/issues/go-webgpu/webgpu?style=flat-square&label=)](https://github.com/go-webgpu/webgpu/issues) | [![](https://img.shields.io/github/issues-pr/go-webgpu/webgpu?style=flat-square&label=)](https://github.com/go-webgpu/webgpu/pulls) |
| **[goffi](https://github.com/go-webgpu/goffi)** | go-webgpu | Pure Go FFI library (88-114ns overhead) | [![](https://img.shields.io/github/v/release/go-webgpu/goffi?style=flat-square&label=)](https://github.com/go-webgpu/goffi/releases) | [![](https://img.shields.io/github/stars/go-webgpu/goffi?style=flat-square&label=)](https://github.com/go-webgpu/goffi) | [![](https://img.shields.io/github/issues/go-webgpu/goffi?style=flat-square&label=)](https://github.com/go-webgpu/goffi/issues) | [![](https://img.shields.io/github/issues-pr/go-webgpu/goffi?style=flat-square&label=)](https://github.com/go-webgpu/goffi/pulls) |
| **[born](https://github.com/born-ml/born)** | born-ml | Pure Go ML framework (97%+ MNIST) | [![](https://img.shields.io/github/v/release/born-ml/born?style=flat-square&label=)](https://github.com/born-ml/born/releases) | [![](https://img.shields.io/github/stars/born-ml/born?style=flat-square&label=)](https://github.com/born-ml/born) | [![](https://img.shields.io/github/issues/born-ml/born?style=flat-square&label=)](https://github.com/born-ml/born/issues) | [![](https://img.shields.io/github/issues-pr/born-ml/born?style=flat-square&label=)](https://github.com/born-ml/born/pulls) |

---

## Status

| Component | Status | Description |
|:----------|:------:|:------------|
| **gputypes** | ✅ Stable | WebGPU types (webgpu.h spec compliant) |
| **gpucontext** | ✅ Stable | Shared interfaces (zero deps) |
| **wgpu** | ✅ Stable | Vulkan, Metal, GLES, Software backends |
| **naga** | ✅ Stable | SPIR-V, MSL, GLSL, HLSL outputs |
| **gg** | ✅ Stable | 2D graphics + ggcanvas integration |
| **gogpu** | ✅ Stable | Graphics framework, windowing |
| **ui** | 🚧 Planning | GUI widget toolkit |

### Platforms

| Platform | Vulkan | Metal | GLES | Software |
|:---------|:------:|:-----:|:----:|:--------:|
| Windows | ✅ | — | ✅ | ✅ |
| macOS | — | ✅ | — | ✅ |
| Linux (X11) | ✅ | — | ✅ | ✅ |
| Linux (Wayland) | ✅ | — | ✅ | ✅ |

See individual project ROADMAP.md files for detailed roadmaps.

---

## Contributing

We welcome contributions! See individual repository CONTRIBUTING.md files.

**Areas where we need help:**
- WebGPU examples and tutorials
- Documentation
- GUI widget toolkit (gogpu/ui)
- Cross-platform testing (macOS, Linux)

---

## License

All projects are licensed under the **MIT License**.

---

<p align="center">
  <sub>Building the GPU computing ecosystem Go deserves</sub><br>
  <a href="https://github.com/gogpu">github.com/gogpu</a>
</p>
