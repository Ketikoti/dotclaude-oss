# Command: /fix-issue

> Targeted, safe bug fix workflow.
> Use for fixing a specific issue without causing regressions.

## Workflow

### Step 1: Understand the Bug
- Read the issue/bug report carefully
- Reproduce the bug locally before touching any code
- Identify the exact failure point
- Understand WHY it's failing, not just WHERE

### Step 2: Locate the Root Cause
- Trace the execution path
- Check recent commits that may have introduced the bug
- Look for related tests that may reveal intent
- Do NOT fix symptoms — fix the root cause

### Step 3: Plan the Fix
- Describe the fix in one sentence before writing any code
- Identify which files will change
- Identify potential side effects
- Check if any existing tests need updating

### Step 4: Implement
- Make the smallest change that fixes the root cause
- Do not refactor or clean up unrelated code in the same fix
- Add a comment if the fix is non-obvious

### Step 5: Write a Regression Test
- Write a test that fails WITHOUT the fix
- Verify the test passes WITH the fix
- Add it to the appropriate test file

### Step 6: Verify
- Run the full test suite (not just the new test)
- Check for regressions in related functionality
- Manually verify the fix in the affected flow

### Step 7: Commit
- Commit message: `fix: <short description of what was fixed>`
- Reference the issue: `fix: handle null user on login (#99)`

## Anti-patterns to avoid

- Never add a workaround without fixing the root cause
- Never skip writing the regression test
- Never bundle a bug fix with unrelated refactoring
