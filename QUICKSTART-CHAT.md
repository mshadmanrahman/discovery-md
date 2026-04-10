# Quickstart: Use discovery.md in Claude.ai, ChatGPT, or Any Chat Interface

No terminal. No installation. Just paste and go.

---

## Option 1: Claude.ai (Recommended)

Claude Projects give you persistent instructions, so the discovery copilot stays active across conversations.

### Setup (2 minutes)

1. Go to [claude.ai](https://claude.ai) and create a **new Project**
2. Name it something like "Product Discovery"
3. Click **"Set project instructions"** and paste the entire contents of [`system-prompt.md`](system-prompt.md)
4. Optionally, upload the template files from `templates/` as project knowledge

### Use it

Start a new conversation in the project and say:

> "I want to start product discovery for [your problem area]"

The copilot will guide you through the full cycle:
- **Frame** the problem (starts with a braindump)
- **Plan** interviews (Mom Test questions, bias warnings)
- **Synthesize** findings (raw notes in, opportunity tree out)
- **Package** evidence (stakeholder one-pager with GO / PIVOT / KILL)

### Tips
- Each phase works independently. You can say "I just need an interview guide" and skip straight there.
- Paste your raw interview notes directly into the chat for synthesis. Messy is fine.
- Ask it to export any artifact as a shareable markdown doc.

---

## Option 2: ChatGPT

### Setup (2 minutes)

1. Go to [chatgpt.com](https://chatgpt.com)
2. Start a new conversation
3. Paste the contents of [`system-prompt.md`](system-prompt.md) as your first message, prefixed with:

> "Use the following as your instructions for this conversation. After reading them, confirm you're ready and wait for me to start."

### Or: Create a Custom GPT

1. Go to **Explore GPTs > Create**
2. In the **Instructions** field, paste the contents of `system-prompt.md`
3. Name it "Discovery Copilot"
4. Save and use it anytime

### Tips
- ChatGPT doesn't have persistent project instructions in free tier, so you may need to re-paste for new conversations.
- Custom GPTs (Plus/Team plans) solve this -- the instructions persist.

---

## Option 3: Gemini, Copilot, or Any Other AI Chat

The system prompt works with any AI assistant that follows instructions well.

1. Start a new conversation
2. Paste the contents of `system-prompt.md` as your first message
3. Say "I want to start product discovery"

Quality will vary by model. Claude and GPT-4 class models work best for the conversational push-back that makes this tool valuable.

---

## What You Get

Each phase produces a structured artifact you can copy-paste into your team's tools:

| Phase | What you say | What you get |
|---|---|---|
| Frame | "I want to explore [problem]" | Discovery brief with hypothesis + research questions |
| Interview | "Help me plan interviews" | Mom Test interview guide with bias warnings |
| Synthesize | "Here are my notes: [paste]" | Themes, pain ranking, opportunity tree |
| Package | "Help me package this for stakeholders" | One-pager with GO/PIVOT/KILL recommendation |

All outputs are markdown. Works in Notion, Confluence, Google Docs, Linear, Jira, email, or anywhere else.

---

## Differences from the CLI Version

| | Chat version | CLI version (Claude Code) |
|---|---|---|
| Setup | Paste system prompt | Install as skill |
| File output | Copy-paste from chat | Auto-saves to project |
| Persistence | Per-project (Claude.ai) or per-session | Permanent in project |
| Quality | Same discovery logic | Same discovery logic |

The discovery methodology is identical. The only difference is how artifacts are saved.

---

## Next Steps

- **Want the full CLI experience?** See the [main README](README.md) for Claude Code / Cursor / Windsurf setup.
- **New to AI coding tools?** Check out the [Claude Code Guide](https://claudecodeguide.dev) to get started.
- **Questions?** Open an [issue](https://github.com/mshadmanrahman/discovery-md/issues) or reach out on [LinkedIn](https://linkedin.com/in/mshadmanrahman).
