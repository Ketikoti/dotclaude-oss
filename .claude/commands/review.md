# Command: /review

> Deep code review with a structured checklist.
> Use before merging any non-trivial change.

## Review Checklist

### Correctness
- [ ] Does the code do what it claims to do?
- [ ] Are edge cases handled?
- [ ] Are error cases handled explicitly?
- [ ] Is there any off-by-one, null, or type error risk?

### Code Quality
- [ ] Is the code readable without needing comments to understand?
- [ ] Are functions small and single-purpose?
- [ ] Is there duplication that should be extracted?
- [ ] Are variable names clear and descriptive?

### Security
- [ ] Are inputs validated?
- [ ] Are there any SQL injection, XSS, or CSRF risks?
- [ ] Are secrets handled correctly (not hardcoded)?
- [ ] Are permissions checked server-side?

### Tests
- [ ] Are there tests for the happy path?
- [ ] Are there tests for edge cases?
- [ ] Are there tests for error cases?
- [ ] Do the tests actually test behavior, not just implementation?

### Performance
- [ ] Are there any obvious N+1 query issues?
- [ ] Are there unnecessary database calls in loops?
- [ ] Is caching used appropriately?

### Conventions
- [ ] Does the code follow `.claude/rules/code-style.md`?
- [ ] Does the commit message follow Conventional Commits?
- [ ] Is the PR scope focused (not too large)?

## Output Format

Provide:
1. **Summary**: 1-2 sentence overview of what the code does
2. **Issues found**: List of specific issues with line references
3. **Suggestions**: Optional improvements (not blockers)
4. **Verdict**: APPROVE / REQUEST CHANGES / NEEDS DISCUSSION
