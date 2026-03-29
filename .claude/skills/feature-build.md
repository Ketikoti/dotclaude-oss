# Skill: feature-build

> End-to-end workflow for building a new feature from scratch.
> Combines /spec, /ship, and /review into one coherent process.

## When to use

Use this skill when:
- Starting a new feature from a ticket or requirement
- You want a repeatable, quality-first build process
- The feature touches multiple files or services

## Full Workflow

### Phase 1: Understand
1. Read the feature requirement carefully
2. Identify any ambiguities — resolve before proceeding
3. Check if similar features already exist (don't duplicate)
4. Identify which parts of the codebase are affected

### Phase 2: Specify
Run `/spec` to produce:
- Problem statement
- Technical design
- Edge cases
- Test plan
- Definition of done

Do NOT proceed until the spec is confirmed.

### Phase 3: Build
Run `/ship` to:
1. Explore existing code
2. Plan the implementation
3. Write the code
4. Write tests
5. Verify everything passes
6. Commit

### Phase 4: Review
Run `/review` or activate `code-reviewer` agent to:
- Check correctness, security, and quality
- Verify test coverage
- Confirm the implementation matches the spec

### Phase 5: Ship
- Ensure CI passes
- Update any relevant documentation
- Create PR with clear description referencing the spec

## Success Metrics

- Feature works as specified
- Tests cover happy path + edge cases
- No regressions introduced
- PR is focused and reviewable (< 400 lines changed where possible)
