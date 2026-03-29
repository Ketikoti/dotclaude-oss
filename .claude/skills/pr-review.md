# Skill: pr-review

> Structured pull request review workflow.
> Use when reviewing a PR from a teammate or your own PR before requesting review.

## Preparation

1. Read the PR description fully before looking at any code
2. Understand the ticket/issue this PR addresses
3. Check the PR size — if > 600 lines changed, ask for it to be split

## Review Steps

### Step 1: High-level check
- Does the PR do what the description says?
- Is the scope appropriate (not too large, not too small)?
- Are there any obvious missing pieces?

### Step 2: Code review
Activate `code-reviewer` agent and run through the checklist:
- Correctness
- Security
- Performance
- Test coverage
- Code quality

### Step 3: Test review
- Run the tests locally if possible
- Check that new tests actually test the right things
- Verify no tests were deleted without reason

### Step 4: Documentation check
- Are public APIs documented?
- Is the README updated if needed?
- Are any migration steps documented?

## PR Checklist (for PR author)

- [ ] PR description explains WHAT and WHY
- [ ] PR is linked to an issue or ticket
- [ ] Self-reviewed before requesting review
- [ ] Tests written and passing
- [ ] No debug code left in
- [ ] CI passing
- [ ] Docs updated if needed

## Feedback Guidelines

- Be specific: cite file and line number
- Explain WHY something is an issue
- Distinguish blockers from suggestions
- Be constructive and respectful
