# Command: /refactor

> Safe structural cleanup without changing behavior.
> Refactoring improves maintainability but must never introduce bugs.

## Rules

- Refactoring must NOT change observable behavior
- Always run the full test suite before AND after
- Keep refactoring commits separate from feature or fix commits
- Make small, incremental changes — not one giant cleanup

## When to refactor

- A function is doing more than one thing
- A file is over 300 lines
- Code is duplicated in 3+ places
- A name is misleading or unclear
- A module has too many dependencies

## Refactoring Patterns

### Extract Function
Move logic into a named function to improve readability.

### Extract Module/File
Split a large file into smaller, focused modules.

### Rename for Clarity
Rename variables, functions, or files that are confusing.

### Remove Duplication
Extract shared logic into a utility or helper.

### Simplify Conditionals
Replace complex if/else chains with early returns or lookup tables.

## Workflow

1. Run tests — confirm they pass BEFORE starting
2. Identify the specific smell to fix (one at a time)
3. Make the change
4. Run tests again — confirm they still pass
5. Commit with message: `refactor: <what was cleaned up>`
6. Repeat for next smell

## Definition of Done

- [ ] All tests still pass
- [ ] No behavior change introduced
- [ ] Code is simpler and more readable than before
- [ ] Commit message uses `refactor:` prefix
