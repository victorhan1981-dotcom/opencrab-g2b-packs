# G2B Public Procurement 9-Space 1500N 25MB Ontology Pack v1

G2B Public Procurement 9-Space 1500N 25MB Ontology Pack v1은 나라장터/G2B 공개 OpenAPI 캐시를 OpenCrab의 9개 space(주체, 리소스, 증거, 개념, 주장, 커뮤니티, 결과, 레버, 정책)로 재구성한 업로드용 Cloud Pack입니다. 공식 공공데이터 응답 필드는 선별된 문장 증거 chunk로 보존하고, API key/token/password/cookie/session 같은 비밀정보는 포함하지 않는 정책을 따릅니다. 약 1,500개 노드의 확장 compact graph와 약 25MB cloud chunk payload를 결합한 GitHub URL ingest용 버전이며, Web UI 직접 업로드보다 서버-side fetch 검증과 이후 서비스별 shard pack 확장에 적합합니다.

## 9 Spaces
- subject: 주체 / Subject — 행위하거나 책임지는 사람, 조직, 시스템, 역할, 이해관계자.
- resource: 리소스 / Resource — 문서, API, 데이터셋, 파일, URL, 원문처럼 참조되거나 사용되는 자료/자산.
- evidence: 증거 / Evidence — 주장과 판단을 뒷받침하는 원문 발췌, chunk, 관측값, 로그, 수치.
- concept: 개념 / Concept — 도메인 용어, 분류, 스키마, 속성, 절차명 등 이해를 위한 추상 단위.
- claim: 주장 / Claim — 검증 가능한 statement 또는 데이터/규칙/관계에 대한 명시적 단언.
- community: 커뮤니티 / Community — 사용자/기관/공급자/시장/프로젝트 같은 집단과 네트워크.
- result: 결과 / Result — 낙찰, 계약, 유찰, 변경, 분석 결과, 리포트처럼 과정 이후 생긴 산출/상태.
- lever: 레버 / Lever — 검색조건, 평가방식, 제한조건, 전략, 기능 등 결과를 바꾸는 개입 수단.
- policy: 정책 / Policy — 법령, 내부규정, 지침, 이용정책, 거버넌스 제약과 판단 기준.
