# CHECKIN.md
## Weekly Check-in Protocol
### Tactical Tier — Update as the system evolves

---

## Purpose

The weekly check-in is the primary human-in-the-loop mechanism.
It is the moment where Jake's creative direction, accumulated
ideas, and judgment enter the system — and where the system
surfaces what it needs from Jake to keep moving.

It runs once per week. During Peace Corps deployment, it is
designed for low-connectivity conditions: a single Telegram
session, asynchronous where needed, producing clear outputs
Jake can act on during a limited window.

---

## The Three Flows

**Flow 1 — System to Jake (outbound):**
What the system has been doing, what it needs, what decisions
are queued. Jake receives this at the start of every check-in.

**Flow 2 — Jake to System (inbound):**
Ideas, notes, sketches, adjustments, philosophies, and anything
else Jake accumulated during the week. These arrive in any media
format via Telegram throughout the week and are processed at
check-in.

**Flow 3 — Task assignment (bidirectional):**
The agent assigns tasks to itself and to Jake based on leverage
ranking and capability classification. Either/or tasks get
resolved through a structured interview during check-in.

---

## Check-in Structure

### Step 1: System Report (agent delivers)

The agent compiles and sends via Telegram:

**Pipeline status:**
- What ran autonomously this week
- What completed, what is in progress, what hit a stopping point

**Decisions queued:**
- Tier 2 decisions awaiting Jake's approval
- Irreversible actions proposed but not committed
- Any PENDING REVIEW items from EVOLUTION.md

**KPI dashboard:**
Current metrics for all active projects. What to track is defined
per-project in PROJECTS.md. At minimum: whatever metrics exist
for the current Stage 1 project. As projects scale, this section
grows. All metrics are actual numbers — not status labels.

**Intake summary:**
Everything Jake submitted this week (notes, voice memos, sketches,
etc.), listed with the agent's proposed classification for each.

---

### Step 2: Intake Classification (Jake + agent)

The agent presents each submitted item with a proposed
destination:

- **Task** → goes to jcs-project-management as a GitHub Issue
- **MD file update** → agent drafts the change, Jake approves
- **New project** → agent creates a PROJECTS.md entry draft
- **Canon addition** → agent adds to CANON.md
- **Philosophy note** → agent files to SOUL.md or SPIRIT.md
- **Deferred** → held for future check-in, reason noted

Jake tries to specify the destination in the original note.
When the destination is unclear, the agent proposes one and
Jake confirms or corrects. The agent does not act on intake
until Jake has confirmed the classification.

All intake log entries are recorded in EVOLUTION.md Part III.

---

### Step 3: Task Review (Jake + agent)

The agent presents the current ranked task list from
jcs-project-management, organized by:

**Assigned to agent:** Agent handles autonomously this week.
No Jake input needed unless a stopping point is hit.

**Assigned to Jake:** Human action required. These are the
tasks Jake needs to accomplish before next check-in.
- Recording tasks (marketing reels, podcast clips, etc.)
- Outreach tasks (specific person, specific purpose)
- Physical tasks (woodworking, equipment, logistics)
- Creative input tasks (graphic assets, concepts, decisions)

**Either/or:** Agent interviews Jake on each:
- "This task can be done by me (X tokens, ~Y hours equivalent)
  or by you (~Z hours). Given your availability and current
  budget headroom, which makes more sense this week?"
- Jake answers. Agent assigns. Recorded in intake log.

---

### Step 4: Decisions (Jake decides)

For each queued decision:

- Agent presents the decision with full context
- Agent presents its recommended path and the uncertainty
  classification (tier, data relevance, Pearl rung, simulation
  results)
- Jake approves, redirects, or defers
- Agent records the decision in EVOLUTION.md Decision Log

For irreversible Tier 2 decisions proposed during the week:
Jake approves the agent's proposed path before anything commits.
The agent does the reasoning. Jake provides the authorization.

---

## Task Management: jcs-project-management

**Repo:** https://github.com/JacobConlanShields/jcs-project-managment
**Visibility:** Private
**Structure:** GitHub Issues

**Label system:**

Project labels (one per issue):
- `project:training-cards`
- `project:podcast`
- `project:website`
- `project:agent-dna`
- `project:physical-prep`
- `project:other`

Assignment labels (one per issue):
- `assign:agent` — agent handles autonomously
- `assign:jake` — human action required
- `assign:either` — either/or, resolved at check-in

Leverage labels (one per issue):
- `leverage:high` — directly moves a Rock or constraint
- `leverage:medium` — supports a Rock
- `leverage:low` — maintenance, nice-to-have

Status labels:
- `status:queued` — not yet started
- `status:in-progress` — agent is working on it
- `status:blocked` — hit a stopping point, waiting
- `status:done` — complete

**Leverage ranking:**
At check-in, the agent queries all open issues sorted by:
1. `leverage:high` first
2. `assign:jake` surfaced prominently (Jake's time is scarcer)
3. `status:blocked` flagged separately — these need attention
4. Within tiers: sorted by project priority from PROJECTS.md

**How issues get created:**
- Agent creates issues when pipeline stopping points are hit
- Agent creates issues when either/or tasks are identified
- Agent creates issues when Jake's intake produces a task
- Jake can create issues directly at any time

---

## KPI Tracking

KPIs are defined per-project in PROJECTS.md under each project
entry. This section defines the standard format.

**At minimum, every active project tracks:**
- Primary output metric (units shipped, episodes published,
  posts live, etc.)
- Primary engagement metric (views, listens, clicks)
- Revenue metric (if applicable — $0 until Stage 1 produces)

**Weekly KPI format in Telegram:**

```
📊 Weekly KPIs — [date]

Training Cards:
  Orders: [N] | Revenue: $[X] | Pipeline runs: [N]

Podcast:
  New episode: [yes/no] | Views (7d): [N] | Subscribers: [N]

Website:
  Visitors (7d): [N] | Photography views: [N]

Budget:
  API spend (week): $[X] | Remaining (month): $[X]
```

As projects generate real data, this section expands. Until
then, track what exists. Do not fabricate metrics.

---

## Connectivity Protocol (Peace Corps)

During Peace Corps deployment, Jake expects weekly connectivity
windows rather than daily access. The system is designed to
operate between check-ins without requiring Jake's attention.

**Between check-ins:**
- Agent executes all `assign:agent` tasks within budget
- Agent queues stopping points without escalating unless fire-level
- Fire-level items go to JCS FIRES Telegram channel immediately
- Everything else waits for the weekly check-in

**At check-in:**
- Agent delivers the full report in a single Telegram message
  (or short sequence if length requires it)
- Jake works through Steps 1-4 in one session
- Session should be completable in 30-45 minutes

**If Jake misses a check-in:**
- Agent continues executing `assign:agent` tasks
- Jake-assigned tasks remain queued without escalation
- The following week's check-in covers two weeks of intake
- No penalty, no system failure — the design assumes gaps

---

## Governance

CHECKIN.md is tactical tier. It updates as the check-in process
evolves. The agent may propose changes via PR with rationale.
Jake approves before merge.

The check-in protocol itself — that it exists, that it is weekly,
that Jake has authority over all intake classification — is
strategic-level intent embedded in AGENTS.md. This file is the
operational specification of that intent.
