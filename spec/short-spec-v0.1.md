# Short Spec v0.1
Measurement: { zone_id, device_id, sensor_type, ts, value, unit }
Batch: { batch_id, ts_min, ts_max, count, measures[] }
Hash = SHA-256(file bytes). One IPFS CID per batch. Memo payload = { cid, sha256, count, ts_min, ts_max }.
