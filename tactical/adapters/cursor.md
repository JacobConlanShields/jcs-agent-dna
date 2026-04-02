# Cursor Adapter
## How to load jcs-agent-dna into Cursor

Cursor reads .cursorrules from the project root.

### Setup

After adding the jcs-agent-dna submodule:

```bash
git submodule add https://github.com/YOURUSER/jcs-agent-dna .jcs-agent-dna
```

Create .cursorrules in the project root:

```
Read and follow the agent configuration files in .jcs-agent-dna/.
Load order:
1. constitutional/IDENTITY.md
2. constitutional/VOICE.md
3. strategic/SOUL.md
4. strategic/MEMORY.md
5. strategic/SPIRIT.md (when populated)
6. strategic/GOALS.md
7. strategic/AGENTS.md
8. strategic/USER.md
9. tactical/PROJECTS.md
10. tactical/CONTEXT.md
11. tactical/CANON.md
IDENTITY.md and VOICE.md are immutable — never contradict them.
AGENTS.md contains decision-making rules — follow them.
PROJECTS.md and CONTEXT.md have current project state — reference for awareness.
Note: MEMORY.md is listed under strategic/ in the load order to
reflect its reading priority, even though it lives in tactical/.
```

### Notes

Cursor's .cursorrules file has a size limit. Keep the loader
directive short and let the referenced files carry the detail.
If Cursor cannot read submodule files directly, copy the contents
into .cursorrules or use the pull script from the jcs-agent-dna README.
