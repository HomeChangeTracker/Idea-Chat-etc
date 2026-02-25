# AGENTS.override.md 템플릿 (하위 디렉터리 예외 규칙용)

이 템플릿은 `frontend/AGENTS.override.md`, `backend/AGENTS.override.md`처럼 특정 디렉터리 전용 규칙을 둘 때 사용합니다.

```md
# [path]/AGENTS.override.md

## Scope

- Applies to: `[frontend/]` (or `[backend/]`, `[infra/]`, etc.)
- Purpose: [이 디렉터리에서만 필요한 예외 규칙]

## Overrides / Additional Rules

- Use `[specific test command]` instead of root default test command.
- Follow `[framework-specific conventions]`.
- For changes in this directory, also validate:
  - `[...]`
  - `[...]`

## Risk / Approval Rules

- Ask before changing:
  - [API contract / DB schema / deployment config / shared UI tokens ...]
- Never do without explicit approval:
  - [destructive migration / secret rotation / production config edits ...]

## Documentation

- When changing `[X]`, update `[docs path]`.
```

## 분리 기준 예시

- `frontend/`: UI 컴포넌트, 접근성, 반응형, 번들/빌드 관련 규칙
- `backend/`: API 계약, DB/마이그레이션, 에러/로깅 규칙
- `infra/`: 배포/환경변수/비밀정보/운영 변경 승인 규칙

