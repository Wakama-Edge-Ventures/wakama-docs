# Devnet Runbook

## Prerequisites
- Node.js 20+
- Solana CLI (devnet)
- Pinata JWT

## Environment
- ANCHOR_PROVIDER_URL = https://api.devnet.solana.com
- ANCHOR_WALLET = ~/.config/solana/<your-keypair>.json
- PINATA_JWT = <your-jwt>

## Flow
1) Start `wakama-oracle-ingest` → batches of 50 in `./batches/`.
2) Run `wakama-oracle-publisher` → IPFS pin + Solana Memo + CSV manifest in `runs/`.
3) Confirm the transaction on devnet. Open the CID via an IPFS gateway.

**Signature:** CREATED BY WAKAMA.farm & Supported by Solana foundation
