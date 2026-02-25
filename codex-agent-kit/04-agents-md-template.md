# AGENTS.md 템플릿 (리포지토리 루트용)

아래 템플릿은 루트 `AGENTS.md` 초안으로 바로 사용할 수 있습니다.

```md
# AGENTS.md

## Repository Overview

- Project type: [웹앱/SaaS/라이브러리 등]
- Primary goal: [핵심 목표]
- Non-goals: [이번 범위에서 하지 않을 것]

## Working Agreements

- Use `[package-manager]` for dependency management.
- Ask for confirmation before adding new production dependencies.
- Prefer minimal, targeted changes over broad refactors unless explicitly requested.
- If requirements are ambiguous and may affect architecture/data shape, ask first.

## Development Workflow

- Branch strategy: [main only / feature branches / ...]
- Commit message convention: [Conventional Commits / custom]
- Before starting implementation:
  - Confirm scope and acceptance criteria.
  - Check for existing patterns/files to follow.
- After code changes, run:
  - `[...]` (lint)
  - `[...]` (test)
  - `[...]` (build)

## Code Conventions

- Follow existing project structure and naming before introducing new patterns.
- Keep functions/components focused and small where practical.
- Add comments only for non-obvious logic or constraints.
- Handle errors explicitly; avoid silent failures.

## Quality Bar

- Minimum testing requirement: [핵심 로직/주요 플로우/...]
- Type safety rule: [strict 여부, any 허용 기준]
- Accessibility/responsive expectations (if frontend): [기준]
- Security-sensitive changes (auth/payment/secrets) require extra caution and confirmation.

## Documentation & Collaboration

- Update docs when public behavior, setup steps, or API contracts change.
- Record important decisions in `[docs/... or ADR]` if applicable.
- PR checklist before merge:
  - Scope matches request
  - Tests/lint/build pass
  - Docs updated if needed

## Codex-Specific Instructions

- Autonomy allowed:
  - [예: 작은 리팩터링, 테스트 추가, 문구 수정]
- Ask before:
  - [예: 신규 의존성, 스키마 변경, 대규모 구조 변경]
- Never do:
  - [예: 비밀키 회전, 파괴적 명령, 승인 없는 프로덕션 변경]
```

## 사용 팁

- 루트 파일에는 "공통 규칙"만 넣고, 특정 폴더 규칙은 하위 override로 분리하세요.
- 테스트/린트/빌드 명령은 실제 명령어로 구체적으로 적을수록 좋습니다.

