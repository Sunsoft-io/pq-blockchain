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


# pq-blockchain

pq-blockchain is an experimental post-quantum blockchain prototype written in Rust.  
The project explores how modern post-quantum cryptography (PQC) can be integrated into a clean, minimal, and auditable blockchain-style architecture.

The core focus is on:

- Post-quantum digital signatures using **Dilithium**
- Post-quantum key exchange using **Kyber**
- A simple **gRPC-based node architecture**
- Clean separation between:
  - classical systems (e.g. Bitcoin, Taproot, Lightning, Taproot Assets)
  - and a native post-quantum transaction domain

This repository currently contains:

- `pq-node` – a minimal gRPC-based Rust node that verifies Dilithium-signed transactions  
- `pq-node-client` – a Rust client that generates Dilithium key pairs, signs transactions, and submits them to the node

Cryptography is provided by the Open Quantum Safe project via `liboqs` and its Rust bindings (`oqs`).

---

## Project Goals

- Explore **real-world integration of post-quantum cryptography** in distributed systems
- Keep the codebase:
  - minimal
  - auditable
  - dependency-light
- Avoid unnecessary complexity (KISS principle)
- Provide a foundation for:
  - post-quantum wallets
  - post-quantum validators
  - post-quantum asset layers
  - future interoperability with Bitcoin and Taproot-based systems

This project is primarily a **research and engineering prototype**.  
It is **not production-ready** and **not intended for real-world financial use at this stage**.

---

## Cryptographic Stack

- **Signatures:** Dilithium (ML-DSA)
- **Key Exchange:** Kyber (ML-KEM)
- **Transport:** gRPC over TCP (TLS/hybrid modes may be added later)
- **Language:** Rust

---

## Cross-Platform PQ Wallets

- Rust library Tauri
- Windows, MacOS, Linux, iPhone and Android
- Non-Custodial Wallet
- Private Keys can optionaly be stored on regular USB-Sticks (Desktops: Windows, MacOS and Linux)

---

## Design Philosophy 

- Security first
- Minimal trusted computing base
- Post-quantum by default
- No hybrid signature complexity in the base layer
- Clear separation between:
  - PQ-native logic
  - and classical blockchain infrastructure

---

## Disclaimer

This is an experimental research project intended for educational and technical exploration of post-quantum blockchain architectures.  
It does **not** constitute a financial product, investment offering, or payment system.
