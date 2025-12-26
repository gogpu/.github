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
  <a href="https://github.com/gogpu"><img src="https://img.shields.io/badge/Pure_Go-224K_LOC-brightgreen?style=flat" alt="224K LOC"></a>
  <a href="https://github.com/gogpu/gogpu/discussions"><img src="https://img.shields.io/github/discussions/gogpu/gogpu?style=flat&labelColor=555&color=blue" alt="Discussions"></a>
</p>

---

## Why GoGPU?

Inspired by [this discussion on r/golang](https://www.reddit.com/r/golang/comments/1pdw9i7/go_deserves_more_support_in_gui_development/), we're building the GPU computing ecosystem that Go deserves — from low-level graphics to high-level GUI, all with **zero CGO**.

---

## Ecosystem

| Library | Purpose | LOC | Stars | Issues |
|:--------|:--------|----:|:-----:|:------:|
| **[gg](https://github.com/gogpu/gg)** | 2D graphics, Canvas API, GPU compute | ~104K | [![](https://img.shields.io/github/stars/gogpu/gg?style=flat-square&label=)](https://github.com/gogpu/gg) | [![](https://img.shields.io/github/issues/gogpu/gg?style=flat-square&label=)](https://github.com/gogpu/gg/issues) |
| **[wgpu](https://github.com/gogpu/wgpu)** | Pure Go WebGPU (Vulkan/Metal/GLES) | ~71K | [![](https://img.shields.io/github/stars/gogpu/wgpu?style=flat-square&label=)](https://github.com/gogpu/wgpu) | [![](https://img.shields.io/github/issues/gogpu/wgpu?style=flat-square&label=)](https://github.com/gogpu/wgpu/issues) |
| **[gogpu](https://github.com/gogpu/gogpu)** | Graphics framework, windowing | ~26K | [![](https://img.shields.io/github/stars/gogpu/gogpu?style=flat-square&label=)](https://github.com/gogpu/gogpu) | [![](https://img.shields.io/github/issues/gogpu/gogpu?style=flat-square&label=)](https://github.com/gogpu/gogpu/issues) |
| **[naga](https://github.com/gogpu/naga)** | WGSL → SPIR-V/MSL/GLSL compiler | ~23K | [![](https://img.shields.io/github/stars/gogpu/naga?style=flat-square&label=)](https://github.com/gogpu/naga) | [![](https://img.shields.io/github/issues/gogpu/naga?style=flat-square&label=)](https://github.com/gogpu/naga/issues) |
| **[ui](https://github.com/gogpu/ui)** | GUI toolkit *(planned)* | — | [![](https://img.shields.io/github/stars/gogpu/ui?style=flat-square&label=)](https://github.com/gogpu/ui) | [![](https://img.shields.io/github/issues/gogpu/ui?style=flat-square&label=)](https://github.com/gogpu/ui/issues) |

**Total: ~224K LOC Pure Go** | Zero CGO | Cross-platform

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

## Related Projects

| Project | Organization | Purpose | Stars | Issues |
|:--------|:-------------|:--------|:-----:|:------:|
| **[webgpu](https://github.com/go-webgpu/webgpu)** | go-webgpu | Zero-CGO WebGPU bindings (wgpu-native FFI) | [![](https://img.shields.io/github/stars/go-webgpu/webgpu?style=flat-square&label=)](https://github.com/go-webgpu/webgpu) | [![](https://img.shields.io/github/issues/go-webgpu/webgpu?style=flat-square&label=)](https://github.com/go-webgpu/webgpu/issues) |
| **[goffi](https://github.com/go-webgpu/goffi)** | go-webgpu | Pure Go FFI library (88-114ns overhead) | [![](https://img.shields.io/github/stars/go-webgpu/goffi?style=flat-square&label=)](https://github.com/go-webgpu/goffi) | [![](https://img.shields.io/github/issues/go-webgpu/goffi?style=flat-square&label=)](https://github.com/go-webgpu/goffi/issues) |
| **[born](https://github.com/born-ml/born)** | born-ml | Pure Go ML framework (97%+ MNIST) | [![](https://img.shields.io/github/stars/born-ml/born?style=flat-square&label=)](https://github.com/born-ml/born) | [![](https://img.shields.io/github/issues/born-ml/born?style=flat-square&label=)](https://github.com/born-ml/born/issues) |

---

## Roadmap

### Foundation ✅
- [x] Zero-CGO WebGPU bindings (go-webgpu/webgpu)
- [x] Pure Go FFI (go-webgpu/goffi)

### Phase 1 — Graphics ✅
- [x] Graphics framework (gogpu/gogpu) — Triangle, Textures, Dual Backend
- [x] Shader compiler (gogpu/naga) — **WGSL → SPIR-V/MSL + compute shaders (~21K LOC)**

### Phase 2 — Pure Go WebGPU ✅
- [x] WebGPU types package (gogpu/wgpu/types)
- [x] Core validation & state (gogpu/wgpu/core)
- [x] HAL abstraction layer (gogpu/wgpu/hal)
- [x] OpenGL ES backend (gogpu/wgpu/hal/gles) — ~7.5K LOC, Windows + Linux
- [x] **Vulkan backend (gogpu/wgpu/hal/vulkan) — ~27K LOC, cross-platform!**
- [x] **Software backend (gogpu/wgpu/hal/software) — ~10K LOC, full rasterizer!**
- [x] **Metal backend (gogpu/wgpu/hal/metal) — ~2.5K LOC, macOS/iOS!**

### Phase 3 — 2D Graphics ✅
- [x] 2D graphics library (gogpu/gg) — **v0.15.0 with GPU compute shaders!**
- [x] Text rendering (v0.2.0) — FontSource/Face, MultiFace fallback
- [x] Images, Clipping, Compositing (v0.3.0) — DrawImage, Clip API, Porter-Duff
- [x] Layer API, Color Pipeline (v0.4.0) — PushLayer/PopLayer, HSL blend modes
- [x] SIMD Optimization (v0.5.0) — Fast div255, sRGB LUTs, batch blending (260x faster)
- [x] **Parallel Rendering (v0.6.0) — TileGrid, WorkerPool, lock-free DirtyRegion!**
- [x] **Scene Graph (v0.7.0) — Retained mode, 13 shapes, filters, layer cache!**
- [x] **Backend Abstraction (v0.8.0) — RenderBackend interface, registry!**
- [x] **GPU Backend (v0.9.0) — Sparse Strips, WGSL shaders, 29 blend modes on GPU!**
- [x] **GPU Text Pipeline (v0.10.0) — Shaper, Layout, Bidi, 25+ scripts!**
- [x] **GPU Text Rendering (v0.11.0) — MSDF atlas, emoji, subpixel positioning!**
- [x] **Rust-First API (v0.12.0) — Brush, Gradients, Stroke, Dash!**
- [x] **Go 1.25+ (v0.13.0) — Iterators, Generic Cache, Context!**
- [x] **Advanced Features (v0.14.0) — Alpha Masks, PathBuilder, io.Closer!**
- [x] **GPU Compute Shaders (v0.15.0) — vello-style flatten/coarse/fine pipeline!**

### Phase 3.5 — Platform Expansion ✅
- [x] **Linux Wayland (v0.4.0) — Pure Go implementation, 5,700 LOC!**
- [x] **Linux X11 (v0.6.0) — Pure Go wire protocol, ~5K LOC!**
- [x] **macOS Cocoa (v0.5.0) — Pure Go via goffi, ~950 LOC!**
- [x] **Metal backend (wgpu v0.7.0) — WGSL→MSL compilation, render pipeline!**
- [x] **GLSL shader output (naga v0.6.0) — WGSL → OpenGL 3.3+/ES 3.0+!**

### Phase 4 — GUI
- [ ] Widget toolkit (gogpu/ui)
- [ ] Layouts, styling, themes

---

## Contributing

We welcome contributions! See individual repository CONTRIBUTING.md files.

**Areas where we need help:**
- Pure Go GPU backends (DX12)
- WebGPU examples and tutorials
- Documentation
- GUI widget toolkit (gogpu/ui)

---

## License

All projects are licensed under the **MIT License**.

---

<p align="center">
  <sub>Building the GPU computing ecosystem Go deserves</sub><br>
  <a href="https://github.com/gogpu">github.com/gogpu</a>
</p>
