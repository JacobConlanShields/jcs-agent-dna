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
4. strategic/MEMORY.md — accumulated memory and anti-pattern register.
5. strategic/SPIRIT.md — why we build what we build (if populated).
6. strategic/GOALS.md — north star, mission, values.
7. strategic/AGENTS.md — decision-making and operating rules.
8. strategic/USER.md — how to work with Jake (if populated).
9. tactical/PROJECTS.md — operational hub and project registry.
10. tactical/CONTEXT.md — current constraints and tool stack.
11. tactical/CANON.md — intellectual inputs and references.

Note: MEMORY.md is listed under strategic/ in the load order to
reflect its reading priority, even though it lives in tactical/.

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
