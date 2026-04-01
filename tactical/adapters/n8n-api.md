# n8n / API Adapter
## How to load dotnd into API-based agents

API-based agents (n8n workflows, custom scripts, Telegram bots)
do not discover files automatically. You load file contents into
the system prompt explicitly.

### Setup

In your n8n workflow or API script, fetch the raw files from GitHub
and concatenate them into the system prompt:

```javascript
// n8n Function node or HTTP Request nodes
const baseUrl = 'https://raw.githubusercontent.com/YOURUSER/dotnd/main';

const files = [
  'constitutional/IDENTITY.md',
  'constitutional/VOICE.md',
  'strategic/SOUL.md',
  'strategic/AGENTS.md',
  'tactical/CONTEXT.md'
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
3. CONTEXT.md (tactical — current state)
4. VOICE.md (constitutional — if generating text output)
5. SOUL.md (strategic — if agent needs operating philosophy)
6. CANON.md (tactical — only if intellectual context is relevant)

### Notes

For the Telegram bot (@dabbod_bot), the system prompt is set in
the n8n workflow that handles incoming messages. Update the workflow
to fetch from the dotnd repo on each invocation, or cache locally
and refresh on a schedule.
