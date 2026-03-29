# Command: /ship

> Full end-to-end workflow: plan → implement → test → commit.
> Use this for any non-trivial feature or change.

## When to use

Use `/ship` when:
- Building a new feature
- Making a non-trivial change
- You want to ensure quality end-to-end

## Workflow

### Step 1: Explore
- Read all relevant existing files before touching anything
- Understand the current structure, conventions, and dependencies
- Identify potential side effects of the change

### Step 2: Plan
- Write a brief plan (bullet points are fine)
- Identify which files will change
- Identify which tests need to be written or updated
- Confirm the plan makes sense before proceeding

### Step 3: Implement
- Follow `.claude/rules/code-style.md`
- Follow `.claude/rules/api-conventions.md` for API changes
- Follow `.claude/rules/security.md` for any auth/data changes
- Keep changes focused: one concern per commit

### Step 4: Test
- Write unit tests for all new logic
- Write integration tests for API changes
- Run the full test suite
- Fix any failures before proceeding

### Step 5: Commit
- Use Conventional Commits format: `feat:`, `fix:`, `refactor:`, `docs:`, `test:`
- Keep commit message under 72 characters
- Reference issue number if applicable: `feat: add user auth (#42)`

## Definition of Done

- [ ] Code is implemented and working
- [ ] Tests are written and passing
- [ ] No existing tests broken
- [ ] Lint/type checks passing
- [ ] Commit message follows convention
- [ ] No debug code or console.logs left in
