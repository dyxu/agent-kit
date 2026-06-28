---
description: Run the full test suite and fix failures
---

# Run All Tests and Fix Failures

Execute the full test suite and systematically fix any failures, ensuring code quality and functionality.

## Inputs

- Optional test command, package target, or focus area: `$ARGUMENTS`

## Steps

1. **Determine the test command**
   - If `$ARGUMENTS` includes a concrete command, use it.
   - Otherwise inspect project configuration and existing documentation to find the full test-suite command.
   - Prefer the repository's declared package manager and scripts; do not invent tooling.
2. **Run test suite**
   - Execute the full test suite for the project.
   - Capture output and identify failures.
   - Check both unit and integration tests when present.
3. **Analyze failures**
   - Categorize failures by type: flaky, broken, new failures, environment/setup.
   - Prioritize fixes based on impact and root cause.
   - Check whether failures are related to recent changes.
4. **Fix issues systematically**
   - Start with the most critical or root-cause failure.
   - Fix one issue at a time.
   - Re-run the relevant failing test after each fix.
   - Re-run the full test suite after targeted failures pass.
5. **Report results**
   - Summarize the root cause, changed files, and final passing command.
   - If a failure cannot be fixed because of missing external services or credentials, state the blocker and what was verified locally.

## Test Recovery Checklist

- [ ] Full test suite executed
- [ ] Failures categorized and tracked
- [ ] Root causes resolved
- [ ] Relevant failing tests re-run after each fix
- [ ] Full test suite re-run with passing results
- [ ] Follow-up improvements noted only when they are outside the requested fix
