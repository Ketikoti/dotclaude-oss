# Rule: Code Style

## General

- Use clear, descriptive names for variables, functions, and classes
- Prefer explicit over implicit
- Keep functions small and focused on a single responsibility
- Maximum function length: 50 lines (refactor if longer)
- Maximum file length: 300 lines (split if longer)

## Naming Conventions

- **Variables & functions**: camelCase (JS/TS) or snake_case (Python)
- **Classes & components**: PascalCase
- **Constants**: UPPER_SNAKE_CASE
- **Files**: kebab-case for components, snake_case for Python modules

## Comments

- Write comments for WHY, not WHAT
- Remove commented-out code before committing
- Use JSDoc / docstrings for public APIs

## Formatting

- Use Prettier (JS/TS) or Black (Python) for auto-formatting
- 2-space indentation for JS/TS, 4-space for Python
- Trailing commas where valid
- Single quotes for JS/TS strings

## Imports

- Group imports: stdlib > third-party > local
- No unused imports
- Use absolute imports over relative where possible

## Error Handling

- Always handle errors explicitly
- Never swallow exceptions silently
- Log errors with context (not just the error message)
- Return meaningful error messages to callers
