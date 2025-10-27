# Devnet Runbook

## Prereqs
- Node 20+, Git
- Solana CLI configured on devnet
- Pinata JWT

## Env
- `ANCHOR_PROVIDER_URL=https://api.devnet.solana.com`
- `ANCHOR_WALLET=~/.config/solana/<your-keypair>.json`
- `PINATA_JWT=<your-jwt>`

## Flow
1) Start ingest → batches of 50 land in `wakama-oracle-ingest/batches/`.
2) Run publisher → IPFS pin + Solana Memo tx + CSV manifest in `wakama-oracle-publisher/runs/`.
3) Confirm tx on devnet explorer and fetch CID via gateway.

**Signature:** CREATED BY WAKAMA.farm & Supported by Solana foundation
