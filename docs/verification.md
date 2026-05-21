# Verification plan

After OpenCrab GitHub ingest of `evidence_json_500`, verify by searching terms that should resolve to shard JSON sources.

Important: success means the source path is `evidence_json_500/g2b_evidence_500row_shard_NNN.json`. README or index hits alone are not enough.

Recommended semantic searches:

- `R26BK01320155 bidNtceNo ntceNticeDt getBidPblancListInfoThngPurchsObjPrdct`
- `전동식와이어로프호이스트 경기도 평택시 상하수도사업소 uprc 208753600`
- `getPrvtScsbidListSttus 20230214128 아워홈 더케이호텔서울 여주점 식자재 282891242`
- `getScsbidListSttusFrgcpt 20210514076 이카코리아 자동열량분석시스템 서울특별시 보건환경연구원`
- `getPrdctClsfcNoUnit6Info 211017 수확용농업기계 Agricultural machinery for harvesting`

There are also unique probe marker strings embedded only inside selected shard JSON files; use the runtime/test notes rather than this repo document when checking them, so marker searches do not match documentation.
