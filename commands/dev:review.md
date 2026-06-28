---
description: Perform a thorough code review for a change
---

# Code Review

Perform a thorough code review that verifies functionality, maintainability, and security before approving a change. Focus on architecture, readability, performance implications, and provide actionable suggestions for improvement.

## Inputs

- Optional PR, branch, commit range, file path, or review focus: `$ARGUMENTS`

## Steps

1. **Understand the change**
   - Read the PR description, issue, branch context, commit range, or files named in `$ARGUMENTS` when provided.
   - If no target is provided, review the current repository changes using git status and diff.
   - Identify the scope of files and features impacted.
   - Note any assumptions or questions to clarify with the author.
2. **Validate functionality**
   - Confirm the code delivers the intended behavior.
   - Exercise edge cases or guard conditions mentally or by running focused local checks when appropriate.
   - Check error handling paths and logging for clarity.
3. **Assess quality**
   - Ensure functions are focused, names are descriptive, and code is readable.
   - Watch for duplication, dead code, unnecessary abstractions, or missing tests.
   - Verify documentation and comments reflect the latest changes.
4. **Review security and risk**
   - Look for injection points, insecure defaults, missing validation, and unsafe parsing.
   - Confirm secrets or credentials are not exposed.
   - Evaluate performance, scalability, resource management, and operational impacts.
5. **Provide actionable feedback**
   - Prioritize findings by severity and user impact.
   - Include concrete file paths, examples, and suggested fixes.
   - Distinguish blocking issues from optional improvements.

## Review Checklist

### Functionality

- [ ] Intended behavior works and matches requirements
- [ ] Edge cases handled gracefully
- [ ] Error handling is appropriate and informative

### Code Quality

- [ ] Code structure is clear and maintainable
- [ ] No unnecessary duplication or dead code
- [ ] Tests/documentation updated as needed

### Security & Safety

- [ ] No obvious security vulnerabilities introduced
- [ ] Inputs validated and outputs sanitized
- [ ] Sensitive data handled correctly

## Additional Review Notes

- Architecture and design decisions considered
- Performance bottlenecks or regressions assessed
- Coding standards and best practices followed
- Resource management, error handling, and logging reviewed
- Suggested alternatives, additional test cases, or documentation updates captured

## Output

Provide constructive feedback with concrete examples and actionable guidance for the author. If there are no blocking issues, say so explicitly and still note any non-blocking risks or follow-ups.
