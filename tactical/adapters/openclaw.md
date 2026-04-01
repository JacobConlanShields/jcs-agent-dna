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
4. .jcs-agent-dna/strategic/AGENTS.md
5. .jcs-agent-dna/tactical/CONTEXT.md
6. .jcs-agent-dna/tactical/CANON.md

Project-specific instructions follow below.
```

### Notes

OpenClaw's AGENTS.md is the natural entry point. The jcs-agent-dna
AGENTS.md (in strategic/) contains the operating rules. The
workspace AGENTS.md acts as a loader that points to the submodule
and adds project context.
