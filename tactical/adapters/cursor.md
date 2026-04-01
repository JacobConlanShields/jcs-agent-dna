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
Load order: constitutional/ first, then strategic/, then tactical/.
IDENTITY.md and VOICE.md are immutable — never contradict them.
AGENTS.md contains decision-making rules — follow them.
CONTEXT.md has current project state — reference for awareness.
```

### Notes

Cursor's .cursorrules file has a size limit. Keep the loader
directive short and let the referenced files carry the detail.
If Cursor cannot read submodule files directly, copy the contents
into .cursorrules or use the pull script from the jcs-agent-dna README.
