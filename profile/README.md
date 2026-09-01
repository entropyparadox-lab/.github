<div align="center">

# ⚡ EntropyParadox Lab

**Engineering Zero-Overhead Systems, Deterministic AI Agent Infrastructure & Native Zig v0.16.0+ Primitives**

**[ English ](README.md)** • **[ 한국어 ](README.ko.md)** • **[ 日本語 ](README.ja.md)** • **[ 简体中文 ](README.zh.md)**

<p align="center">
  <img src="https://img.shields.io/badge/Language-Zig_v0.16.0+-f7a41d.svg?style=flat-square&logo=zig&logoColor=white" alt="Zig 0.16" />
  <img src="https://img.shields.io/badge/Language-Rust_Edition_2024-000000.svg?style=flat-square&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/License-MIT%20%7C%20Apache--2.0-blue.svg?style=flat-square" alt="License" />
  <img src="https://img.shields.io/badge/Architecture-AOT%20%7C%20Zero--Alloc-success.svg?style=flat-square" alt="Zero-Alloc" />
</p>

</div>

---

## 🏛️ Mission & Engineering Philosophy

EntropyParadox Lab builds high-density, deterministic systems and foundational developer tools. We eliminate abstraction tax and non-deterministic behavior across two core disciplines:

1. **Deterministic Agent Runtime**: Building sub-millisecond execution harnesses, sandbox runtimes, and self-healing action caches for autonomous coding agents.
2. **Pure Zig (v0.16.0+) Ecosystem**: Crafting zero-allocation, compile-time verified primitives with zero external runtime dependencies.

```
┌──────────────────────────────────────────────────────────────────────────┐
│                         EntropyParadox Ecosystem                         │
├────────────────────────────────────┬─────────────────────────────────────┤
│     Deterministic AI Agents        │      Native Zig Systems Suite       │
├────────────────────────────────────┼─────────────────────────────────────┤
│ • web-reflex (Instant Web Cache)   │ • zig-doc-engine (FTS5 Docs)        │
│ • mos (Firecracker MicroVM PaaS)   │ • zmcp & zmcp-gateway (Native MCP)  │
│ • maniac-killer (Process Watchdog) │ • zcli, zserde, zenv (Core Libs)    │
│ • argus-audit (Host Activity Log)  │ • zlog, zfetch, zbench (Utilities)  │
└────────────────────────────────────┴─────────────────────────────────────┘
```

---

## 🚀 Key Open-Source Projects

### 1. 🤖 Autonomous AI Agent Infrastructure

* **[`web-reflex`](https://github.com/entropyparadox-lab/web-reflex)**: Deterministic, instant (<45ms), and self-healing action cache for AI web agents. Eliminates redundant LLM browser navigation loops.
* **[`mos`](https://github.com/entropyparadox-lab/mos)**: Lightweight, hyper-dense, scale-to-zero serverless PaaS built directly on Linux KVM and Firecracker MicroVMs.
* **[`maniac-killer`](https://github.com/entropyparadox-lab/maniac-killer)**: Process watchdog and remote executioner safeguarding macOS & Linux hosts from runaway agent loops.
* **[`argus-audit`](https://github.com/entropyparadox-lab/argus-audit)**: Zero-overhead host activity and developer audit engine written in pure Rust.

---

### 2. ⚡ Zig (v0.16.0+) Systems Suite

All Zig packages are strictly designed for **Zig v0.16.0+**, featuring zero heap allocation (`0-Alloc`), explicit allocator semantics, and zero external C dependencies.

* **[`zig-doc-engine`](https://github.com/entropyparadox-lab/zig-doc-engine)**: Ultra-lightweight (<550KB), blazing-fast offline documentation FTS5 indexing and retrieval engine. Guarantees 0-error code generation for LLMs.
* **[`zmcp`](https://github.com/entropyparadox-lab/zmcp)** & **[`zmcp-gateway`](https://github.com/entropyparadox-lab/zmcp-gateway)**: High-performance Model Context Protocol (MCP) server SDK, tool multiplexer, and caching gateway in pure Zig.
* **[`zcli`](https://github.com/entropyparadox-lab/zcli)**: Zero-allocation comptime declarative CLI, flag parser, and shell completion generator.
* **[`zserde`](https://github.com/entropyparadox-lab/zserde)**: Zero-allocation multi-format serialization and comptime schema validation toolkit.
* **[`zenv`](https://github.com/entropyparadox-lab/zenv)**: Zero-allocation `.env` parser and comptime typed environment injector.
* **[`zlog`](https://github.com/entropyparadox-lab/zlog)**: Zero-allocation structured logger with ANSI/NDJSON formatters and OpenTelemetry tracing.
* **[`zfetch`](https://github.com/entropyparadox-lab/zfetch)**: Ergonomic, type-safe HTTP client wrapping Zig's standard `std.http.Client`.
* **[`zbench`](https://github.com/entropyparadox-lab/zbench)**: Statistical microbenchmarking and memory profiling toolkit.

---

### 3. 📖 Documentation & Guides

* **[`zig-guide-kr`](https://github.com/entropyparadox-lab/zig-guide-kr)** ([🌐 Live Site](https://entropyparadox-lab.github.io/zig-guide-kr/)): Complete Korean translation of the official Zig v0.16.0 reference and Rails-style practical systems guide.

---

## 🛡️ Governance & Quality Standards

* **Adversarial Verification Gate**: All architectures, roadmaps, and PRs pass 4-Gate red-team stress testing before release.
* **Immutable Tagging**: Semantic Versioning (SemVer 2.0) with immutable release tags (`vX.Y.Z`).
* **Branch Protection**: Direct pushes to `main` are strictly blocked via pre-push hooks and GitHub branch protection.
* **Dual Licensing**: Open-source libraries are licensed under either **MIT** or **Apache-2.0**.

---

<div align="center">
  <sub>Maintained with precision by EntropyParadox Lab.</sub>
</div>
