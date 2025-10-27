# Short Spec v0.1

## Measurement
{
  "zone_id": "string",
  "device_id": "string",
  "sensor_type": "soil|temp|hum",
  "ts": "ISO-8601 UTC",
  "value": number,
  "unit": "%|°C|raw"
}

## Batch
{
  "batch_id": "uuid",
  "ts_min": "ISO-8601",
  "ts_max": "ISO-8601",
  "count": 50,
  "measures": [Measurement...]
}

- Hash = SHA-256 of the batch JSON file bytes.
- One IPFS CID per batch.
- Memo payload: `{ cid, sha256, count, ts_min, ts_max }`.

**Signature:** CREATED BY WAKAMA.farm & Supported by Solana foundation
