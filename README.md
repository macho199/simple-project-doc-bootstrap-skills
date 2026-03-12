# create-skill-codex-project-doc-bootstrap

프로젝트 문서를 최소 구조로 유지하도록 돕는 스킬 2종을 담고 있는 저장소입니다.

- Codex용 `simple-project-codex-doc-bootstrap`
- Claude Code용 `simple-project-claude-doc-bootstrap`

이 프로젝트는 새 프로젝트를 시작할 때, 혹은 기존 문서가 뒤엉킨 저장소를 정리할 때 최소한의 기준 문서만 유지하도록 돕는 데 초점을 맞춥니다. 핵심 목표는 문서를 많이 만드는 것이 아니라, AI와 사람이 다음 작업을 바로 이어갈 수 있을 만큼만 정확하고 최신인 문서를 유지하는 것입니다.

## 무엇을 제공하나

이 저장소에는 다음 구성이 포함되어 있습니다.

- `skills/simple-project-codex-doc-bootstrap/`: Codex용 스킬
- `skills/simple-project-claude-doc-bootstrap/`: Claude Code용 스킬

각 스킬 폴더에는 아래 구성이 공통으로 들어 있습니다.

- `SKILL.md`: 스킬의 동작 원칙과 실행 절차
- `README.md`: 스킬 소개와 사용 예시
- `templates/`: 기본 문서 템플릿
- `examples/`: 신규/기존 프로젝트 예시

## 이 스킬이 다루는 기본 문서

두 스킬 모두 아래 4개 문서를 프로젝트의 최소 기준 문서로 유지하는 방향을 제안합니다.

- Codex 스킬: `AGENTS.md`, `PROJECT.md`, `STATUS.md`, `ARCHITECTURE.md`
- Claude Code 스킬: `CLAUDE.md`, `PROJECT.md`, `STATUS.md`, `ARCHITECTURE.md`

차이는 첫 번째 규칙 문서 이름뿐이며, 나머지 철학과 운영 방식은 거의 동일합니다.

## 핵심 철학

- 문서는 적을수록 좋다
- 오래된 정보는 보존보다 갱신을 우선한다
- 새 문서를 만들기 전에 기존 문서에 통합 가능한지 먼저 검토한다
- 긴 작업 로그보다 현재 상태를 빠르게 이해할 수 있는 문서를 선호한다
- 사용자의 최신 요구사항이 기존 문서보다 우선한다

## 이런 프로젝트에 잘 맞는다

- AI와 여러 세션에 걸쳐 협업하는 개인 또는 소규모 프로젝트
- 시작은 했지만 기준 문서 체계가 없는 저장소
- 문서가 많아졌지만 어떤 파일이 기준인지 불분명한 프로젝트
- 맥락 손실 없이 다음 작업을 바로 이어가고 싶은 장기 개발 작업

## 어떤 스킬을 쓰면 되나

- Codex 기반 워크플로우를 쓰면 `simple-project-codex-doc-bootstrap`
- Claude Code 기반 워크플로우를 쓰면 `simple-project-claude-doc-bootstrap`

기존 단일 스킬 `simple-project-doc-bootstrap`는 두 스킬로 분리되었습니다.

## 저장소 구조

```text
.
├── README.md
└── skills/
    ├── simple-project-codex-doc-bootstrap/
    │   ├── README.md
    │   ├── SKILL.md
    │   ├── examples/
    │   └── templates/
    └── simple-project-claude-doc-bootstrap/
        ├── README.md
        ├── SKILL.md
        ├── examples/
        └── templates/
```

## 시작 방법

Codex에서는 `simple-project-codex-doc-bootstrap` 스킬을, Claude Code에서는 `simple-project-claude-doc-bootstrap` 스킬을 사용해 달라고 요청하면 됩니다.

두 스킬 모두 저장소의 현재 상태를 먼저 파악한 뒤, 필요할 경우 최소 문서 세트를 만들거나 기존 문서를 정리하고, 작업 후에는 관련 문서를 현재 상태 기준으로 다시 맞춥니다.
