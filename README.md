# simple-project-doc-bootstrap

프로젝트 문서를 최소 구조로 유지하도록 돕는 통합 스킬 저장소입니다.

핵심 목표는 문서를 많이 만드는 것이 아니라, AI와 사람이 다음 작업을 바로 이어갈 수 있을 만큼만 정확하고 최신인 문서를 유지하는 것입니다. 실행 시 먼저 `Codex` 기준으로 운영할지 `Claude Code` 기준으로 운영할지 확인한 뒤 그에 맞는 규칙 문서를 선택합니다.

## 무엇을 제공하나

이 저장소에는 다음 구성이 포함되어 있습니다.

- `skills/simple-project-doc-bootstrap/SKILL.md`: 스킬의 동작 원칙과 실행 절차
- `skills/simple-project-doc-bootstrap/README.md`: 스킬 소개와 사용 예시
- `skills/simple-project-doc-bootstrap/templates/`: 기본 문서 템플릿
- `skills/simple-project-doc-bootstrap/examples/`: 신규/기존 프로젝트 예시

## 이 스킬이 다루는 기본 문서

스킬은 아래 3개 문서를 공통 기준 문서로 유지합니다.

- `PROJECT.md`: 목표, 범위, 제약사항
- `STATUS.md`: 현재 상태와 다음 작업
- `ARCHITECTURE.md`: 현재 확정된 구조와 설계 결정

그리고 실행 시 선택된 워크플로우에 따라 아래 둘 중 하나를 규칙 문서로 사용합니다.

- Codex면 `AGENTS.md`
- Claude Code면 `CLAUDE.md`

## 핵심 철학

- 문서는 적을수록 좋다
- 오래된 정보는 보존보다 갱신을 우선한다
- 새 문서를 만들기 전에 기존 문서에 통합 가능한지 먼저 검토한다
- 긴 작업 로그보다 현재 상태를 빠르게 이해할 수 있는 문서를 선호한다
- 사용자의 최신 요구사항이 기존 문서보다 우선한다
- 의미 있는 작업이 끝난 뒤에는 관련 문서를 반드시 현행화한다

## 이런 프로젝트에 잘 맞는다

- AI와 여러 세션에 걸쳐 협업하는 개인 또는 소규모 프로젝트
- 시작은 했지만 기준 문서 체계가 없는 저장소
- 문서가 많아졌지만 어떤 파일이 기준인지 불분명한 프로젝트
- 맥락 손실 없이 다음 작업을 바로 이어가고 싶은 장기 개발 작업

## 동작 방식

1. 사용자가 이미 `Codex` 또는 `Claude Code`를 명시했다면 그대로 사용합니다.
2. 명시되지 않았다면 먼저 어떤 워크플로우로 운영할지 물어봅니다.
3. Codex면 `AGENTS.md`, Claude Code면 `CLAUDE.md`를 규칙 문서로 선택합니다.
4. 나머지 공통 문서 `PROJECT.md`, `STATUS.md`, `ARCHITECTURE.md`를 함께 정리합니다.

## 저장소 구조

```text
.
├── README.md
└── skills/
    └── simple-project-doc-bootstrap/
        ├── README.md
        ├── SKILL.md
        ├── examples/
        └── templates/
```

## 시작 방법

`simple-project-doc-bootstrap` 스킬을 사용해 달라고 요청하면 됩니다.
