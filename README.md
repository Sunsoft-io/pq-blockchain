# pq-blockchain – Post-Quantum Rust Prototype (Dilithium + gRPC)

This repository contains a minimal post-quantum blockchain prototype:

- `pq-node` – gRPC server (node) verifying Dilithium signatures
- `pq-node-client` – Rust client creating Dilithium signatures and submitting a transaction

Cryptography is provided by [liboqs](https://github.com/open-quantum-safe/liboqs) and the Rust bindings `oqs`.

## Requirements

- Ubuntu 22.04 / 24.04 (or similar)
- Rust (rustup, stable)
- liboqs installed system-wide
- `protoc` (protobuf-compiler)

## Build

```bash
cargo build
