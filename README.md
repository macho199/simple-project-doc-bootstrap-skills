# simple-project-doc-bootstrap-skills

AI와 함께 프로젝트를 진행할 때 기준 문서를 빠르게 세우고 유지하도록 돕는 스킬 저장소입니다.

이 저장소는 현재 두 가지 흐름을 제공합니다.

- `simple-project-doc-bootstrap`: 프로젝트 기준 문서를 최소 구조로 정리하는 스킬
- `spec-driven-doc-bootstrap`: 소프트웨어 개발용 spec/plan/task/contract/testing 문서를 정리하는 스킬

## 무엇을 제공하나

### 1. simple-project-doc-bootstrap

프로젝트 문서를 최소 구조로 유지하도록 돕습니다.

기본 관리 대상:
- `PROJECT.md`: 목표, 범위, 제약사항
- `STATUS.md`: 현재 상태와 다음 작업
- `ARCHITECTURE.md`: 현재 확정된 구조와 설계 결정
- `AGENTS.md` 또는 `CLAUDE.md`: 작업 규칙 문서

이 스킬은 문서를 많이 만드는 대신,
AI와 사람이 다음 작업을 바로 이어갈 수 있을 만큼만 정확하고 최신인 문서를 유지하는 데 초점을 둡니다.

### 2. spec-driven-doc-bootstrap

프로그램 개발에서 비사소한 변경을 spec 중심으로 관리하도록 돕습니다.

기본 관리 대상:
- `SPECS.md`: 관리 중인 spec 인덱스
- `specs/<id-slug>/SPEC.md`: 문제 정의와 요구사항
- `specs/<id-slug>/PLAN.md`: 구현 접근과 영향 범위
- `specs/<id-slug>/TASKS.md`: 실행 체크리스트와 검증 상태

조건부 확장 문서:
- `DECISIONS.md`: 장기 유지할 기술 결정
- `CONTRACTS.md`: API, 이벤트, 파일 포맷, CLI 등 경계 계약
- `TESTING.md`: 프로젝트 공통 검증 기준
- `OPERATIONS.md`: 서비스 운영 절차
- `fixtures/contracts/`: 계약 예시 데이터

## 어떤 때 어떤 스킬을 쓰나

- 프로젝트의 기준 문서가 없거나 너무 흩어져 있으면 `simple-project-doc-bootstrap`
- 소프트웨어 기능 개발을 spec 기준으로 운영하고 싶으면 `spec-driven-doc-bootstrap`
- 둘 다 필요하면 먼저 `simple-project-doc-bootstrap`로 기준 문서를 정리한 뒤, 기능 단위 작업부터 `spec-driven-doc-bootstrap`를 함께 사용하면 됩니다.

## 저장소 구조

```text
.
├── README.md
└── skills/
    ├── simple-project-doc-bootstrap/
    │   ├── README.md
    │   ├── SKILL.md
    │   ├── examples/
    │   └── templates/
    └── spec-driven-doc-bootstrap/
        ├── README.md
        ├── SKILL.md
        ├── agents/
        ├── examples/
        └── templates/
```

## 시작 방법

필요한 흐름에 맞춰 아래처럼 요청하면 됩니다.

- `simple-project-doc-bootstrap 스킬로 이 저장소의 최소 기준 문서를 정리해줘`
- `spec-driven-doc-bootstrap 스킬로 이 기능의 spec 문서 세트를 만들어줘`
