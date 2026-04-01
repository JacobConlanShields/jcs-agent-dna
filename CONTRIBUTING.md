# CONTRIBUTING.md
## How to Modify the dotnd System

This file governs how changes are made to dotnd — whether by a
human or an agent.

---

## Tier System

Files are organized into three tiers. The tier determines who can
change the file and how.

### Constitutional (human-only)
Location: `constitutional/`
Contains: IDENTITY.md, VOICE.md

These files define who Jake is and how he communicates. They do not
change based on tools, projects, or agent frameworks. Only Jake
edits these files, directly on the main branch or via PR he authors
himself.

Agents may suggest changes to constitutional files in conversation.
Agents must never file a PR against constitutional files.

### Strategic (agent-proposes, human-approves)
Location: `strategic/`
Contains: SOUL.md, AGENTS.md, USER.md, SPIRIT.md

These files define operating philosophy, decision-making rules, and
working preferences. They evolve slowly and deliberately.

Agents may propose changes by opening a PR. All strategic PRs
require Jake's review and approval before merge. PRs must follow
the format below.

### Tactical (agent-managed, logged)
Location: `tactical/`
Contains: CONTEXT.md, CANON.md, MEMORY.md, adapters/, patterns/

These files change frequently. Agents may open PRs and self-merge
tactical changes if the change is additive only (no deletions, no
modifications to existing content). All changes must be logged in
`changelog/EVOLUTION.md`.

---

## PR Requirements

Every PR must include:

- **Branch name**: `improve/short-description`
- **WHAT**: What changed (the diff is visible, but summarize)
- **WHY**: What triggered this — a failure, a friction, a new
  capability, a new tool
- **RISK**: What could go wrong if this change is wrong
- **REVERSIBILITY**: How to undo if needed
- **EVOLUTION entry**: Append one line to `changelog/EVOLUTION.md`

---

## Rules That Never Bend

1. Never delete content from strategic or constitutional files —
   only add or modify
2. Never change the tier classification of a file
3. Never remove a constraint without documenting the rationale
   for removal
4. Never modify this list of rules via PR — only Jake edits these
   directly
5. The evolution log is append-only — never edit previous entries
