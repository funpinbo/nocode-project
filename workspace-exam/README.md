# workspace-exam — 완성된 AI-DLC 예시

이 폴더는 AI-DLC 로 **AI-DLC Monitor**(`monitor/`)를 만든 실제 결과물을 그대로 보관한 **읽기 전용 예시**입니다.
`/aidlc-init` 이 만드는 `workspace/` 와 같은 구조(`user/` → `project/` → `teams/` → `memory/`)이므로,
각 단계 산출물이 어떤 수준·형식으로 쓰이는지 참고하는 용도입니다.

| 폴더 | 볼 만한 것 |
|------|-----------|
| `user/` | 사용자가 쓴 문서 4종 (개요·기능 요구, 개발 표준, 아키텍처 철학, 데이터 정의) |
| `project/` | 요구 해석서(00), 비즈니스(10), 아키텍처(20)+ADR, 데이터 EDA(30), 팀 구성(40), 계약·보안·QA·UAT 문서 |
| `teams/` | 팀 charter 8개 |
| `memory/` | Plan → Tasks → Long-term → Short-term, `archive/` 의 STM 기록 |

## 주의
- **Hook 과 `aidlc.py` 는 이 폴더를 보지 않습니다.** 프레임워크는 항상 `workspace/` 만 읽고 씁니다. 그래서 이 폴더는 고쳐도 파이프라인에 영향이 없고, 고칠 필요도 없습니다.
- 문서 안의 `workspace/...` 경로는 예시가 만들어질 당시의 실제 경로입니다. 지금은 이 폴더(`workspace-exam/...`)에 있습니다.
- Monitor 의 계약 스키마와 OpenAPI 명세(`project/contracts/`)는 `monitor/` 의 테스트와 게이트(`monitor/tools/check.py`)가 이 폴더에서 읽습니다. 지우면 게이트가 실패합니다.
- 새 프로젝트를 시작하려면 `/aidlc-init` 을 실행하세요. 빈 `workspace/` 가 템플릿으로 만들어집니다.
