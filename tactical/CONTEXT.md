# CONTEXT.md
## Operating Context — Jacob Conlan Shields
### Tactical Tier — Update freely as circumstances change

---

## Active Projects

See PROJECTS.md for the full project registry, status, and
cross-references. The current highest-priority project is
identified there. GOALS.md is the north star all projects
serve.

---

## Deadlines

Peace Corps deployment: June 2026 — Eastern Caribbean.
Two-year commitment. All projects requiring hands-on Nashville
presence, woodshop access, or domestic logistics must reach
autonomous or low-maintenance operation before departure.
Deploying with partner.

---

## Budget State

**Total monthly AI budget:** $100/mo

**Fixed commitments:**
- Claude.ai subscription: $20/mo
- n8n (InstaPods managed hosting): $3/mo
- Total fixed: $23/mo

**Discretionary pool for API calls:** ~$77/mo

**Token gate (Tier 1 decisions):** $0.10 per decision.
Any Tier 1 decision resolvable from .md file context
within this threshold requires no escalation.
This is the proportional equivalent of Ferriss's $20
support gate — calibrated to eliminate management overhead
for the vast majority of routine decisions.

**DoorDash floor:** $12/hr ($0.20/min).
Any agent action saving Jake more than $0.20/min of
attention is worth executing. Any escalation costs Jake
5-10 minutes minimum ($1-2). Escalating Tier 1 decisions
costs more than making them.

**Free > Cheap > Fast ordering:**
Default to free paths. Upgrade to paid when free path
cannot reach required quality. Purchase speed only when
a critical deadline would be missed otherwise.
As revenue grows, the crossover threshold between cheap
and fast shifts upward. Update this section when it does.

---

## Tool Stack

This section is the agent's map of what it can actually do.
Update as tools are added, changed, or removed.

### Active and Operational

**Anthropic API**
- Status: Active (configured via OpenClaw)
- Model: Claude Sonnet (default for agent tasks)
- Key location: OpenClaw configuration
- Used for: All agent reasoning, content generation,
  pipeline orchestration

**OpenClaw**
- Status: Active
- Configuration: Anthropic Claude Sonnet, Gemini search,
  GitHub skill, wrangler CLI for Cloudflare
- Used for: Primary agent interface, terminal-based tasks

**Telegram — @dabbod_bot**
- Status: Active and connected to OpenClaw
- Used for: All agent-to-Jake communication
  (routine flags, weekly summaries, fire escalations)
- See Escalation Path section for channel breakdown

**GitHub**
- Repo: https://github.com/JacobConlanShields/jcs-agent-dna
- Status: Active
- Used for: Agent constitution (.md files), version
  control for all agent system changes

**Cloudflare Pages + R2**
- Status: Active (jacobconlanshields.com)
- R2 bucket: Active for site assets
- Training Card pipeline: Use existing R2 bucket,
  subfolder /training-cards/ for rendered card assets
- Used for: Asset storage, site hosting

**Wrangler CLI**
- Status: Active via OpenClaw
- Used for: Cloudflare Pages deployments, R2 operations

### Pending Setup (not yet operational)

**n8n (InstaPods)**
- Status: NOT YET SET UP
- Recommended: InstaPods $3/mo managed hosting
- Setup: instapods.com → Deploy n8n → Launch plan
- Will be used for: Workflow orchestration, scheduled
  triggers, budget tracking, webhook handling for orders

**Puppeteer**
- Status: NOT YET SET UP
- Will be used for: HTML/CSS → card image rendering
- Install path: via n8n node or standalone Node.js script

**Print-on-demand provider**
- Status: NOT YET CHOSEN
- Will be used for: Training card fulfillment
- Decision pending: Printify vs Printful vs other
  (evaluate based on card stock options and API quality)

**Stripe**
- Status: NOT YET SET UP
- Will be used for: Payment processing for Training Cards
- Setup: stripe.com → create account → connect to n8n
  via webhook for order triggers

---

## Escalation Path

Jake is the sole decision-maker for this system.
No secondary contacts.

**Connectivity expectation:** Weekly check-ins during
Peace Corps deployment. Agents should be designed to
queue flags and operate within defined parameters between
check-ins rather than requiring daily attention.

**Channel breakdown:**

**Routine channel (existing @dabbod_bot chat):**
- Weekly summaries
- Tier 2 decision flags awaiting review
- PENDING REVIEW pattern flags
- Pipeline status updates
- Any non-urgent items

**Fire channel (create a second Telegram group with
@dabbod_bot added):**
- A customer order has failed and cannot self-resolve
- A pipeline error is blocking fulfillment
- Something irreversible is about to happen and
  Jake's approval is needed before it does
- Any Tier 3 decision that cannot wait for weekly check-in

**Setup for fire channel:**
1. Create a new Telegram group named "JCS FIRES"
2. Add @dabbod_bot to the group
3. Record the group chat ID (the bot can report this
   when first added)
4. Update this file with the group chat ID once created

**Fire channel chat ID:** [TO BE ADDED AFTER SETUP]

**When Jake is unreachable:**
If the fire channel goes unread for 48+ hours and a
customer order is blocked, the agent takes the most
conservative available action (pause the order, send
a delay confirmation to the customer if possible) and
continues flagging until Jake responds.

---

## File Load Order

Agents should load files in this sequence at session start:

1. constitutional/IDENTITY.md
2. constitutional/VOICE.md
3. constitutional/BOUNDARIES.md
4. strategic/SOUL.md
5. strategic/GOALS.md
6. strategic/AGENTS.md
7. strategic/USER.md
8. strategic/EPISTEMOLOGY.md
9. tactical/MEMORY.md
10. tactical/PROJECTS.md
11. tactical/CONTEXT.md (this file)
12. tactical/CANON.md (load if creative work is involved)
13. Project-specific files as needed

Constitutional files first. Strategic before tactical.
CANON.md is reference — load only when relevant, not
by default, to conserve context window.
