# OpenClaw Adapter
## How to load jcs-agent-dna into OpenClaw / Cline

OpenClaw reads AGENTS.md from the workspace root and follows file
references within it.

### Setup

In your OpenClaw workspace, create or update AGENTS.md to reference
the jcs-agent-dna submodule:

```bash
git submodule add https://github.com/YOURUSER/jcs-agent-dna .jcs-agent-dna
```

Then in your workspace AGENTS.md:

```
# Agent Configuration

Read and internalize all files in .jcs-agent-dna/ according to the tier
system defined there. Constitutional files are immutable. Strategic
files guide behavior. Tactical files provide current context.

File load order:
1. .jcs-agent-dna/constitutional/IDENTITY.md
2. .jcs-agent-dna/constitutional/VOICE.md
3. .jcs-agent-dna/strategic/SOUL.md
4. .jcs-agent-dna/strategic/MEMORY.md
5. .jcs-agent-dna/strategic/SPIRIT.md (when populated)
6. .jcs-agent-dna/strategic/GOALS.md
7. .jcs-agent-dna/strategic/AGENTS.md
8. .jcs-agent-dna/strategic/USER.md
9. .jcs-agent-dna/tactical/PROJECTS.md
10. .jcs-agent-dna/tactical/CONTEXT.md
11. .jcs-agent-dna/tactical/CANON.md

Note: MEMORY.md is listed under strategic/ in the load order to
reflect its reading priority, even though it lives in tactical/.

Project-specific instructions follow below.
```

### Notes

OpenClaw's AGENTS.md is the natural entry point. The jcs-agent-dna
AGENTS.md (in strategic/) contains the operating rules. The
workspace AGENTS.md acts as a loader that points to the submodule
and adds project context.
