# CLAUDE.md

<!-- Keep this file SHORT. Project-specific context only. -->
<!-- Detailed rules live in .claude/rules/ -->
<!-- Commands live in .claude/commands/ -->
<!-- Agents live in .claude/agents/ -->

## Project

Describe your project here in 2-3 sentences.
What does it do? What stack does it use? What is the primary goal?

## Architecture

- **Frontend**: (e.g. Next.js / React / Vue)
- **Backend**: (e.g. FastAPI / Django / Node)
- **Database**: (e.g. PostgreSQL / MongoDB)
- **Infrastructure**: (e.g. Docker / GCP / Azure)

## Workflow

Always follow this order:
1. **Explore** — read relevant files before making changes
2. **Plan** — think through the approach, check assumptions
3. **Implement** — write clean, tested code
4. **Verify** — run tests, lint, check for regressions
5. **Commit** — clear commit message following Conventional Commits

## Quality Standards

- All new code must have tests
- No secrets in code or commits
- Follow rules in `.claude/rules/`
- Run lint and type checks before committing
- Prefer clarity over cleverness

## Key Commands

| Command | Purpose |
|---|---|
| `/spec` | Write spec before building |
| `/ship` | Full plan-build-test-commit cycle |
| `/review` | Deep code review |
| `/fix-issue` | Targeted bug fix |
| `/refactor` | Safe cleanup |

## What NOT to do

- Never modify files outside the current task scope
- Never commit without running tests
- Never skip the planning step for non-trivial changes
- Never store credentials in code

## References

- Rules: `.claude/rules/`
- Commands: `.claude/commands/`
- Agents: `.claude/agents/`
- Skills: `.claude/skills/`
- Personal overrides: `.claude/*.local.md` (gitignored)
