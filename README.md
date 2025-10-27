# Wakama Docs
Specs and runbooks for the Wakama oracle stack.

## Quickstart
- Ingest: POST `/ingest` with one measurement JSON. Server batches 50 into `./batches/*.json`.
- Publisher: pins each batch to IPFS (Pinata), posts a Solana Memo on devnet with `{cid, sha256, count, ts_min, ts_max}`, and writes a daily CSV manifest in `runs/`.
- Verify: confirm the transaction on devnet and resolve the CID via your preferred IPFS gateway.

**Signature:** CREATED BY WAKAMA.farm & Supported by Solana foundation
