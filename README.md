# Wakama Docs
Specs and runbooks for the Wakama oracle stack.

## Quickstart
- Ingest: POST `/ingest` → batches of 50 JSON files.
- Publisher: IPFS pin (Pinata) + Solana Memo `{cid, sha256, count, ts_min, ts_max}` + daily CSV manifest.
- Verify: confirm the transaction on devnet and resolve the CID via an IPFS gateway.

**Signature:** CREATED BY WAKAMA.farm & Supported by Solana foundation
