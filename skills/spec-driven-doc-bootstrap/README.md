# spec-driven-doc-bootstrap

프로그램 개발에서 비사소한 변경을 spec 단위로 정리하고 유지하는 스킬입니다.

이 스킬은 기능 요구사항, 구현 계획, 작업 체크리스트, 계약 변경, 테스트 정책, 운영 절차를 역할별 문서로 분리해 관리합니다.

## 핵심 문서

항상 중심이 되는 문서는 아래와 같습니다.

- `SPECS.md`
- `specs/<id-slug>/SPEC.md`
- `specs/<id-slug>/PLAN.md`
- `specs/<id-slug>/TASKS.md`

프로젝트 기준 문서와 함께 사용할 때는 아래 문서도 함께 봅니다.

- `AGENTS.md` 또는 `CLAUDE.md`
- `PROJECT.md`
- `STATUS.md`
- `ARCHITECTURE.md`

## 조건부 확장 문서

프로젝트 상황에 따라 아래 문서를 추가합니다.

- `DECISIONS.md`
- `CONTRACTS.md`
- `TESTING.md`
- `OPERATIONS.md`
- `fixtures/contracts/`

## 핵심 원칙

- 사소한 수정에는 새 spec를 만들지 않는다
- 요구사항, 구현 접근, 실행 체크리스트를 한 문서에 섞지 않는다
- 오래 남을 정보와 일시적인 작업 상태를 분리한다
- 계약 변경과 테스트 기준은 코드와 함께 갱신한다
- 구현 완료 후 관련 문서를 반드시 동기화한다

## 기본 흐름

1. 현재 저장소 구조와 기존 문서를 확인한다.
2. 프로젝트 기준 문서와 충돌하지 않도록 문서 역할을 나눈다.
3. 비사소한 작업이면 `SPECS.md`와 `specs/<id-slug>/`를 만든다.
4. 계약, 테스트, 운영 정보가 반복해서 필요할 때만 조건부 문서를 추가한다.
5. 작업 완료 후 `TASKS.md`, `SPECS.md`, 관련 기준 문서를 함께 갱신한다.

## 호출 예시

### 새 기능 spec 작성

```text
spec-driven-doc-bootstrap 스킬로 이번 기능의 spec 문서 세트를 만들어줘.

조건:
- 요구사항은 SPEC.md
- 구현 접근은 PLAN.md
- 작업 체크리스트는 TASKS.md
- API 계약 변경이 있으면 CONTRACTS.md도 같이 정리해줘
```

### 기존 spec 문서 정리

```text
spec-driven-doc-bootstrap 스킬로 이 저장소의 spec 문서를 재정리해줘.

목표:
- 진행 중인 spec 상태를 SPECS.md에 맞춰 정리
- 오래된 TASKS.md는 현재 상태 중심으로 갱신
- 필요한 경우 DECISIONS.md, TESTING.md를 추가
```
