# Validation Report

- pack_id: g2b-public-procurement-9space-25mb-v1
- nodes: 1050
- edges: 2132
- documents: 659
- chunks: 10001
- spaces: {'concept': 357, 'resource': 230, 'claim': 84, 'evidence': 329, 'policy': 9, 'subject': 8, 'community': 9, 'result': 12, 'lever': 12}
- node target: approximately 1000
- ordinary file limit: 30MB
- Neo4j: passive; Cypher kept in 03_graph/neo4j_cypher_bundle.json, no .cypher file in ZIP.

## Structural validator result

PASS. validate_pack_zip.py passed all checks. ZIP integrity testzip returned null. Secret-pattern scan for ServiceKey/serviceKey/API key/password/cookie/session/ocm_ tokens returned 0 matches. ZIP is stored without compression to keep the upload artifact close to the requested 25MB size while each ordinary file remains under 30MB.
