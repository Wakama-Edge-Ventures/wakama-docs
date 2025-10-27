# Short Spec v0.1
Batch = 50 measurements.

Measurement JSON
{ "zone_id":"string","device_id":"string","sensor_type":"soil|temp|hum",
  "ts":"ISO-8601 UTC","value":number,"unit":"%|°C|raw" }

Batch JSON
{ "batch_id":"uuid","ts_min":"ISO","ts_max":"ISO","count":50,"measures":[...] }

Batch hash = SHA-256 of the JSON file. One IPFS CID per batch.
On-chain event: { cid, sha256, count, ts_min, ts_max }.
