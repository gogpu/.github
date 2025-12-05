# GoGPU

**Pure Go GPU Computing Ecosystem**

> GPU power, Go simplicity. Zero CGO.

---

## 🎯 Vision

Build the most ergonomic GPU computing ecosystem for Go — from graphics to machine learning — with zero CGO dependencies.

## 📦 Projects

| Repository | Description | Status |
|------------|-------------|--------|
| **[gogpu](https://github.com/gogpu/gogpu)** | Graphics framework for Go | 🚧 Active |
| **[naga](https://github.com/gogpu/naga)** | Pure Go shader compiler (WGSL → SPIR-V) | 🚧 Active |
| **[gg](https://github.com/gogpu/gg)** | Simple 2D graphics library | 📋 Planned |
| **[wgpu](https://github.com/gogpu/wgpu)** | Pure Go WebGPU implementation | 🔮 Future |

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    Your Application                         │
├─────────────────────────────────────────────────────────────┤
│              gogpu/gogpu (Graphics Framework)               │
├─────────────────────────────────────────────────────────────┤
│   go-webgpu/webgpu (FFI)  ───▶  gogpu/wgpu (Pure Go)       │
├─────────────────────────────────────────────────────────────┤
│              Vulkan │ Metal │ DX12 │ OpenGL                 │
└─────────────────────────────────────────────────────────────┘
```

## ✨ Key Features

- **Zero CGO** — No C compiler required, simple cross-compilation
- **WebGPU API** — Modern, portable GPU abstraction
- **Pure Go** — Gradually replacing FFI with native Go implementation
- **Production Ready** — Powers [born-ml](https://github.com/born-ml/born) ML framework

## 🔗 Related Projects

- [go-webgpu/webgpu](https://github.com/go-webgpu/webgpu) — Zero-CGO WebGPU bindings
- [go-webgpu/goffi](https://github.com/go-webgpu/goffi) — Pure Go FFI library
- [born-ml/born](https://github.com/born-ml/born) — Pure Go ML framework

## 📖 Documentation

- [Getting Started](https://github.com/gogpu/gogpu#getting-started)
- [Examples](https://github.com/gogpu/gogpu/tree/main/examples)
- [Architecture](https://github.com/gogpu/gogpu/blob/main/docs/ARCHITECTURE.md)

## 🤝 Contributing

We welcome contributions! See [CONTRIBUTING.md](https://github.com/gogpu/gogpu/blob/main/CONTRIBUTING.md) for guidelines.

## 📄 License

All projects are licensed under the MIT License.

---

<p align="center">
  <i>Building the future of GPU computing in Go</i>
</p>
