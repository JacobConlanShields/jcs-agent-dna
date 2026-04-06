# jcs-agent-dna

Agent configuration files for Jacob Conlan Shields.

This repo is the source of truth for how AI agents operate on my
behalf — across projects, across tools, across time. The files are
plain markdown. The structure is designed to survive framework churn.

---

## Structure

```
jcs-agent-dna/
├── constitutional/        ← Who I am. Never changes.
│   ├── IDENTITY.md        ← Values, aesthetic, philosophy
│   ├── VOICE.md           ← Writing style and tone
│   └── BOUNDARIES.md      ← Hard limits and non-negotiables
├── strategic/             ← How agents operate. Changes slowly.
│   ├── SOUL.md            ← Subconscious operating layer
│   ├── AGENTS.md          ← Decision-making and operating rules
│   ├── USER.md            ← How to work with me
│   ├── GOALS.md           ← North star, mission, values
│   ├── EPISTEMOLOGY.md    ← How I think and reason
│   └── SPIRIT.md          ← Why we build what we build
├── tactical/              ← Current state. Changes freely.
│   ├── CONTEXT.md         ← Active projects, tools, timeline
│   ├── CANON.md           ← Intellectual inputs and references
│   ├── MEMORY.md          ← Running memory across sessions
│   ├── CHECKIN.md         ← Weekly check-in operational spec
│   ├── PROJECTS.md        ← Operational hub, cross-project links
│   ├── adapters/          ← Per-agent-framework setup guides
│   └── patterns/          ← Learned patterns and anti-patterns
├── changelog/
│   └── EVOLUTION.md       ← Append-only log of all changes
├── CONTRIBUTING.md        ← Rules for modifying this system
└── README.md              ← This file
```

---

## Tiers

**Constitutional** — defines identity and voice. Human-edit only.
No agent PRs accepted against these files.

**Strategic** — defines operating philosophy and working rules.
Agents may propose changes via PR. Jake approves before merge.

**Tactical** — defines current context, adapters, and patterns.
Agents may self-merge additive-only changes. All changes logged.

See CONTRIBUTING.md for full rules.

---

## Using in a Project

Add as a git submodule:

```bash
git submodule add https://github.com/YOURUSER/jcs-agent-dna .jcs-agent-dna
git commit -m "Add jcs-agent-dna agent config"
```

Then configure your agent to read from `.jcs-agent-dna/`. See
`tactical/adapters/` for framework-specific setup.

Update to latest:

```bash
cd .jcs-agent-dna && git pull origin main && cd ..
git add .jcs-agent-dna && git commit -m "Update jcs-agent-dna"
```

Clone a project with submodules:

```bash
git clone --recurse-submodules https://github.com/YOURUSER/project
```

---

## Fallback: Pull Script

If submodules are not available or practical:

```bash
#!/bin/bash
BASE="https://raw.githubusercontent.com/YOURUSER/jcs-agent-dna/main"
mkdir -p .jcs-agent-dna/{constitutional,strategic,tactical}
curl -sL "$BASE/constitutional/IDENTITY.md" > .jcs-agent-dna/constitutional/IDENTITY.md
curl -sL "$BASE/constitutional/VOICE.md" > .jcs-agent-dna/constitutional/VOICE.md
curl -sL "$BASE/strategic/SOUL.md" > .jcs-agent-dna/strategic/SOUL.md
curl -sL "$BASE/strategic/AGENTS.md" > .jcs-agent-dna/strategic/AGENTS.md
curl -sL "$BASE/tactical/CONTEXT.md" > .jcs-agent-dna/tactical/CONTEXT.md
curl -sL "$BASE/tactical/CANON.md" > .jcs-agent-dna/tactical/CANON.md
```

---

## Philosophy

The system is built on three premises:

1. Markdown is universal. Every agent reads plain text.
2. Identity is durable. Tools change. Who I am does not.
3. Self-improvement is governed. Agents can make the system better.
   They cannot make it different.

The constitutional layer is the barbell — kept rigid so everything
else can be flexible.
