# G2B OpenCrab GitHub evidence pack

Validated OpenCrab GitHub-ingest pack for G2B public procurement row-level evidence.

## Current validated shape

- Repo URL: https://github.com/victorhan1981-dotcom/opencrab-g2b-packs
- Branch: main
- OpenCrab ingest path: `.`
- Evidence shard format: flat root JSON, 50 rows per file
- Evidence shards: 201 files, `g2b_evidence_50row_shard_001.json` ... `g2b_evidence_50row_shard_201.json`
- Evidence rows: 10,001
- Final shard: `g2b_evidence_50row_shard_201.json` contains the policy/9-space row at source_line 10001
- Exact probe markers are intentionally stored only inside shard JSON bodies, not in README/MANIFEST.

## OpenCrab validation probes

Use `opencrab_search_documents(source_type="github", scan_limit=20000)` for row evidence checks.

Known-good probes:

1. `R26BK01320155 bidNtceNo ntceNticeDt getBidPblancListInfoThngPurchsObjPrdct 전동식와이어로프호이스트 uprc=208753600`
   - Expected source: `g2b_evidence_50row_shard_069.json`

2. `R26BK01362809 bidPrceCalclAOpenDt mrfnHealthInsrprm npnInsrprm getBidPblancListBidPrceCalclAInfo`
   - Expected source: `g2b_evidence_50row_shard_001.json`

3. `g2b_evidence_50row_shard_201 10001 OPENCRAB_JSON_50_SHARD_201`
   - Expected source: `g2b_evidence_50row_shard_201.json`

## Search indexes

The `indexes/` directory contains small discovery indexes. These are not the canonical evidence; they point back to shard files and source lines.

- `INDEX_institutions.json`: institution/requesting-organization names and aliases
- `INDEX_suppliers.json`: supplier/vendor/company names where present
- `INDEX_products.json`: product/classification/spec names
- `INDEX_bid_notice_numbers.json`: bid notice number lookup
- `INDEX_amounts_dates.json`: high amount/date probes for analytical starting points
- `INDEX_operations.json`: service/operation/field distribution
- `INDEX_institution_aliases_seed.json`: seed aliases for future targeted collection, including KOSPO/한국남부발전

## Structured analysis export

The `analysis_exports/` directory is for local structured analysis, not canonical OpenCrab evidence.

- `g2b_rows_selected.csv.gz`: selected normalized columns for spreadsheet/Python/R analysis
- `g2b_rows_selected.sqlite`: SQLite table `rows` with indexes on bid notice, institution, product, and operation

Example local query:

```bash
sqlite3 analysis_exports/g2b_rows_selected.sqlite "select bidNtceNo,dminsttNm,dtilPrdctClsfcNoNm,uprc,shard_file from rows where dminsttNm like '%평택시%' limit 10;"
```

## Institution reports

For institution-level reporting:

1. Search exact official name.
2. Search aliases from `indexes/INDEX_institution_aliases_seed.json` and generated aliases in `INDEX_institutions.json`.
3. Verify direct row evidence in `g2b_evidence_50row_shard_*.json` or OpenCrab search results.
4. If direct evidence is absent, do targeted API/cache collection first; do not write a report from broad substring false positives.

한국남부발전/KOSPO direct rows were not present in this 10,001-row sample as of the validation run, so a KOSPO report requires targeted collection.

## Ontology quality review

See `ONTOLOGY_QUALITY_CRITERIA.md` for review criteria, validation probes, provenance checks, and suggested future OpenCrab quality tools.
