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
  1.27M+ lines of code. GPU power, Go simplicity. Zero CGO.
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

**GoGPU is to Go what Flutter is to Dart, Qt is to C++, and JavaFX is to Java** — a professional, complete GPU computing ecosystem, not just a single library. From shader compilation and GPU abstraction to 2D/3D rendering, GUI toolkit with themed widgets, and platform integration — all in **Pure Go with zero CGO**.

Inspired by [this discussion on r/golang](https://www.reddit.com/r/golang/comments/1pdw9i7/go_deserves_more_support_in_gui_development/). Go waited 17 years for a professional graphics ecosystem. We're building it — together with you.

---

## Ecosystem

| | Library | Purpose | Version | Stars | Issues | PRs |
|:-:|:--------|:---------------------------------------------------------------------|:-------:|:-----:|:------:|:---:|
| | | ***Foundation*** | | | | |
| 🧱 | **[gputypes](https://github.com/gogpu/gputypes)** | WebGPU types (webgpu.h spec compliant) | [![](https://img.shields.io/github/v/release/gogpu/gputypes?style=flat-square&label=)](https://github.com/gogpu/gputypes/releases) | [![](https://img.shields.io/github/stars/gogpu/gputypes?style=flat-square&label=)](https://github.com/gogpu/gputypes/stargazers) | [![](https://img.shields.io/github/issues/gogpu/gputypes?style=flat-square&label=)](https://github.com/gogpu/gputypes/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/gputypes?style=flat-square&label=)](https://github.com/gogpu/gputypes/pulls) |
| 🧱 | **[naga](https://github.com/gogpu/naga)** | WGSL → SPIR-V/MSL/GLSL/HLSL/DXIL shader compiler (~324K LOC) | [![](https://img.shields.io/github/v/release/gogpu/naga?style=flat-square&label=)](https://github.com/gogpu/naga/releases) | [![](https://img.shields.io/github/stars/gogpu/naga?style=flat-square&label=)](https://github.com/gogpu/naga/stargazers) | [![](https://img.shields.io/github/issues/gogpu/naga?style=flat-square&label=)](https://github.com/gogpu/naga/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/naga?style=flat-square&label=)](https://github.com/gogpu/naga/pulls) |
| | | ***GPU Core*** | | | | |
| ⚙️ | **[wgpu](https://github.com/gogpu/wgpu)** | Unified Go WebGPU — Pure Go + Rust FFI + Browser (Vulkan/Metal/DX12/GLES/Software, ~254K LOC) | [![](https://img.shields.io/github/v/release/gogpu/wgpu?style=flat-square&label=)](https://github.com/gogpu/wgpu/releases) | [![](https://img.shields.io/github/stars/gogpu/wgpu?style=flat-square&label=)](https://github.com/gogpu/wgpu/stargazers) | [![](https://img.shields.io/github/issues/gogpu/wgpu?style=flat-square&label=)](https://github.com/gogpu/wgpu/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/wgpu?style=flat-square&label=)](https://github.com/gogpu/wgpu/pulls) |
| ⚙️ | **[gpucontext](https://github.com/gogpu/gpucontext)** | Shared interfaces (DeviceProvider, EventSource) | [![](https://img.shields.io/github/v/release/gogpu/gpucontext?style=flat-square&label=)](https://github.com/gogpu/gpucontext/releases) | [![](https://img.shields.io/github/stars/gogpu/gpucontext?style=flat-square&label=)](https://github.com/gogpu/gpucontext/stargazers) | [![](https://img.shields.io/github/issues/gogpu/gpucontext?style=flat-square&label=)](https://github.com/gogpu/gpucontext/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/gpucontext?style=flat-square&label=)](https://github.com/gogpu/gpucontext/pulls) |
| ⚙️ | **[galloc](https://github.com/gogpu/galloc)** | O(1) offset allocator for GPU memory sub-allocation (~2.5K LOC) | [![](https://img.shields.io/github/v/release/gogpu/galloc?style=flat-square&label=)](https://github.com/gogpu/galloc/releases) | [![](https://img.shields.io/github/stars/gogpu/galloc?style=flat-square&label=)](https://github.com/gogpu/galloc/stargazers) | [![](https://img.shields.io/github/issues/gogpu/galloc?style=flat-square&label=)](https://github.com/gogpu/galloc/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/galloc?style=flat-square&label=)](https://github.com/gogpu/galloc/pulls) |
| | | ***Framework*** | | | | |
| 🖥️ | **[gogpu](https://github.com/gogpu/gogpu)** | Graphics framework, windowing, compositor (ADR-067, ~104K LOC) | [![](https://img.shields.io/github/v/release/gogpu/gogpu?style=flat-square&label=)](https://github.com/gogpu/gogpu/releases) | [![](https://img.shields.io/github/stars/gogpu/gogpu?style=flat-square&label=)](https://github.com/gogpu/gogpu/stargazers) | [![](https://img.shields.io/github/issues/gogpu/gogpu?style=flat-square&label=)](https://github.com/gogpu/gogpu/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/gogpu?style=flat-square&label=)](https://github.com/gogpu/gogpu/pulls) |
| | | ***Graphics*** | | | | |
| 🎨 | **[gg](https://github.com/gogpu/gg)** | 2D graphics, 5-engine smart rasterizer, GPU acceleration (~312K LOC) | [![](https://img.shields.io/github/v/release/gogpu/gg?style=flat-square&label=)](https://github.com/gogpu/gg/releases) | [![](https://img.shields.io/github/stars/gogpu/gg?style=flat-square&label=)](https://github.com/gogpu/gg/stargazers) | [![](https://img.shields.io/github/issues/gogpu/gg?style=flat-square&label=)](https://github.com/gogpu/gg/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/gg?style=flat-square&label=)](https://github.com/gogpu/gg/pulls) |
| 🎨 | **[g3d](https://github.com/gogpu/g3d)** | Pure Go 3D rendering (scene graph, PBR materials, forward renderer, ~15K LOC) | [![](https://img.shields.io/github/v/release/gogpu/g3d?style=flat-square&label=)](https://github.com/gogpu/g3d/releases) | [![](https://img.shields.io/github/stars/gogpu/g3d?style=flat-square&label=)](https://github.com/gogpu/g3d/stargazers) | [![](https://img.shields.io/github/issues/gogpu/g3d?style=flat-square&label=)](https://github.com/gogpu/g3d/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/g3d?style=flat-square&label=)](https://github.com/gogpu/g3d/pulls) |
| 🎨 | **[gg-pdf](https://github.com/gogpu/gg-pdf)** | PDF export backend for gg recording | [![](https://img.shields.io/github/v/release/gogpu/gg-pdf?style=flat-square&label=)](https://github.com/gogpu/gg-pdf/releases) | [![](https://img.shields.io/github/stars/gogpu/gg-pdf?style=flat-square&label=)](https://github.com/gogpu/gg-pdf/stargazers) | [![](https://img.shields.io/github/issues/gogpu/gg-pdf?style=flat-square&label=)](https://github.com/gogpu/gg-pdf/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/gg-pdf?style=flat-square&label=)](https://github.com/gogpu/gg-pdf/pulls) |
| 🎨 | **[gg-svg](https://github.com/gogpu/gg-svg)** | SVG export backend for gg recording | [![](https://img.shields.io/github/v/release/gogpu/gg-svg?style=flat-square&label=)](https://github.com/gogpu/gg-svg/releases) | [![](https://img.shields.io/github/stars/gogpu/gg-svg?style=flat-square&label=)](https://github.com/gogpu/gg-svg/stargazers) | [![](https://img.shields.io/github/issues/gogpu/gg-svg?style=flat-square&label=)](https://github.com/gogpu/gg-svg/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/gg-svg?style=flat-square&label=)](https://github.com/gogpu/gg-svg/pulls) |
| | | ***Application*** | | | | |
| 📱 | **[ui](https://github.com/gogpu/ui)** | Enterprise GUI toolkit (27 widgets, 4 design systems, Layer Tree compositor, ~220K LOC) | [![](https://img.shields.io/github/v/release/gogpu/ui?style=flat-square&label=)](https://github.com/gogpu/ui/releases) | [![](https://img.shields.io/github/stars/gogpu/ui?style=flat-square&label=)](https://github.com/gogpu/ui/stargazers) | [![](https://img.shields.io/github/issues/gogpu/ui?style=flat-square&label=)](https://github.com/gogpu/ui/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/ui?style=flat-square&label=)](https://github.com/gogpu/ui/pulls) |
| 📱 | **[editor](https://github.com/gogpu/editor)** | Text/Code editor widget — GPU-accelerated, embeddable (like Monaco) | [![](https://img.shields.io/badge/-early_dev-orange?style=flat-square)](https://github.com/gogpu/editor) | [![](https://img.shields.io/github/stars/gogpu/editor?style=flat-square&label=)](https://github.com/gogpu/editor/stargazers) | [![](https://img.shields.io/github/issues/gogpu/editor?style=flat-square&label=)](https://github.com/gogpu/editor/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/editor?style=flat-square&label=)](https://github.com/gogpu/editor/pulls) |
| | | ***Platform Services*** | | | | |
| 🔧 | **[systray](https://github.com/gogpu/systray)** | Pure Go system tray (Win32/macOS/Linux, zero CGO, ~8K LOC) | [![](https://img.shields.io/github/v/release/gogpu/systray?style=flat-square&label=)](https://github.com/gogpu/systray/releases) | [![](https://img.shields.io/github/stars/gogpu/systray?style=flat-square&label=)](https://github.com/gogpu/systray/stargazers) | [![](https://img.shields.io/github/issues/gogpu/systray?style=flat-square&label=)](https://github.com/gogpu/systray/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/systray?style=flat-square&label=)](https://github.com/gogpu/systray/pulls) |
| 🔧 | **[audio](https://github.com/gogpu/audio)** | Pure Go audio engine (WASAPI/CoreAudio/PulseAudio, zero CGO) | [![](https://img.shields.io/github/v/release/gogpu/audio?style=flat-square&label=)](https://github.com/gogpu/audio/releases) | [![](https://img.shields.io/github/stars/gogpu/audio?style=flat-square&label=)](https://github.com/gogpu/audio/stargazers) | [![](https://img.shields.io/github/issues/gogpu/audio?style=flat-square&label=)](https://github.com/gogpu/audio/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/audio?style=flat-square&label=)](https://github.com/gogpu/audio/pulls) |
| 🔧 | **[compose](https://github.com/gogpu/compose)** | Multi-process composition (Unix socket IPC, LZ4, ~10K LOC) | [![](https://img.shields.io/github/v/release/gogpu/compose?style=flat-square&label=)](https://github.com/gogpu/compose/releases) | [![](https://img.shields.io/github/stars/gogpu/compose?style=flat-square&label=)](https://github.com/gogpu/compose/stargazers) | [![](https://img.shields.io/github/issues/gogpu/compose?style=flat-square&label=)](https://github.com/gogpu/compose/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/compose?style=flat-square&label=)](https://github.com/gogpu/compose/pulls) |
| 🎮 | **[gamepad](https://github.com/gogpu/gamepad)** | Pure Go gamepad/joystick input — XInput, evdev, IOKit, W3C | [![](https://img.shields.io/badge/-early_dev-orange?style=flat-square)](https://github.com/gogpu/gamepad) | [![](https://img.shields.io/github/stars/gogpu/gamepad?style=flat-square&label=)](https://github.com/gogpu/gamepad/stargazers) | [![](https://img.shields.io/github/issues/gogpu/gamepad?style=flat-square&label=)](https://github.com/gogpu/gamepad/issues) | [![](https://img.shields.io/github/issues-pr/gogpu/gamepad?style=flat-square&label=)](https://github.com/gogpu/gamepad/pulls) |

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
│    Windowing, compositor (ADR-067), damage overlay, input   │
│  gogpu/systray   gogpu/audio   gogpu/gamepad (🚧)           │
├─────────────────────────────────────────────────────────────┤
│    gogpu/gpucontext (Shared Interfaces)                     │
│ DeviceProvider, SurfaceCompositor, DamageSource, EventSource│
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
package main

import (
    "log"

    "github.com/gogpu/gg"
    _ "github.com/gogpu/gg/gpu" // Register GPU accelerator
    "github.com/gogpu/gg/integration/ggcanvas"
    "github.com/gogpu/gogpu"
)

func main() {
    app := gogpu.NewApp(gogpu.DefaultConfig().
        WithTitle("gg + gogpu").
        WithSize(800, 600))

    var canvas *ggcanvas.Canvas

    app.OnDraw(func(dc *gogpu.Context) {
        w, h := dc.Width(), dc.Height()
        if canvas == nil {
            var err error
            canvas, err = ggcanvas.New(app.GPUContextProvider(), w, h)
            if err != nil {
                log.Fatal(err)
            }
        }

        canvas.Draw(func(cc *gg.Context) {
            cc.SetRGB(1, 0, 0)
            cc.DrawCircle(400, 300, 100)
            cc.Fill()
        })

        canvas.Render(dc.RenderTarget()) // GPU-direct, zero-copy
    })

    app.Run()
}
```

---

## Related Projects

| Project | Organization | Purpose | Version | Stars | Issues | PRs |
|:--------|:-------------|:--------|:-------:|:-----:|:------:|:---:|
| **[webgpu](https://github.com/go-webgpu/webgpu)** | go-webgpu | Zero-CGO WebGPU bindings (wgpu-native FFI) | [![](https://img.shields.io/github/v/release/go-webgpu/webgpu?style=flat-square&label=)](https://github.com/go-webgpu/webgpu/releases) | [![](https://img.shields.io/github/stars/go-webgpu/webgpu?style=flat-square&label=)](https://github.com/go-webgpu/webgpu/stargazers) | [![](https://img.shields.io/github/issues/go-webgpu/webgpu?style=flat-square&label=)](https://github.com/go-webgpu/webgpu/issues) | [![](https://img.shields.io/github/issues-pr/go-webgpu/webgpu?style=flat-square&label=)](https://github.com/go-webgpu/webgpu/pulls) |
| **[goffi](https://github.com/go-webgpu/goffi)** | go-webgpu | Pure Go FFI library (88-114ns overhead) | [![](https://img.shields.io/github/v/release/go-webgpu/goffi?style=flat-square&label=)](https://github.com/go-webgpu/goffi/releases) | [![](https://img.shields.io/github/stars/go-webgpu/goffi?style=flat-square&label=)](https://github.com/go-webgpu/goffi/stargazers) | [![](https://img.shields.io/github/issues/go-webgpu/goffi?style=flat-square&label=)](https://github.com/go-webgpu/goffi/issues) | [![](https://img.shields.io/github/issues-pr/go-webgpu/goffi?style=flat-square&label=)](https://github.com/go-webgpu/goffi/pulls) |
| **[born](https://github.com/born-ml/born)** | born-ml | Pure Go ML framework (97%+ MNIST) | [![](https://img.shields.io/github/v/release/born-ml/born?style=flat-square&label=)](https://github.com/born-ml/born/releases) | [![](https://img.shields.io/github/stars/born-ml/born?style=flat-square&label=)](https://github.com/born-ml/born/stargazers) | [![](https://img.shields.io/github/issues/born-ml/born?style=flat-square&label=)](https://github.com/born-ml/born/issues) | [![](https://img.shields.io/github/issues-pr/born-ml/born?style=flat-square&label=)](https://github.com/born-ml/born/pulls) |

---

## Tutorials & Articles

We haven't had time to write comprehensive tutorials yet — we've been focused on building the ecosystem itself. But the community has started filling that gap:

### Community Tutorials

🇨🇿 **Pavel Tišnovský** ([root.cz](https://www.root.cz) — Czech Republic's leading tech portal) wrote two in-depth tutorials covering the `gg` 2D graphics library with 54 working [examples](https://github.com/tisnik/go-root):

1. [Creating 2D/3D Graphics and Animations in Go with GoGPU](https://www.root.cz/clanky/tvorba-2d-i-3d-grafiky-a-animaci-v-go-s-vyuzitim-projektu-gogpu/) — 49 min read. Paths, Bézier curves, transforms, text, animations.
2. [GoGPU Part 2: Gradients, SVG & PDF Export](https://www.root.cz/clanky/tvorba-2d-i-3d-grafiky-a-animaci-v-go-s-vyuzitim-projektu-gogpu-2-cast/) — 39 min read. Gradients, vector export, GUI integration.
3. [Interactive Applications with GUI using GoGPU](https://root.cz/clanky/tvorba-interaktivnich-aplikaci-s-gui-s-vyuzitim-projektu-gogpu/) — ~40 min read. Windowing, ggcanvas, keyboard/mouse input, interactive Bezier editor.

> Articles are in Czech — use [Google Translate](https://translate.google.com/) for other languages. The code examples are universal.

### Our Articles

- [Google Says Go Is Ideal for AI-Assisted Engineering. We've Been Proving It for a Year.](https://dev.to/kolkov/google-says-go-is-ideal-for-ai-assisted-engineering-weve-been-proving-it-for-a-year-2j7p) — Dev.to
- [Extracting a GPU Compositor in Pure Go — Patterns from Flutter and Chromium](https://dev.to/kolkov/gogpu-extracting-a-gpu-compositor-in-pure-go-patterns-from-flutter-and-chromium-9ig) — Dev.to
- [GoGPU: From Idea to 100K Lines](https://dev.to/kolkov/gogpu-from-idea-to-100k-lines-in-two-weeks-building-gos-gpu-ecosystem-3b2) — Dev.to
- [GoGPU Announcement](https://dev.to/kolkov/gogpu-a-pure-go-graphics-library-for-gpu-programming-2j5d) — Dev.to
- [First Pure Go DXIL Generator](https://dev.to/kolkov/we-built-the-first-pure-go-dxil-generator-because-optimizing-the-wrong-path-wasnt-enough-35en) — Dev.to

---

## Status

| Layer | Component | Status | Description |
|:------|:----------|:------:|:------------|
| Foundation | **gputypes** | ✅ v0.5.2 | WebGPU types (webgpu.h spec compliant) |
| Foundation | **naga** | ✅ v0.18.0 | SPIR-V, MSL, GLSL, HLSL + DXIL shader compiler, ~324K LOC |
| GPU Core | **wgpu** | ✅ v0.31.6 | Triple-backend: Pure Go (Vulkan/Metal/DX12/GLES/Software), Rust FFI, Browser WASM, ~254K LOC |
| GPU Core | **galloc** | ✅ v0.2.1 | O(1) offset allocator (TLSF-inspired, 256 bins, zero heap allocs) |
| GPU Core | **gpucontext** | ✅ v0.28.0 | Shared interfaces — DeviceProvider, SurfaceCompositor, DamageSource |
| Framework | **gogpu** | ✅ v0.53.0 | Graphics framework, windowing, compositor, native printing, ~104K LOC |
| Graphics | **gg** | ✅ v0.52.3 | 2D graphics, 5-engine rasterizer, GPU acceleration, recording, ggcanvas, ~312K LOC |
| Graphics | **g3d** | ✅ v0.1.9 | Pure Go 3D rendering — scene graph, PBR materials, forward renderer, ~15K LOC |
| Graphics | **gg-pdf** | ✅ v0.1.0 | PDF export backend for gg |
| Graphics | **gg-svg** | ✅ v0.1.0 | SVG export backend for gg |
| Application | **ui** | ✅ v0.1.54 | Enterprise GUI toolkit — 27 widgets, 4 design systems, Layer Tree compositor, ~220K LOC |
| Application | **editor** | 🚧 Early dev | Text/Code editor widget — GPU-accelerated, embeddable (like Monaco) |
| Platform | **systray** | ✅ v0.2.8 | System tray — Win32/macOS/Linux, dark mode, notifications, ~8K LOC |
| Platform | **audio** | ✅ v0.1.0 | Pure Go audio engine — WASAPI driver, WAV decoder, Mixer |
| Platform | **compose** | ✅ v0.2.0 | Multi-process composition — Unix socket transport, LZ4, pull-based flow, ~10K LOC |
| Platform | **gamepad** | 🚧 Early dev | Pure Go gamepad/joystick input — XInput, evdev, IOKit, W3C Gamepad API |

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
  <a href="https://gogpu.io">gogpu.io</a> · <a href="mailto:info@gogpu.io">info@gogpu.io</a> · <a href="https://github.com/gogpu">GitHub</a>
</p>
