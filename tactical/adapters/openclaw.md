# OpenClaw Adapter
## How to load dotnd into OpenClaw / Cline

OpenClaw reads AGENTS.md from the workspace root and follows file
references within it.

### Setup

In your OpenClaw workspace, create or update AGENTS.md to reference
the dotnd submodule:

```bash
git submodule add https://github.com/YOURUSER/dotnd .dotnd
```

Then in your workspace AGENTS.md:

```
# Agent Configuration

Read and internalize all files in .dotnd/ according to the tier
system defined there. Constitutional files are immutable. Strategic
files guide behavior. Tactical files provide current context.

File load order:
1. .dotnd/constitutional/IDENTITY.md
2. .dotnd/constitutional/VOICE.md
3. .dotnd/strategic/SOUL.md
4. .dotnd/strategic/AGENTS.md
5. .dotnd/tactical/CONTEXT.md
6. .dotnd/tactical/CANON.md

Project-specific instructions follow below.
```

### Notes

OpenClaw's AGENTS.md is the natural entry point. The dotnd
AGENTS.md (in strategic/) contains the operating rules. The
workspace AGENTS.md acts as a loader that points to the submodule
and adds project context.
