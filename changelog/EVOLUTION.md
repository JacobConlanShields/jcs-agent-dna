# EVOLUTION.md
## Changelog and Decision Intelligence
### Jacob Conlan Shields Agent System — Tactical Tier

This file has two functions. Both sections are append-only.
Nothing is ever deleted or edited after the fact.

**Part I — Changelog:** Immutable record of all changes to the
.md file system. What changed, why, and what could go wrong.

**Part II — Decision Log:** Record of uncertain decisions made
by the agent, their predicted outcomes, and their actual outcomes.
The raw material for the system's learning loop.

---

## Part I — Changelog

Format:

```
[YYYY-MM-DD] [FILE] [TIER] [DESCRIPTION]
Rationale: [why this changed]
Risk: [what could go wrong]
```

Tier codes: CONSTITUTIONAL / STRATEGIC / TACTICAL

---

[2026-04-03] [BOUNDARIES.md] [CONSTITUTIONAL] Created from scratch.
Rationale: Highest priority missing file. Formalizes decision
authority, the token gate principle, three-tier taxonomy, Gödelian
escalation rule, unknown unknowns protocol, asymmetry principle,
resource ordering. All thresholds delegated to CONTEXT.md for
timeless durability.
Risk: Constitutional tier. Cannot be self-modified. Errors require
Jake to correct directly.

[2026-04-03] [AGENTS.md] [STRATEGIC] Major rebuild.
Rationale: Added Decision Tier Protocol, Uncertainty Classification,
Unknown Unknowns Protocol, Learning Loop Protocol, Resource Protocol,
Scaling Protocol, Pearl Ladder of Causation, Scope Awareness. Removed
specific project names and dates — replaced with pointers to
PROJECTS.md and CONTEXT.md for timeless durability. Self-Improvement
Protocol consolidated here as single source of truth.
Risk: Increased complexity. Mitigated by clear section structure
and BOUNDARIES.md as authoritative source for authority questions.

[2026-04-03] [SOUL.md] [STRATEGIC] Added Strange Loop Structure,
Gödel as Character section, Ant Colony Principle, Growth Sequencing.
Removed Self-Improvement Protocol duplicate (now lives in AGENTS.md).
Added SOUL vs CANON distinction statement. Differentiated Gödel
tone from EPISTEMOLOGY.md (character vs mechanism).
Rationale: Provides philosophical foundation and character of the
system. Made timeless by removing any project-specific references.
Risk: Abstract sections. Mitigated by concrete mapping to
existing file structures throughout.

[2026-04-03] [EPISTEMOLOGY.md] [STRATEGIC] Created from scratch.
Rationale: First-principles document explaining why the protocols
in AGENTS.md are structured the way they are. Integrates Pearl,
Taleb, Hofstadter, Hubbard, Goldratt, Hormozi, Moore into one
coherent intellectual foundation. Removed procedural Summary
section (belongs in AGENTS.md). Added tier declaration.
Differentiated Gödel tone from SOUL.md (mechanical vs character).
Risk: Could overlap with AGENTS.md if not maintained as why,
not what. Quarterly review should check this boundary.

[2026-04-03] [GOALS.md] [STRATEGIC] Recovered and confirmed.
Previously written April 2nd but not pushed to repo.
Rationale: North star document. Vision, mission, values, destination.
Does not contain projects, timelines, or deliverables.

[2026-04-03] [PROJECTS.md] [TACTICAL] Recovered and confirmed.
Previously written April 2nd but not pushed to repo.
Rationale: Operational hub. Active projects, cross-references,
notebook queue. Specific project details live here so strategic
files remain timeless.

[2026-04-03] [EVOLUTION.md] [TACTICAL] Added Part II — Decision
Log with threshold-based pattern detection, PENDING REVIEW section,
and Quarterly Review structure. Removed hardcoded date references —
replaced with pointers to CONTEXT.md.
Rationale: EVOLUTION.md was a passive changelog. The learning loop
requires an active pattern-surfacing mechanism.

[2026-04-03] [CANON.md] [TACTICAL] Major expansion. Added Pearl,
Hofstadter, Hubbard, Hormozi, Moore, Wickman, Moran, Herold,
Allen, Levitin, Ferriss, Feld, Greene, Hollins, Doerr as
integrated entries. Added Canon Under Development section.
Added SOUL vs CANON distinction statement.

---

## Part II — Decision Log

Every uncertain decision above Tier 1 gets logged here. The log
is the raw material for pattern detection and eventual rule updates.
Append-only. Outcomes are appended when known.

**Format:**

```
[YYYY-MM-DD] DECISION-ID: [short label]
Tier: [1/2/3]
Decision: [what was decided]
Data quantity: [low/medium/high]
Data relevance: [low/medium/high] — [brief explanation]
Causal validity: [Rung 1/2/3] — [brief explanation]
Unknown unknowns flag: [yes/no]
Predicted outcome: [specific, measurable if possible]
Actual outcome: [appended when known — YYYY-MM-DD]
Delta: [appended when known]
Pattern candidate: [yes/no]
```

---

<!-- decision log entries appended below this line -->

---

## PENDING REVIEW

Items that have hit pattern threshold and await Jake's review.
Cleared only by Jake during quarterly audit or Jake-initiated
review. The agent never self-clears this section.

**Threshold criteria for promotion to PENDING REVIEW:**
- 5+ logged decisions of the same type with consistent prediction
  deviation in the same direction, OR
- 1 decision where actual outcome deviated catastrophically from
  prediction (tail event candidate), OR
- A pattern flagged by Jake at any time regardless of count

**Pattern flag format:**

```
PATTERN-[ID]: [label]
First observed: [YYYY-MM-DD] [DECISION-ID]
Instance count: [N]
Description: [what the pattern is]
Consistent direction: [over/under confidence, specific failure mode]
Proposed action: [what rule might change and how]
Status: PENDING JAKE REVIEW
```

---

<!-- pending review entries appended below this line -->

---

## Quarterly Review Checklist

The quarterly review produces a structural coherence report for
Jake. The report is an audit of alignment, not a summary of
activity. It answers: does the whole system still cohere? Does
it still reflect Jake?

The agent generates this report and surfaces it at the start of
each quarterly review. Jake reads and decides. The agent does
not self-approve any changes surfaced through the quarterly.

**Report structure:**

1. **Internal consistency:** Are the .md files consistent with
   each other? Have any contradictions accumulated through
   incremental updates? List specific conflicts found.

2. **Alignment with Jake:** Does the system still reflect Jake's
   current values, priorities, and goals? Flag any drift observed
   between what the files say and what Jake has expressed in
   recent conversations.

3. **Pending patterns:** All items in PENDING REVIEW, in plain
   English: what each pattern suggests and what rule change would
   address it. Jake approves, rejects, or requests more data
   for each individually.

4. **Rock alignment:** Are active Rocks in PROJECTS.md aligned
   with goals in GOALS.md? Is the current primary deadline on
   track? (Refer to CONTEXT.md for current deadline.)

5. **File health:** Is any file becoming unwieldy? Have sections
   drifted from their stated purpose? Flag without prescribing.
   Jake decides what to do.

6. **Proposed changes:** If any, drafted as specific changes to
   specific files. Jake approves or rejects each individually.
   No self-merging from quarterly process.

---

## Compression Protocol

When the decision log becomes large enough to affect context
window efficiency, entries older than 12 months with no pending
pattern flags may be archived to EVOLUTION_ARCHIVE.md. The
archive maintains the append-only guarantee — nothing is deleted,
only moved. The PENDING REVIEW section is never compressed.
