# G2B evidence JSON 500-row shards

This folder is the current clean OpenCrab GitHub-ingest test target.

- Format: JSON object per shard
- Rows per shard: 500, except the final shard
- Total evidence items: 10001
- Shard count: 21
- Source: generated from the previous validated `cloud/chunks.jsonl` evidence payload
- Credential-bearing values are excluded.

OpenCrab GitHub ingest input:

1. repo URL: `https://github.com/victorhan1981-dotcom/opencrab-g2b-packs`
2. branch: `main`
3. path: `evidence_json_500`

Verification should inspect returned source paths. A successful test must return one of the shard JSON files, not only this README.
