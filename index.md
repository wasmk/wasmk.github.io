---
layout: index
---

## What is Wasm/k?

**Wasm/k** (WebAssembly continuations) is an extension of WebAssembly with additional primitive instructions that offer
support for full first-class continuations, very similar to `call/cc` in Scheme / Racket. These instructions allow
for significantly more efficient implementations of high-level language features such as green threads.
**Wasm/k** consists of three parts:

1. A fork of **wasmtime** (a JIT implementation of WebAssembly) which implements the additional instructions of **Wasm/k**.
2. **C/k**, a wrapper around [Emscripten](https://emscripten.org) which exposes first-class continuations to C, and compiles them to **Wasm/k**.
3. Our paper, which includes the full formal definition of **Wasm/k** and proofs of safety.

## Wasmtime
TODO

## emcc/k
TODO
