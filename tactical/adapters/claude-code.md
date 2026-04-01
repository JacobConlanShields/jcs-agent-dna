# Claude Code Adapter
## How to load jcs-agent-dna into Claude Code

Claude Code reads CLAUDE.md from the project root and parent
directories.

### Global setup (applies to all projects)

Create ~/.claude/CLAUDE.md with the following content:

```
# Agent Configuration

Read the following files from the .jcs-agent-dna submodule in this project
(or from ~/.jcs-agent-dna/ if no submodule exists) and follow all
instructions within:

1. constitutional/IDENTITY.md — who Jake is. Do not contradict.
2. constitutional/VOICE.md — writing style. Match on all outputs.
3. strategic/SOUL.md — operating philosophy. Internalize.
4. strategic/AGENTS.md — decision-making and operating rules.
5. tactical/CONTEXT.md — current projects and constraints.
6. tactical/CANON.md — intellectual inputs and references.

If strategic/USER.md and strategic/SPIRIT.md exist and are
populated, read those as well.

For project-specific context, also read any project-context.md
in the project root.
```

### Per-project setup

After adding the jcs-agent-dna submodule to a project:

```bash
git submodule add https://github.com/YOURUSER/jcs-agent-dna .jcs-agent-dna
```

Create a project-level CLAUDE.md that references the submodule:

```
# Project Agent Configuration

Global agent config: .jcs-agent-dna/
Project-specific context follows.

## Project: [name]
[project-specific instructions here]
```
