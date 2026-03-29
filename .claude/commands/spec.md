# Command: /spec

> Write a specification before building anything.
> Always run /spec before /ship for non-trivial features.

## Purpose

Force clarity before coding. A good spec prevents wrong implementations, scope creep, and wasted effort.

## Spec Template

When running `/spec`, produce a document with these sections:

### 1. Problem Statement
What problem does this solve? Who has this problem?

### 2. Proposed Solution
What will we build? High-level approach.

### 3. Scope
**In scope:**
- Feature A
- Feature B

**Out of scope:**
- Feature C (future)

### 4. Technical Design
- Which files/modules will change?
- What new files will be created?
- What database changes are needed?
- What API changes are needed?

### 5. Edge Cases
List at least 3 edge cases to handle.

### 6. Test Plan
- Unit tests: what functions need coverage?
- Integration tests: what endpoints/flows need testing?
- Manual tests: what should QA verify?

### 7. Definition of Done
- [ ] All acceptance criteria met
- [ ] Tests written and passing
- [ ] Code reviewed
- [ ] Documentation updated

## Instructions

1. Generate the spec above for the described feature
2. Ask clarifying questions if the requirements are ambiguous
3. Do NOT write any code until the spec is confirmed
4. Save the spec as a comment or in a temporary file for reference
