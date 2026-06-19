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
  1.1M+ lines of code. GPU power, Go simplicity. Zero CGO.
</p>

<p align="center">
  <a href="https://github.com/gogpu/gogpu"><img src="https://img.shields.io/badge/Go-1.25+-00ADD8?style=flat&logo=go" alt="Go Version"></a>
  <a href="https://github.com/gogpu/gogpu/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License"></a>
  <a href="https://github.com/gogpu"><img src="https://img.shields.io/badge/Pure_Go-Zero_CGO-brightgreen?style=flat" alt="Pure Go"></a>
  <a href="https://github.com/gogpu/gogpu/discussions"><img src="https://img.shields.io/github/discussions/gogpu/gogpu?style=flat&labelColor=555&color=blue" alt="Discussions"></a>
  <a href="https://opencollective.com/gogpu"><img src="https://img.shields.io/opencollective/all/gogpu?style=flat&label=sponsors&color=brightgreen" alt="Open Collective"></a>
</p>

---

## Why GoGPU?

**GoGPU is to Go what Flutter is to Dart and Qt is to C++** — a complete GPU computing ecosystem, not just a single library. From shader compilation and GPU abstraction to 2D/3D rendering, GUI toolkit with themed widgets, and platform integration — all in **Pure Go with zero CGO**.

Inspired by [this discussion on r/golang](https://www.reddit.com/r/golang/comments/1pdw9i7/go_deserves_more_support_in_gui_development/). Go waited 17 years for a professional graphics ecosystem. We're building it.

---

## Ecosystem

| Library | Purpose                                                              | Version | Stars | Issues | PRs |
|:--------|:---------------------------------------------------------------------|:-------:|:-----:|:------:|:---:|
| **[gg](https://github.com/gogpu/gg)** | 2D graphics, 5-engine smart rasterizer, GPU acceleration (~215K LOC) | [![](https://img.shields.io/github/v/release/gogpu/gg?style=flat-square&label=)](https://github.com/gogpu/gg/releases) | [![](https://img.shields.io/github/stars/gogpu/gg?style=flat-square&label=)](https://github.com/gogpu/gg/stargazers) | [![](https://img.shields.io/github/issues/gogpu/gg?style=flat-square&label=)](https://github.com/gogpu/gg/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/gg?style=flat-square&label=)](https://github.com/gogpu/gg/pulls) |
| **[wgpu](https://github.com/gogpu/wgpu)** | Unified Go WebGPU — Pure Go + Rust FFI + Browser (Vulkan/Metal/DX12/GLES/Software, ~130K LOC) | [![](https://img.shields.io/github/v/release/gogpu/wgpu?style=flat-square&label=)](https://github.com/gogpu/wgpu/releases) | [![](https://img.shields.io/github/stars/gogpu/wgpu?style=flat-square&label=)](https://github.com/gogpu/wgpu/stargazers) | [![](https://img.shields.io/github/issues/gogpu/wgpu?style=flat-square&label=)](https://github.com/gogpu/wgpu/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/wgpu?style=flat-square&label=)](https://github.com/gogpu/wgpu/pulls) |
| **[naga](https://github.com/gogpu/naga)** | WGSL → SPIR-V/MSL/GLSL/HLSL/DXIL shader compiler (~189K LOC)                 | [![](https://img.shields.io/github/v/release/gogpu/naga?style=flat-square&label=)](https://github.com/gogpu/naga/releases) | [![](https://img.shields.io/github/stars/gogpu/naga?style=flat-square&label=)](https://github.com/gogpu/naga/stargazers) | [![](https://img.shields.io/github/issues/gogpu/naga?style=flat-square&label=)](https://github.com/gogpu/naga/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/naga?style=flat-square&label=)](https://github.com/gogpu/naga/pulls) |
| **[gogpu](https://github.com/gogpu/gogpu)** | Graphics framework, windowing (~53K LOC)                             | [![](https://img.shields.io/github/v/release/gogpu/gogpu?style=flat-square&label=)](https://github.com/gogpu/gogpu/releases) | [![](https://img.shields.io/github/stars/gogpu/gogpu?style=flat-square&label=)](https://github.com/gogpu/gogpu/stargazers) | [![](https://img.shields.io/github/issues/gogpu/gogpu?style=flat-square&label=)](https://github.com/gogpu/gogpu/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/gogpu?style=flat-square&label=)](https://github.com/gogpu/gogpu/pulls) |
| **[gpucontext](https://github.com/gogpu/gpucontext)** | Shared interfaces (DeviceProvider, EventSource)                      | [![](https://img.shields.io/github/v/release/gogpu/gpucontext?style=flat-square&label=)](https://github.com/gogpu/gpucontext/releases) | [![](https://img.shields.io/github/stars/gogpu/gpucontext?style=flat-square&label=)](https://github.com/gogpu/gpucontext/stargazers) | [![](https://img.shields.io/github/issues/gogpu/gpucontext?style=flat-square&label=)](https://github.com/gogpu/gpucontext/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/gpucontext?style=flat-square&label=)](https://github.com/gogpu/gpucontext/pulls) |
| **[gputypes](https://github.com/gogpu/gputypes)** | WebGPU types (webgpu.h spec compliant)                               | [![](https://img.shields.io/github/v/release/gogpu/gputypes?style=flat-square&label=)](https://github.com/gogpu/gputypes/releases) | [![](https://img.shields.io/github/stars/gogpu/gputypes?style=flat-square&label=)](https://github.com/gogpu/gputypes/stargazers) | [![](https://img.shields.io/github/issues/gogpu/gputypes?style=flat-square&label=)](https://github.com/gogpu/gputypes/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/gputypes?style=flat-square&label=)](https://github.com/gogpu/gputypes/pulls) |
| **[gg-pdf](https://github.com/gogpu/gg-pdf)** | PDF export backend for gg recording                                  | [![](https://img.shields.io/github/v/release/gogpu/gg-pdf?style=flat-square&label=)](https://github.com/gogpu/gg-pdf/releases) | [![](https://img.shields.io/github/stars/gogpu/gg-pdf?style=flat-square&label=)](https://github.com/gogpu/gg-pdf/stargazers) | [![](https://img.shields.io/github/issues/gogpu/gg-pdf?style=flat-square&label=)](https://github.com/gogpu/gg-pdf/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/gg-pdf?style=flat-square&label=)](https://github.com/gogpu/gg-pdf/pulls) |
| **[gg-svg](https://github.com/gogpu/gg-svg)** | SVG export backend for gg recording                                  | [![](https://img.shields.io/github/v/release/gogpu/gg-svg?style=flat-square&label=)](https://github.com/gogpu/gg-svg/releases) | [![](https://img.shields.io/github/stars/gogpu/gg-svg?style=flat-square&label=)](https://github.com/gogpu/gg-svg/stargazers) | [![](https://img.shields.io/github/issues/gogpu/gg-svg?style=flat-square&label=)](https://github.com/gogpu/gg-svg/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/gg-svg?style=flat-square&label=)](https://github.com/gogpu/gg-svg/pulls) |
| **[ui](https://github.com/gogpu/ui)** | Enterprise GUI toolkit (22 widgets, M3/Fluent/Cupertino, ~167K LOC)  | [![](https://img.shields.io/github/v/release/gogpu/ui?style=flat-square&label=)](https://github.com/gogpu/ui/releases) | [![](https://img.shields.io/github/stars/gogpu/ui?style=flat-square&label=)](https://github.com/gogpu/ui/stargazers) | [![](https://img.shields.io/github/issues/gogpu/ui?style=flat-square&label=)](https://github.com/gogpu/ui/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/ui?style=flat-square&label=)](https://github.com/gogpu/ui/pulls) |
| **[g3d](https://github.com/gogpu/g3d)** | Pure Go 3D rendering (scene graph, PBR materials, forward renderer, ~12K LOC) | [![](https://img.shields.io/github/v/release/gogpu/g3d?style=flat-square&label=)](https://github.com/gogpu/g3d/releases) | [![](https://img.shields.io/github/stars/gogpu/g3d?style=flat-square&label=)](https://github.com/gogpu/g3d/stargazers) | [![](https://img.shields.io/github/issues/gogpu/g3d?style=flat-square&label=)](https://github.com/gogpu/g3d/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/g3d?style=flat-square&label=)](https://github.com/gogpu/g3d/pulls) |
| **[systray](https://github.com/gogpu/systray)** | Pure Go system tray (Win32/macOS/Linux, zero CGO, ~6.2K LOC)         | [![](https://img.shields.io/github/v/release/gogpu/systray?style=flat-square&label=)](https://github.com/gogpu/systray/releases) | [![](https://img.shields.io/github/stars/gogpu/systray?style=flat-square&label=)](https://github.com/gogpu/systray/stargazers) | [![](https://img.shields.io/github/issues/gogpu/systray?style=flat-square&label=)](https://github.com/gogpu/systray/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/systray?style=flat-square&label=)](https://github.com/gogpu/systray/pulls) |
| **[audio](https://github.com/gogpu/audio)** | Pure Go audio engine (WASAPI/CoreAudio/PulseAudio, zero CGO)         | [![](https://img.shields.io/github/v/release/gogpu/audio?style=flat-square&label=)](https://github.com/gogpu/audio/releases) | [![](https://img.shields.io/github/stars/gogpu/audio?style=flat-square&label=)](https://github.com/gogpu/audio/stargazers) | [![](https://img.shields.io/github/issues/gogpu/audio?style=flat-square&label=)](https://github.com/gogpu/audio/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/audio?style=flat-square&label=)](https://github.com/gogpu/audio/pulls) |
| **[editor](https://github.com/gogpu/editor)** | Text/Code editor widget — GPU-accelerated, embeddable (like Monaco)   | [![](https://img.shields.io/badge/-early_dev-orange?style=flat-square)](https://github.com/gogpu/editor) | [![](https://img.shields.io/github/stars/gogpu/editor?style=flat-square&label=)](https://github.com/gogpu/editor/stargazers) | [![](https://img.shields.io/github/issues/gogpu/editor?style=flat-square&label=)](https://github.com/gogpu/editor/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/editor?style=flat-square&label=)](https://github.com/gogpu/editor/pulls) |
| **[compose](https://github.com/gogpu/compose)** | Multi-process composition (Unix socket IPC, LZ4, ~9K LOC)            | [![](https://img.shields.io/github/v/release/gogpu/compose?style=flat-square&label=)](https://github.com/gogpu/compose/releases) | [![](https://img.shields.io/github/stars/gogpu/compose?style=flat-square&label=)](https://github.com/gogpu/compose/stargazers) | [![](https://img.shields.io/github/issues/gogpu/compose?style=flat-square&label=)](https://github.com/gogpu/compose/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/compose?style=flat-square&label=)](https://github.com/gogpu/compose/pulls) |

**Pure Go** | Zero CGO | Cross-platform

---

## Architecture

```
┌─────────────────────────────────────────────────────────────┐
│              Your Application                               │
├─────────────────────────────────────────────────────────────┤
│   gogpu/ui (GUI)   │   born-ml/born   │   Your Framework    │
├─────────────────────────────────────────────────────────────┤
│  gogpu/gg (2D Graphics)  │  gogpu/g3d (3D Rendering)        │
│   Smart Rasterizer: Scanline│4×4 Tiles│16×16│SDF│Compute    │
│                 ↓ export to ↓                               │
│           gg-pdf (PDF)    gg-svg (SVG)                      │
├─────────────────────────────────────────────────────────────┤
│              gogpu/gogpu (Graphics Framework)               │
│         GPU abstraction, windowing, input, math             │
│     gogpu/systray (System Tray)   gogpu/audio (Audio)       │
├─────────────────────────────────────────────────────────────┤
│    gogpu/gpucontext (Shared Interfaces)                     │
│       DeviceProvider, EventSource, Registry                 │
├─────────────────────────────────────────────────────────────┤
│    gogpu/gputypes (WebGPU Types, webgpu.h compliant)        │
│       TextureFormat, BufferUsage, PresentMode, etc.         │
├─────────────────────────────────────────────────────────────┤
│       gogpu/wgpu (Unified WebGPU: Pure Go │ Rust FFI │ WASM)│
├─────────────────────────────────────────────────────────────┤
│                   gogpu/naga (Shader Compiler)              │
│       (WGSL → SPIR-V/MSL/GLSL/HLSL/DXIL)                    │
├─────────────────────────────────────────────────────────────┤
│        Vulkan │ Metal │ DX12 │ OpenGL │ Software            │
└─────────────────────────────────────────────────────────────┘
```

---

## Key Features

| Feature | Description |
|:--------|:------------|
| **Zero CGO** | No C compiler required, simple `go build` |
| **WebGPU API** | Modern, portable GPU abstraction |
| **Smart Rasterizer** | 5 algorithms with per-path auto-selection (scanline, 4×4 tiles, 16×16 tiles, SDF, compute) |
| **Triple Backend** | Pure Go (default), Rust FFI (`-tags rust`), Browser WASM — same API, build tag selects |
| **Layered Design** | Use only what you need |
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

Use 2D graphics from **gg** directly in **gogpu** windows — with smart rasterizer auto-selection and GPU-direct rendering (zero CPU readback):

```go
import (
    "github.com/gogpu/gg"
    "github.com/gogpu/gg/integration/ggcanvas"
)

canvas, _ := ggcanvas.New(app.GPUContextProvider(), 800, 600)

app.OnDraw(func(dc *gogpu.Context) {
    sv := dc.SurfaceView()
    sw, sh := dc.SurfaceSize()
    gg.SetAcceleratorSurfaceTarget(sv, sw, sh)

    canvas.Draw(func(cc *gg.Context) {
        cc.SetRGB(1, 0, 0)
        cc.DrawCircle(400, 300, 100)
        cc.Fill()
    })

    canvas.RenderDirect(sv, sw, sh) // GPU-direct, zero-copy
})
```

---

## Related Projects

| Project | Organization | Purpose | Version | Stars | Issues | PRs |
|:--------|:-------------|:--------|:-------:|:-----:|:------:|:---:|
| **[webgpu](https://github.com/go-webgpu/webgpu)** | go-webgpu | Zero-CGO WebGPU bindings (wgpu-native FFI) | [![](https://img.shields.io/github/v/release/go-webgpu/webgpu?style=flat-square&label=)](https://github.com/go-webgpu/webgpu/releases) | [![](https://img.shields.io/github/stars/go-webgpu/webgpu?style=flat-square&label=)](https://github.com/go-webgpu/webgpu/stargazers) | [![](https://img.shields.io/github/issues/go-webgpu/webgpu?style=flat-square&label=)](https://github.com/go-webgpu/webgpu/issues) | [![](https://img.shields.io/github/issues-pr/go-webgpu/webgpu?style=flat-square&label=)](https://github.com/go-webgpu/webgpu/pulls) |
| **[goffi](https://github.com/go-webgpu/goffi)** | go-webgpu | Pure Go FFI library (88-114ns overhead) | [![](https://img.shields.io/github/v/release/go-webgpu/goffi?style=flat-square&label=)](https://github.com/go-webgpu/goffi/releases) | [![](https://img.shields.io/github/stars/go-webgpu/goffi?style=flat-square&label=)](https://github.com/go-webgpu/goffi/stargazers) | [![](https://img.shields.io/github/issues/go-webgpu/goffi?style=flat-square&label=)](https://github.com/go-webgpu/goffi/issues) | [![](https://img.shields.io/github/issues-pr/go-webgpu/goffi?style=flat-square&label=)](https://github.com/go-webgpu/goffi/pulls) |
| **[born](https://github.com/born-ml/born)** | born-ml | Pure Go ML framework (97%+ MNIST) | [![](https://img.shields.io/github/v/release/born-ml/born?style=flat-square&label=)](https://github.com/born-ml/born/releases) | [![](https://img.shields.io/github/stars/born-ml/born?style=flat-square&label=)](https://github.com/born-ml/born/stargazers) | [![](https://img.shields.io/github/issues/born-ml/born?style=flat-square&label=)](https://github.com/born-ml/born/issues) | [![](https://img.shields.io/github/issues-pr/born-ml/born?style=flat-square&label=)](https://github.com/born-ml/born/pulls) |

---

## Status

| Component | Status | Description |
|:----------|:------:|:------------|
| **gputypes** | ✅ Stable | WebGPU types (webgpu.h spec compliant) |
| **gpucontext** | ✅ Stable | Shared interfaces (zero deps) |
| **wgpu** | ✅ Stable | Triple-backend: Pure Go (Vulkan/Metal/DX12/GLES/Software), Rust FFI, Browser WASM |
| **naga** | ✅ Stable | SPIR-V, MSL, GLSL, HLSL + DXIL (experimental) outputs |
| **gg** | ✅ Stable | 2D graphics, 5-engine rasterizer, recording, ggcanvas |
| **gg-pdf** | ✅ Stable | PDF export backend for gg |
| **gg-svg** | ✅ Stable | SVG export backend for gg |
| **gogpu** | ✅ Stable | Graphics framework, windowing |
| **ui** | ✅ v0.1.1 | Enterprise GUI toolkit — 22 widgets, Material 3 / Fluent / Cupertino themes, ~167K LOC |
| **systray** | ✅ v0.1.0 | System tray — Win32/macOS/Linux, dark mode, notifications, 72 tests |
| **audio** | ✅ v0.1.0 | Pure Go audio engine — WASAPI driver, WAV decoder, Mixer, 42 tests |
| **g3d** | ✅ v0.1.0 | Pure Go 3D rendering — scene graph, PBR materials, forward renderer, 5 backends, ~12K LOC |
| **editor** | 🚧 Early dev | Text/Code editor widget — GPU-accelerated, embeddable (like Monaco) |
| **compose** | ✅ v0.1.0 | Multi-process composition — Unix socket transport, LZ4, pull-based flow, ~9K LOC |

### Platforms

| Platform | Vulkan | DX12 | Metal | GLES | Software | Rust FFI | Browser |
|:---------|:------:|:----:|:-----:|:----:|:--------:|:--------:|:-------:|
| Windows | ✅ | ✅ | — | ✅ | ✅ | ✅ | — |
| macOS | — | — | ✅ | — | ✅ | ⚠️ | — |
| Linux (X11) | ✅ | — | — | ✅ | ✅ | ✅ | — |
| Linux (Wayland) | ✅ | — | — | ✅ | ✅ | ✅ | — |
| **Browser/WASM** | — | — | — | — | — | — | ✅ |

See individual project ROADMAP.md files for detailed roadmaps.

---

## Support

GoGPU is free and open source. If you find it useful, please consider supporting continued development:

🥇 **First Sponsor:** [Inkflow](https://opencollective.com/inkflow) ([@omer316](https://github.com/omer316)) — the person who asked "is there a way to support this project?" and then became the answer!

<a href="https://opencollective.com/gogpu/donate"><img src="https://opencollective.com/gogpu/donate/button@2x.png?color=blue" width="200" /></a>

### Backers

<a href="https://opencollective.com/gogpu#backer"><img src="https://opencollective.com/gogpu/backers.svg?avatarHeight=36&width=600" /></a>

### Sponsors

<a href="https://opencollective.com/gogpu#sponsor"><img src="https://opencollective.com/gogpu/sponsors.svg?avatarHeight=60&width=600" /></a>

---

## Contributing

We welcome contributions! See individual repository CONTRIBUTING.md files.

**Areas where we need help:**
- GUI widgets and themes for gogpu/ui
- Cross-platform testing (macOS, Linux)
- WebGPU examples and tutorials
- Documentation

---

## License

All projects are licensed under the **MIT License**.

---

<p align="center">
  <img src="https://raw.githubusercontent.com/gogpu/.github/main/assets/go-love-gpu.png" alt="GO ❤ GPU" width="280" />
</p>

<p align="center">
  <sub>Building the GPU computing ecosystem Go deserves</sub><br>
  <a href="https://github.com/gogpu">github.com/gogpu</a>
</p>
