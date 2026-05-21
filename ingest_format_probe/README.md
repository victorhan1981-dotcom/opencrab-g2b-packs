# OpenCrab ingest format probe: JSON vs JSONL

This folder tests whether OpenCrab GitHub ingest indexes small `.json` files but skips `.jsonl` files.

Files:

- `sentinel_row_json_probe.json` — small JSON object containing one public G2B sentinel row.
- `sentinel_row_jsonl_probe.jsonl` — one-line JSONL file containing the same public G2B sentinel row.

Recommended OpenCrab GitHub ingest input:

1. repo URL: `https://github.com/victorhan1981-dotcom/opencrab-g2b-packs`
2. branch: `main`
3. path: `ingest_format_probe`

Verification markers intentionally differ by file:

- JSON marker: `OPENCRAB_FORMAT_PROBE_JSON_SENTINEL_R26BK01320155`
- JSONL marker: `OPENCRAB_FORMAT_PROBE_JSONL_SENTINEL_R26BK01320155`

If the JSON marker is searchable but the JSONL marker is not, `.json` is preferred over `.jsonl` for row evidence on GitHub ingest.
