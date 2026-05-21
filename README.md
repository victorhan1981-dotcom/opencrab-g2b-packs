# G2B OpenCrab GitHub ingest 50-row JSON shard test

Clean flat-root experiment for OpenCrab GitHub ingest.

- Format: JSON object files at repository root
- Shard size: 50 evidence rows per file, except the final small shard
- Total rows: 10001
- Total shard files: 201
- Exact probe markers are intentionally stored only inside shard JSON files, not in this README.

OpenCrab input:

1. repo URL: https://github.com/victorhan1981-dotcom/opencrab-g2b-packs
2. branch: main
3. path: .
