# G2B OpenCrab ontology quality criteria

This checklist is for reviewing the quality of the `g2b_r1` GitHub-ingested OpenCrab evidence pack.

## 1. Ingest completeness

- Expected shard files: 201.
- Expected row count: 10,001.
- Expected final shard: `g2b_evidence_50row_shard_201.json`, `items_in_shard=1`, `item_start_1based=10001`.
- Verify with local JSON validation and `opencrab_list_sources(source_type="github")`.

## 2. Evidence retrievability

- Exact bid notice probes must return the expected shard with score near 1.
- Korean product/institution/value probes must retrieve row text, not just README/MANIFEST.
- Marker-only probes are insufficient; combine marker or bid number with row-specific fields.

## 3. Provenance quality

Each row should preserve `source_line`, `service`, `operation`, `source_file`/`source_path`, `hash`, evidence `text`, and shard source URL after GitHub ingest.

## 4. Search precision and recall

- Precision: top result for a unique row query should be the correct shard/row.
- Recall: common entity searches should be helped by `indexes/INDEX_*.json`.
- Broad substring matches must be manually filtered for institution reports.

## 5. Ontology shape / 9-space coverage

Review whether evidence supports the OpenCrab 9 spaces: subject, resource, evidence, concept, claim, community, result, lever, and policy.

## 6. Data hygiene

- No API keys, MCP URLs, passwords, or private credentials.
- Public OpenAPI response fields are allowed in private packs.
- Empty/`-`/null values should remain in raw evidence, while derived exports may normalize them.

## 7. Tooling recommendations

Current tools: `opencrab_status`, `opencrab_search_packs`, `opencrab_list_sources`, `opencrab_search_documents`, and local `sqlite3` export.

Future OpenCrab quality tools to request/build:

- pack-scoped `opencrab_search_documents(package_id=...)`.
- cursor-based `opencrab_list_documents` and `opencrab_list_chunks`.
- pack-level coverage report: documents, chunks, nodes, edges, sources, failed files.
- retrieval benchmark runner: expected query -> expected source/fields.
- ontology lint: orphan nodes, low-degree concepts, duplicate aliases, field explosion, relation density.
- provenance audit: every derived claim points back to evidence chunk and source URL.
