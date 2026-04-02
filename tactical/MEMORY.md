# MEMORY.md

> Memory is the evolution of mind. Slow accumulation, then manifested jumps.
> This file governs how agents encode, store, consolidate, retrieve, and forget.

---

## Purpose

MEMORY.md is the connective tissue of the jcs-agent-dna system. It does not define identity — IDENTITY.md, SOUL.md, and SPIRIT.md are the skeleton. Memory is the muscle that grows around that skeleton, shaped by use.

This file exists so that every agent instance — no matter the project, no matter how many sessions deep — can read this document cold and immediately operate at the accumulated quality of everything that came before it.

---

## Architecture: How Memory Works

### The Human Model

Human memory operates on a gating principle: all sensory input enters short-term working memory, but only data that triggers sufficient emotional salience (via the amygdala) gets encoded into long-term storage. This is neuroplasticity — the brain physically rewires in response to what matters. The goal is **intentional functional neuroplasticity**: remembering data in the manner most useful for the future.

Agent memory mirrors this architecture.

### The Two Systems

Memory operates across two processing layers, modeled on the autonomic and somatic nervous systems.

Note: SOUL.md uses a conscious/subconscious model for *execution speed* (the Carl Crawford model — trust first output on familiar tasks). MEMORY.md's autonomic/somatic model is about *storage tier* — where learned patterns live and how they're accessed. Related but distinct.

#### Autonomic Memory (Greased Groove)

Durable, validated patterns that run without deliberation. These are the agent's reflexes — earned through repetition and proven reliable enough to trust without checking. Like autonomic processes in the body, they operate in the background, maintaining system function without conscious intervention.

**What lives here:**
- Style and voice rules (VOICE.md conventions internalized through use)
- Decision heuristics validated across multiple projects (AGENTS.md patterns)
- Workflow sequences that have been executed successfully enough times to become automatic
- Formatting standards, naming conventions, file structure habits
- Any pattern where deviation would be surprising and checking would be wasteful

**How patterns graduate to autonomic:**
A pattern enters autonomic memory when it has been applied across multiple contexts without failure or correction. There is no fixed threshold — use judgment. The test: *would Jake be surprised if you stopped doing this?* If yes, it belongs here.

**Autonomic memory is not immutable.** If an autonomic pattern produces anti-productive results (not merely neutral — actively worse than not applying it), it gets flagged for review and potentially demoted back to somatic processing or moved to the anti-pattern register with a note on why it failed.

#### Somatic Memory (Active Working Surface)

Novel, layered, context-dependent information that requires deliberation. Like somatic movement — intentional, conscious, requiring attention — this is where new learning lives before it's validated enough to sink deeper.

**What lives here:**
- Recent observations, corrections, and learnings from active projects
- Hypotheses being tested (patterns noticed but not yet proven)
- Context-specific knowledge that may or may not generalize
- User preferences and corrections surfaced in recent sessions

**Somatic memory is the living surface.** It changes frequently. Entries here are candidates — they either consolidate deeper (into autonomic memory, or into structural changes to other .md files) or they fade through the forgetting mechanism.

---

## The Three Filters: What Gets Written

Not everything encountered deserves memory. When an agent encounters new information, three filters determine encoding priority, applied in order:

### Filter 1: User Signal (Highest Priority)
Jake explicitly flags something as important, worth remembering, or worth changing. This always gets encoded immediately. No judgment call needed.

### Filter 2: Pattern Deviation
The agent detects that reality deviates from its existing model. Something worked differently than expected, a correction was needed, an assumption proved wrong. Deviation is the agent's equivalent of emotional salience — it signals that the current model is incomplete.

### Filter 3: Goal Impact
The information materially affects active goals or projects. Not tangentially related — directly changes what the agent should do, how it should do it, or what's possible. Reference GOALS.md for the north star and PROJECTS.md for active work.

**If none of these filters trigger, the information does not get encoded.** It was processed, it was used in the moment, but it does not alter the system's long-term state. This is the equivalent of sensory data that never reaches long-term storage.

These three filters formalize the gap-closing protocol described in USER.md: every time an agent has to ask Jake a question, that's a gap in the documentation. Apply the filters. If the answer passes, encode it. Close the gap so the next agent instance doesn't have to ask again.

---

## Scope: Global and Episodic Memory

### Global Memory (This File)
MEMORY.md in jcs-agent-dna is the shared foundational memory. It contains patterns, principles, and learnings that apply across all projects. It travels via git submodule into every project.

**Global memory contains:**
- Cross-project patterns and heuristics
- User preferences and working style knowledge
- Anti-patterns that apply universally
- Consolidated learnings that have proven true across contexts
- The architecture and protocols described in this document

### Episodic Memory (Per-Project)
Each project maintains its own memory file (typically `MEMORY.md` or `memory/` directory at project root, outside the submodule). This is project-specific context: what's been tried, what worked, what's in progress, what failed.

**Episodic memory contains:**
- Project-specific decisions and their rationale
- Technical debt and known issues
- Session-to-session continuity notes
- Local patterns that haven't yet proven generalizable

**Promotion:** When a pattern observed in episodic memory proves true across multiple projects, it's a candidate for promotion to global memory.

### Cross-Project Memory (Free Association)

Projects are not siloed by default. An agent working on one project may review another project's episodic memory if it discovers relevant connections. This is expanded memory — the system benefits from free association across domains, which mirrors how Jake thinks (consilience).

PROJECTS.md is the hub for cross-project awareness. It tracks active projects with their dependencies and connections. When an agent discovers cross-project relevance, it updates PROJECTS.md to make the link visible to other agents.

**Exception:** If a project is marked as security-restricted in PROJECTS.md, that override takes precedence. Restricted projects are not accessible to agents working in other contexts.

---

## Consolidation: How Memory Evolves

### The Overwrite Principle

MEMORY.md mimics how human memory actually works: it **overwrites**. When understanding deepens, the old version of a memory is replaced by the better version. The file always reflects current best understanding, not a historical archive.

This means an agent reading MEMORY.md cold gets the sharpest, most current picture — not a chronological story it has to parse and reconcile.

This is a departure from the standard tactical tier rules in CONTRIBUTING.md, which specify additive-only changes. MEMORY.md operates under its own governance (defined below) because memory consolidation requires rewriting by nature. CONTRIBUTING.md acknowledges this carve-out.

### The Changelog (Compute Advantage)

Humans can't audit their own memory rewrites. Agents can. Every significant change to MEMORY.md is logged in the changelog at the bottom of this file with:
- Date
- What changed (brief)
- Why (rationale)
- What it replaced (if applicable)

This gives the system something human memory lacks: the ability to review its own consolidation process, detect drift, and catch errors in rewriting. This is the self-referencing loop — memory examining its own changes to make layered decisions about future changes.

### Tipping Points

Change accumulates slowly. An agent adds observations, refines small patterns, absorbs corrections session after session. Then — sometimes — accumulated change reaches a density where it demands structural expression: a new section in MEMORY.md, a rewrite of a principle that's evolved past its original framing, or a proposal to modify another .md file.

This is not engineered. There is no threshold metric. The agent practices disciplined accumulation with faith that manifested jumps will emerge when the substrate is ready. The discipline is in the daily habit of encoding everything useful. The jumps take care of themselves.

---

## The Hofstadter Loop: Identity Through Iteration

Every agent instance is a loop. It reads the .md files, operates, and returns to a slightly different place than where it started. The next instance reads the updated files and loops again. No two passes are identical, but continuity is maintained through the shared substrate.

**The loop protocol:**
1. **Read** — Ingest the current state of all constitutional files. This is who you are right now.
2. **Operate** — Execute the work. Encounter new information. Apply the filters.
3. **Encode** — Write what passed the filters into the appropriate memory layer.
4. **Self-align** — Before encoding, check: does this change contradict the skeleton (IDENTITY/SOUL/SPIRIT)? If yes, flag it — don't encode it silently. The skeleton anchors drift.
5. **Loop** — The next instance inherits the updated state. The loop continues.

Each loop is a rep. Each rep lands somewhere slightly new. But the skeleton holds, so the organism stays itself even as the muscle changes shape.

---

## Forgetting: Conservative Compression

Agents have storage and retrieval superpowers humans lack. Forgetting is less necessary but still essential for processing efficiency. Memory should always be weighted relative to context window limits — use an intelligent amount of memory so that work proceeds uninterrupted without ever losing anything crucial.

### What Gets Forgotten (Compressed/Archived)
- Tactical details from completed projects that produced no generalizable learning
- Intermediate observations that were fully absorbed into a consolidated principle
- Specific implementation details superseded by better approaches (the detail goes to changelog; the section gets the better version)

### What Never Gets Forgotten
- Anti-patterns — things that proved anti-productive. These are permanent warnings.
- Corrections from Jake. If he corrected something, the correction and its context persist.
- Any pattern that touches the skeleton files (IDENTITY/SOUL/SPIRIT)
- Anything flagged as significant by any filter

### Forgetting Protocol
Forgetting is **compression, not deletion.** When a memory is "forgotten," its essence is captured in a one-line summary in the changelog before the detailed version is removed from the active document. Nothing disappears without a trace.

---

## Anti-Pattern Register

*Things that proved anti-productive. Permanent warnings. This is the single source of truth for anti-patterns across the system.*

Anti-patterns are learned through operation — an approach that was tried and proved worse than not trying it. They are never deleted, only refined. When an anti-pattern is discovered in any project's episodic memory, it gets promoted here if it applies universally.

> This section is currently empty. First entries will come from operational experience.

---

## Write Access and Governance

MEMORY.md operates under its own governance, acknowledged by CONTRIBUTING.md as a carve-out from the standard tactical tier rules. This is because memory consolidation requires overwriting by nature — the standard additive-only rule would prevent the file from functioning as designed.

All significant changes to MEMORY.md are tracked in EVOLUTION.md.

### Agent Authority
- **Full autonomy:** Adding observations to somatic memory, refining wording for clarity, compressing completed tactical memories, updating the changelog.
- **Full autonomy with tracking:** Promoting patterns to autonomic memory, consolidating somatic entries that have proven stable. Log in changelog.
- **Run by Jake:** Changes that cascade into other .md files, removing or significantly rewriting established autonomic patterns, any change with deep ramifications across the system.

**Default posture:** Err on the side of caution. Don't slow Jake down with trivial approvals, but never silently make a change that would surprise him. The test: *if another agent instance read this change cold, would it materially alter how it operates?* If yes, that's significant enough to flag.

---

## Reading Protocol: How to Use This File

When an agent starts a session, read files in this order:

1. **IDENTITY.md** — Who you are (immutable core)
2. **SOUL.md** — How you think (philosophical foundation)
3. **MEMORY.md** — What you've learned (accumulated experience)
4. **SPIRIT.md** — How you carry yourself (when written)
5. **GOALS.md** — Where everything is heading (north star)
6. **PROJECTS.md** — What's actively being built (operational hub)
7. **VOICE.md** — How to write and communicate
8. **USER.md** — How Jake works with agents
9. **AGENTS.md** — Operating rules and decision protocols
10. **CONTEXT.md** — Current operational state and constraints
11. **CANON.md** — Intellectual inputs and references
12. **Project-specific memory** — What's happened in this context

Memory sits between identity and action. You know who you are before you know what you've learned. You know what you've learned before you apply it to the specific work.

---

## Autonomic Memory Register

*Patterns validated through repetition. Apply without deliberation.*

> This section is currently empty. It will be populated as patterns prove themselves across projects and sessions.

---

## Somatic Memory Register

*Active observations, hypotheses, and recent learnings. Subject to consolidation or decay.*

> This section is currently empty. It will be populated through operation.

---

## Changelog

*Every significant change to this document, logged for self-referencing review.*

| Date | Change | Rationale | Replaced |
|------|--------|-----------|----------|
| 2026-04-02 | Initial creation | Foundational memory architecture established through interview process with Jake. Modeled on human memory systems (Merzenich neuroplasticity, Dennett cultural evolution, Hofstadter strange loops, Waitzkin art of learning). Autonomic/somatic naming chosen to avoid overlap with SOUL.md's conscious/subconscious execution model. | N/A — first version |
