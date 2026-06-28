---
description: Create a concise Git commit from the current changes
---

Create a short, focused Git commit for the current repository changes.

## Inputs

- Optional inline issue key or prefix: `$ARGUMENTS`

## Procedure

1. Stage the working tree with `git add -A`.
2. Inspect repository state with `git status --short`.
3. Inspect staged changes with `git diff --cached`.
4. Derive the commit message only from the actual diff.
5. If `$ARGUMENTS` is non-empty, treat it as the issue key or prefix and prepend it to the commit subject as `<issue-key>: `.
6. If `$ARGUMENTS` is empty, infer an issue key from the branch name only when an obvious key is present, such as `PROJ-123` or `#123`; otherwise commit without an issue key and do not ask.
7. Run `git commit -m "<subject>"`.

## Commit message rules

- Use this shape: `<type>(<scope>): <Summary>`.
- With an issue key or prefix: `<issue-key>: <type>(<scope>): <Summary>`.
- Keep the final subject at or under 72 characters when practical.
- Use imperative mood: `fix`, `add`, `update`, not `fixed`, `added`, `updated`.
- Capitalize the summary's first word.
- Do not end with a period.
- Prefer the smallest honest scope from the diff.
- Describe the user-visible reason or effect, not just file movement.

## Output

Report the commit hash and subject after the commit succeeds. If there are no changes to commit, say so and do not create an empty commit.
