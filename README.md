# Decentralized Cloud Storage

A blockchain-backed prototype for decentralized cloud storage — Solidity smart
contracts that share encrypted file references with user-level access control,
deployed with Hardhat on an Ethereum-compatible local chain.

[![GitHub stars](https://img.shields.io/github/stars/5h4d0wn1k/Decentralized-cloud-storage)](#)
[![Last commit](https://img.shields.io/github/last-commit/5h4d0wn1k/Decentralized-cloud-storage)](#)

## Why this project

Cloud storage trusts a single provider with your files; blockchain technology
offers an alternative where file references, access control, and integrity
records live on a tamper-resistant ledger. "Decentralized Secure Cloud Storage
using Blockchain Technology" explores splitting files, storing them in blocks
with AES-based file manipulation, and recording access grants on-chain using
Ethereum smart contracts. This repository contains the Solidity + Hardhat
side: a contract that associates storage references with addresses and lets
owners `allow`/`disallow` other wallets, plus a deployment script for a local
chain (`chainId 1337`). It is a research/education prototype for building
privacy- and integrity-oriented storage systems.

## Features

- **`Upload.sol`** — stores an array of file-reference strings per user address
- **`allow`** — grant read access to another wallet
- **`disallow`** — revoke previously granted access
- **`display`** — access-checked retrieval of stored references
  (`require(owner || granted)` on-chain)
- **`shareAccess`** — view the current access-grant list
- **Hardhat tooling** — `chainId 1337` local network, deploy script, artifacts
  routed to `client/src/artifacts`

## Quickstart

Prerequisites: Node 16+, npm, Hardhat 2.x.

```bash
npm install
npx hardhat node                                # start local blockchain
npx hardhat run --network localhost scripts/deploy.js   # deploy Upload.sol
```

> Note: the original project report references a React/web3 client, but the
> client source is not tracked in this repository — only the contract and
> deployment tooling. Contract artifacts are configured to write into
> `client/src/artifacts` (see `hardhat.config.js`).

## Project structure

- `contracts/Upload.sol` — the storage/access-control contract
- `scripts/deploy.js` — Hardhat deployment script
- `hardhat.config.js` — Solidity 0.8.9, local network `chainId: 1337`

## License

No LICENSE file is currently published in this repository. `Upload.sol` carries
an SPDX `GPL-3.0` identifier.