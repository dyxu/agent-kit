# Repository Guidelines

## Project Overview

`agent-kit` is a Markdown-first toolkit for coding agents: reusable slash commands, skills, extensions, custom tools, and workflow presets for making AI-assisted development more reliable, consistent, and project-aware.

## Architecture & Data Flow

- The repository is content-driven, not an executable app or package workspace.
- Public artifacts are discovered by external agent runtimes:
  - Slash commands: `commands/*.md`
  - Skills: `skills/<skill-name>/SKILL.md`
- Markdown files use YAML frontmatter for discovery metadata, then procedural Markdown instructions for behavior.
- Slash-command flow: user invokes `/namespace:command ...` → runtime expands `$ARGUMENTS` → command body instructs the agent → agent creates the requested artifact or performs the requested workflow.
- Skill flow: runtime loads `SKILL.md` by frontmatter `name` → agent applies the Markdown guidance during matching tasks.

