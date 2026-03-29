# Rule: Testing

## Mandatory

- Every new feature must have tests before merge
- Every bug fix must include a regression test
- Tests must pass before committing

## Test Types

| Type | Coverage Goal | Tool |
|---|---|---|
| Unit | All business logic functions | pytest / Jest |
| Integration | All API endpoints | pytest / Supertest |
| E2E | Critical user flows | Playwright / Cypress |

## Standards

- Test file naming: `test_*.py` or `*.test.ts` or `*.spec.ts`
- One assertion focus per test
- Use descriptive test names: `should_return_404_when_user_not_found`
- Mock external services (API calls, DB) in unit tests
- Use real DB in integration tests (test DB, not production)

## Coverage

- Minimum coverage: 80% for new code
- Never lower existing coverage
- Coverage report must be part of CI pipeline

## Definition of Done

- [ ] Unit tests written and passing
- [ ] Integration tests written and passing
- [ ] No existing tests broken
- [ ] Coverage threshold maintained
