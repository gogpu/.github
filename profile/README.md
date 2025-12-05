<p align="center">
  <img src="https://raw.githubusercontent.com/gogpu/.github/main/assets/logo.png" alt="GoGPU Logo" width="200" />
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

## 🎯 Mission

Build the most ergonomic GPU computing ecosystem for Go — from graphics to machine learning — with **zero CGO dependencies**.

## 📦 Projects

| Repository | Description | Status |
|:-----------|:------------|:------:|
| **[gogpu](https://github.com/gogpu/gogpu)** | Graphics framework for Go | 🚧 Active |
| **[naga](https://github.com/gogpu/naga)** | Pure Go shader compiler (WGSL → SPIR-V) | 🚧 Active |
| **[gg](https://github.com/gogpu/gg)** | Simple 2D graphics library | 📋 Planned |
| **[wgpu](https://github.com/gogpu/wgpu)** | Pure Go WebGPU implementation | 🔮 Future |

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    Your Application                         │
├─────────────────────────────────────────────────────────────┤
│  born-ml/born        gogpu/gogpu         gogpu/gg          │
│  (ML Framework)    (Graphics)          (2D Graphics)       │
├─────────────────────────────────────────────────────────────┤
│              WebGPU API (gogpu ecosystem)                   │
├─────────────────────────────────────────────────────────────┤
│   go-webgpu/webgpu    ────────▶    gogpu/wgpu              │
│   (FFI, works now)                 (Pure Go, future)        │
├─────────────────────────────────────────────────────────────┤
│              Vulkan  │  Metal  │  DX12  │  OpenGL           │
└─────────────────────────────────────────────────────────────┘
```

## ✨ Key Features

| Feature | Description |
|:--------|:------------|
| **Zero CGO** | No C compiler required, simple cross-compilation |
| **WebGPU API** | Modern, portable GPU abstraction |
| **Pure Go Goal** | Gradually replacing FFI with native implementation |
| **Production Ready** | Powers [born-ml](https://github.com/born-ml/born) ML framework |

## 🚀 Quick Start

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

## 🔗 Ecosystem

| Project | Organization | Description |
|:--------|:-------------|:------------|
| [webgpu](https://github.com/go-webgpu/webgpu) | go-webgpu | Zero-CGO WebGPU bindings |
| [goffi](https://github.com/go-webgpu/goffi) | go-webgpu | Pure Go FFI library |
| [born](https://github.com/born-ml/born) | born-ml | Pure Go ML framework |

## 📊 Why GoGPU?

| Problem | GoGPU Solution |
|:--------|:---------------|
| CGO complexity | Zero CGO — just `go build` |
| Cross-compilation pain | Works with `GOOS`/`GOARCH` |
| C compiler requirement | Pure Go, no toolchain needed |
| WebGPU in Go | First-class support |

## 🗺️ Roadmap

- [x] Zero-CGO WebGPU bindings (go-webgpu)
- [x] Pure Go FFI (goffi)
- [ ] Graphics framework (gogpu) — **in progress**
- [ ] Shader compiler (naga) — **in progress**
- [ ] 2D graphics (gg)
- [ ] Pure Go WebGPU (wgpu)

## 🤝 Contributing

We welcome contributions! See individual repository CONTRIBUTING.md files for guidelines.

**Areas where we need help:**
- WGSL parser implementation
- WebGPU examples
- Documentation and tutorials
- Testing on different GPUs

## 📄 License

All projects are licensed under the **MIT License**.

---

<p align="center">
  <sub>Building the future of GPU computing in Go</sub><br>
  <a href="https://github.com/gogpu">github.com/gogpu</a>
</p>
