# G2B Evidence JSON full-array probe

This folder tests whether OpenCrab GitHub ingest can index one large `.json` array/object better than `.jsonl`.

File:

- `g2b_evidence_full_10001.json`

Metadata:

- format: `g2b_evidence_json_array_v1`
- evidence_items_total: `10001`
- source_payload: `cloud/chunks.jsonl`
- unique_probe_marker: `OPENCRAB_FORMAT_PROBE_FULL_JSON_ARRAY_R26BK01320155`
- sentinel_bidNtceNo: `R26BK01320155`
- sha256: `c0658259f9d0ee48828532ff292377031e3953f744e8302df969cb60863e6b67`

Recommended OpenCrab GitHub ingest input:

1. repo URL: `https://github.com/victorhan1981-dotcom/opencrab-g2b-packs`
2. branch: `main`
3. path: `evidence_json/g2b_evidence_full_10001.json`

Fallback path if file-level ingest fails:

- `evidence_json`

Verification terms:

- `OPENCRAB_FORMAT_PROBE_FULL_JSON_ARRAY_R26BK01320155`
- `R26BK01320155`
- `bidNtceNo ntceNticeDt getBidPblancListInfoThngPurchsObjPrdct`
- `전동식와이어로프호이스트 경기도 평택시 상하수도사업소`
- `uprc=208753600`
