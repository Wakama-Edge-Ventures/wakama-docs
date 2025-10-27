# Short Spec v0.1

## Measurement JSON
{
  "zone_id":"string",
  "device_id":"string",
  "sensor_type":"soil|temp|hum",
  "ts":"ISO-8601 UTC",
  "value":number,
  "unit":"%|°C|raw"
}

## Batch JSON
{
  "batch_id":"uuid",
  "ts_min":"ISO-8601",
  "ts_max":"ISO-8601",
  "count":50,
  "measures":[Measurement...]
}

- Batch hash = SHA-256 of the JSON file bytes.
- One IPFS CID per batch.
- On-chain memo payload: `{ cid, sha256, count, ts_min, ts_max }`.

**Signature:** CREATED BY WAKAMA.farm & Supported by Solana foundation
