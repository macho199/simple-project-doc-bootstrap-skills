# simple-project-doc-bootstrap

장기 AI 개발 작업을 위한 최소 프로젝트 문서 체계를 초기화하고 유지하는 통합 스킬입니다.

이 스킬은 먼저 이 프로젝트가 `Codex` 기준인지 `Claude Code` 기준인지 확인합니다.
그 다음 선택된 워크플로우에 맞춰 규칙 문서를 하나만 관리합니다.

- Codex 선택 시 `AGENTS.md`
- Claude Code 선택 시 `CLAUDE.md`

공통으로는 아래 3개 문서를 함께 관리합니다.

- `PROJECT.md`
- `STATUS.md`
- `ARCHITECTURE.md`

## 핵심 철학

- 문서는 적을수록 좋다
- 문서는 현재 상태를 반영해야 한다
- 새 문서보다 기존 문서 갱신을 우선한다
- 사용자의 최신 요구사항이 기존 문서보다 우선한다
- 작업이 끝나면 관련 문서를 바로 현행화한다

## 동작 방식

1. 사용자가 이미 `Codex` 또는 `Claude Code`를 말했다면 그대로 사용한다.
2. 명시되지 않았다면 어느 워크플로우를 쓸지 먼저 묻는다.
3. 선택 결과에 따라 `AGENTS.md` 또는 `CLAUDE.md`를 고른다.
4. `PROJECT.md`, `STATUS.md`, `ARCHITECTURE.md`와 함께 최소 문서 세트를 정리한다.

## 호출 예시

### 신규 프로젝트

```text
simple-project-doc-bootstrap 스킬을 사용해서 이 프로젝트의 최소 문서 체계를 초기화해줘.

먼저 내가 Codex로 운영할지 Claude Code로 운영할지 확인해줘.

조건:
- 문서는 꼭 필요한 것만 만들어줘
- 규칙 문서는 선택된 워크플로우에 맞게 AGENTS.md 또는 CLAUDE.md 하나만 생성해줘
- PROJECT.md, STATUS.md, ARCHITECTURE.md도 함께 정리해줘
- STATUS.md는 긴 로그가 아니라 현재 상태 중심으로 써줘
```

### 기존 프로젝트 문서 정리

```text
simple-project-doc-bootstrap 스킬을 사용해서 이 저장소 문서를 최소 구조로 재정리해줘.

먼저 이 프로젝트를 Codex 기준으로 볼지 Claude Code 기준으로 볼지 확인해줘.

목표:
- 문서 수를 줄이고 싶어
- 오래된 내용과 중복 내용을 정리하고 싶어
- 규칙 문서는 하나만 기준 문서로 유지하고 싶어
```

### 작업 후 현행화

```text
방금 변경사항 기준으로 simple-project-doc-bootstrap 스킬 방식으로 문서를 현행화해줘.

먼저 이 프로젝트가 Codex인지 Claude Code인지 확인하고,
그 기준에 맞는 규칙 문서와 STATUS.md, ARCHITECTURE.md를 업데이트해줘.
```
