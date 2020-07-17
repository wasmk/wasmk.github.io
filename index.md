---
layout: index
---

## What is Wasm/k?

**Wasm/k** (WebAssembly continuations) is an extension of WebAssembly with additional primitive instructions that offer
support for full first-class continuations, very similar to `call/cc` in Scheme / Racket. These instructions allow
for significantly more efficient implementations of high-level language features such as green threads.
**Wasm/k** consists of three parts:

1. A fork of **Wasmtime**, a JIT implementation of WebAssembly, which implements the additional instructions of **Wasm/k**.
2. **C/k**, a wrapper around [Emscripten](https://emscripten.org) which exposes first-class continuations to C, and compiles them to **Wasm/k**.
3. [Our paper](FullVersion.pdf), which includes the full formal definition of **Wasm/k** and proofs of safety.

## Wasmtime

Wasmtime is a JIT for WebAssembly implemented in Rust. We extended Wasmtime in a fork to support Wasm/k.
Building our fork of Wasmtime also depends on our forks of a few other Rust WebAssembly toolchain libraries.
Please see the [instructions for building our fork of Wasmtime](https://github.com/donald-pinckney/WasmContinuations).

## C/k

C/k can be used to compile C/C++ which uses first class continuations
to Wasm/k code, which can then be run in the modified Wasmtime JIT.
C/k is implemented as a set of wrapper scripts around Emscripten / WASI-SDK.
Please see the [instructions for installing C/k](https://github.com/plasma-umass/emcc_control/).
