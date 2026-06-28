# agent-kit
agent-kit is a curated toolkit for coding agents: reusable skills, slash commands, extensions, custom tools, and workflow presets for making AI-assisted development more reliable,  consistent, and project-aware.

## Install for Oh My Pi

Run from the repository root to install this project's slash commands and skills at the Oh My Pi user level:

```bash
mkdir -p ~/.omp/agent/commands ~/.omp/agent/skills
cp commands/*.md ~/.omp/agent/commands/
cp -R skills/* ~/.omp/agent/skills/
```

This installs:

- Slash commands to `~/.omp/agent/commands/`
- Skills to `~/.omp/agent/skills/`

### Install a single command or skill

Install one slash command:

```bash
mkdir -p ~/.omp/agent/commands
cp commands/git:commit.md ~/.omp/agent/commands/
```

Install one skill:

```bash
mkdir -p ~/.omp/agent/skills
cp -R skills/karpathy-guidelines ~/.omp/agent/skills/
```

Replace `commands/git:commit.md` or `skills/karpathy-guidelines` with the command file or skill directory you want to install.

Restart or refresh your Oh My Pi session if the new commands or skills are not visible immediately.
