# OpenCrab G2B Packs

Public-source OpenCrab Cloud Pack upload artifacts for G2B / 나라장터 public procurement ontology experiments.

## Current artifact

- `artifacts/g2b-public-procurement-9space-25mb-v1.zip`
- Cloud Pack format: `opencrab-cloud-pack-v1`
- Spaces: subject/주체, resource/리소스, evidence/증거, concept/개념, claim/주장, community/커뮤니티, result/결과, lever/레버, policy/정책
- Nodes: 1050
- Edges: 2132
- Chunks/evidence: 10001
- ZIP size: about 25 MB
- Max ZIP entry: `cloud/chunks.jsonl`, about 13.8 MB

## Security note

This pack is generated from official public OpenAPI response fields for private ontology exploration. API keys, ServiceKey values, tokens, passwords, cookies, sessions, and OpenCrab `ocm_...` endpoint tokens were excluded and scanned before publishing.

## Validation

See `validation_report.md` and `build_summary.json`.


## 1500-node GitHub ingest artifact

- `artifacts/g2b-public-procurement-9space-1500n-25mb-v1.zip`
- Cloud Pack format: `opencrab-cloud-pack-v1`
- Nodes: 1500
- Edges: 3408
- Chunks/evidence: 10001
- ZIP size: about 25.5 MB
- Max ZIP entry: `cloud/chunks.jsonl`, about 13.9 MB
- Intended path: GitHub Release asset / URL ingest, since browser upload worked less reliably than server-side fetch.
