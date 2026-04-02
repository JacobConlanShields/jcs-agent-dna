# n8n / API Adapter
## How to load jcs-agent-dna into API-based agents

API-based agents (n8n workflows, custom scripts, Telegram bots)
do not discover files automatically. You load file contents into
the system prompt explicitly.

### Setup

In your n8n workflow or API script, fetch the raw files from GitHub
and concatenate them into the system prompt:

```javascript
// n8n Function node or HTTP Request nodes
const baseUrl = 'https://raw.githubusercontent.com/YOURUSER/jcs-agent-dna/main';

const files = [
  'constitutional/IDENTITY.md',
  'constitutional/VOICE.md',
  'strategic/SOUL.md',
  'tactical/MEMORY.md',
  'strategic/SPIRIT.md',
  'strategic/GOALS.md',
  'strategic/AGENTS.md',
  'strategic/USER.md',
  'tactical/PROJECTS.md',
  'tactical/CONTEXT.md',
  'tactical/CANON.md'
];

let systemPrompt = '';
for (const file of files) {
  const response = await fetch(`${baseUrl}/${file}`);
  systemPrompt += await response.text() + '\n\n---\n\n';
}

// Use systemPrompt as the system message in your API call
```

### Token budget

Loading all files may exceed token limits on some models. Priority
order if you must trim:

1. IDENTITY.md (constitutional — always load)
2. AGENTS.md (strategic — operating rules)
3. PROJECTS.md (tactical — current project state)
4. CONTEXT.md (tactical — constraints and tool stack)
5. VOICE.md (constitutional — if generating text output)
6. SOUL.md (strategic — if agent needs operating philosophy)
7. MEMORY.md (tactical — accumulated memory and anti-patterns)
8. GOALS.md (strategic — if agent needs north star context)
9. CANON.md (tactical — only if intellectual context is relevant)

### Notes

For the Telegram bot (@dabbod_bot), the system prompt is set in
the n8n workflow that handles incoming messages. Update the workflow
to fetch from the jcs-agent-dna repo on each invocation, or cache locally
and refresh on a schedule.
