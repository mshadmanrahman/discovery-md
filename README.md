<p align="center">
  <h1 align="center">discovery.md</h1>
  <p align="center">
    AI-powered product discovery for PMs who don't have a UX researcher.
  </p>
  <p align="center">
    <a href="#install">Install</a> &middot;
    <a href="#how-it-works">How It Works</a> &middot;
    <a href="#example">Example</a> &middot;
    <a href="#why">Why</a>
  </p>
</p>

---

**Drop it into your project. Run `/product-discovery`. Your AI becomes a discovery copilot.**

It walks you through framing problems, planning interviews, synthesizing findings, and packaging evidence for stakeholders. Built on Teresa Torres's Opportunity Solution Tree, The Mom Test, and 14 years of product discovery practice.

No UX researcher required. No PhD in research methods. Just you, your AI coding tool, and real customer problems to solve.

---

## The Problem

You know you should talk to customers before building. But:

- You don't have a UX researcher on your team
- You don't know what questions to ask (or you ask the wrong ones)
- Even when you DO interviews, you don't know how to turn notes into decisions
- Your stakeholders want evidence, not gut feelings

**discovery.md turns your AI into a discovery copilot that guides you through the entire process and produces artifacts you can actually share with your team.**

---

## Install

### Claude Code

```bash
# Copy the skill into your project
cp -r product-discovery/ your-project/.claude/skills/product-discovery/

# Or just copy SKILL.md for the lightweight version
cp product-discovery/SKILL.md your-project/.claude/skills/product-discovery/SKILL.md
```

Then run:
```
/product-discovery
```

### Cursor / Windsurf / Other AI Editors

Copy `SKILL.md` into your project's AI rules directory (`.cursor/rules/`, `.windsurfrules/`, etc.). The skill works with any AI assistant that reads markdown instructions.

### Manual (No AI Tool)

The templates in `templates/` work standalone. Copy them, fill them in, and you have a structured discovery process.

---

## How It Works

Four commands. Each one produces a real, shareable markdown artifact.

| Command | What happens | Output |
|---|---|---|
| `/product-discovery` | Guided problem framing. Starts with a braindump, then structures it. | `discovery/{name}/brief.md` |
| `/product-discovery interview` | Generates Mom Test interview guide with bias warnings. | `discovery/{name}/interview-guide.md` |
| `/product-discovery synthesize` | Paste your raw notes. Get themes, pain ranking, opportunity tree. | `discovery/{name}/synthesis.md` |
| `/product-discovery package` | Turns insights into a stakeholder one-pager with GO/PIVOT/KILL recommendation. | `discovery/{name}/one-pager.md` |

Run them in sequence for a full discovery cycle, or individually when you just need one piece.

### What Makes It Different

**It's a copilot, not a template.** It doesn't hand you a blank form. It asks you questions, pushes back on bad assumptions, and guides you through the thinking.

**It starts with the mess.** First question is always: "What's the messy thinking you haven't structured yet? Dump it." Structure comes after clarity.

**It's opinionated.** "You're describing a solution, not a problem. Let's back up." This skill has 14 years of product discovery practice baked in. It tells you when you're doing it wrong.

**Every output is portable.** Markdown files that work in GitHub, Notion, Confluence, Linear, Jira, or plain email. Zero lock-in.

---

## Example

**Scenario:** You're a PM investigating why 35% of teams churn in the first 90 days.

### Before discovery.md

> "I think we need better integrations. Our Slack integration sucks. Let's build a Jira importer."

Gut feeling. No evidence. Building the wrong thing.

### After discovery.md

```
discovery/day90-churn/
  brief.md              # Structured hypothesis: "Champions burn out at week 6-8
                        #   because the tool doesn't embed into Slack workflows"
  interview-guide.md    # 7 Mom Test questions testing 3 critical assumptions
  synthesis.md          # 7 interviews synthesized: Slack gap (6/7), champion
                        #   burnout (5/7), week-3 customization wall (4/7)
  one-pager.md          # GO recommendation with evidence. Stakeholder-ready.
```

> "6 of 7 project leads said the same thing: if updates don't flow into Slack, their team reverts to the old tool by week 6. Our top opportunity is workflow embedding, not feature gaps."

Evidence-backed. Stakeholder-ready. Built confidence to say "no" to the Jira importer.

[See the full worked example &rarr;](examples/sample-cycle.md)

---

## The Workflow

```
Week 1                          Week 2                          Week 3
                                                                
  /product-discovery              /product-discovery interview     /product-discovery synthesize
  "What problem are we           "Here are 7 questions that       "Here are the 3 biggest
   actually solving?"              test your assumptions"           pain points from 7
                                                                    interviews"
       |                               |                               |
       v                               v                               v
  brief.md                        interview-guide.md              synthesis.md
  - Problem hypothesis            - Mom Test questions             - Themes + quotes
  - Research questions            - Bias warnings                  - Pain ranking
  - Success criteria              - Saturation tracker             - Opportunity tree
                                                                       |
                                                                       v
                                                                  /product-discovery package
                                                                  "Here's a one-pager your VP
                                                                   can act on"
                                                                       |
                                                                       v
                                                                  one-pager.md
                                                                  - Evidence summary
                                                                  - GO / PIVOT / KILL
                                                                  - TLDR for Slack
```

---

## What's Inside

```
product-discovery/
  SKILL.md                  # The brain. 4 interactive modes with conversation flows.
  README.md                 # You're reading it.
  LICENSE                   # MIT. Use it however you want.
  templates/
    brief.md                # Discovery brief template
    interview-guide.md      # Interview guide with Mom Test structure
    synthesis.md            # Synthesis with opportunity tree
    one-pager.md            # Stakeholder one-pager
  examples/
    sample-cycle.md         # Full worked example (B2B SaaS churn)
```

---

## Frameworks Used

discovery.md operationalizes the best of product discovery thinking:

| Framework | Author | How It's Used |
|---|---|---|
| **Opportunity Solution Tree** | Teresa Torres | Backbone of the synthesis. Maps pain points to opportunities. |
| **The Mom Test** | Rob Fitzpatrick | Interview questions focused on past behavior, not hypotheticals. |
| **Continuous Discovery** | Teresa Torres | Built for ongoing practice, not one-time research projects. |
| **Four Risks** | Marty Cagan | Value, usability, feasibility, viability as validation lenses. |
| **Lean Customer Development** | Cindy Alvarez | Minimum viable research for lean teams. |

---

## Why

Most product teams skip discovery. Not because they don't believe in it, but because:

1. **They don't have a researcher.** Discovery feels like someone else's job.
2. **The methodology is intimidating.** Teresa Torres's book is 300 pages. Who has time?
3. **They don't know where to start.** So they start building instead.
4. **They can't connect insights to decisions.** Notes sit in a doc nobody reads.

discovery.md makes product discovery as accessible as writing a README. One command. Real artifacts. Evidence your team can act on.

---

## Who Is This For

- **Solo PMs** at startups who ARE the product team
- **Founders** who know they should validate before building
- **Product teams** without a dedicated UX researcher
- **Junior PMs** learning the craft (this is the $2,000 workshop in a markdown file)
- **Anyone** who's been told "talk to your users" but doesn't know how

## Who Is This NOT For

- **UX researchers** who already have a research practice (you don't need this)
- **Teams with a full research org** (use your existing tools and processes)
- **People looking for a survey tool** (this is for qualitative discovery, not quantitative data collection)

---

## Built By

**Shadman Rahman** -- Product leader, builder, and recovering "just ship it" PM.

14 years of product work across South Asia and Europe. MSc in Human-Computer Interaction (Uppsala University). Designed the onboarding that brought 35 million people online for the first time. Now building tools that make product craft accessible to everyone.

- [LinkedIn](https://linkedin.com/in/mshadmanrahman)
- [Substack](https://shadmanrahman.substack.com)
- [GitHub](https://github.com/mshadmanrahman)

---

## Contributing

Found a gap in the workflow? Have a better interview question? Open a PR or issue. This is MIT-licensed and community-driven.

**Especially welcome:**
- Industry-specific examples (fintech, healthcare, B2C, marketplace)
- Translations
- Integration guides for other AI tools (Cursor, Windsurf, Cline, Aider)

---

## Related Projects

- [Claude Code Guide](https://claudecodeguide.dev) -- Learn Claude Code from scratch (if you're new to AI coding tools)
- [Ceremonies](https://ceremonies.dev) -- Free, open-source agile ceremonies toolkit

---

## License

MIT. Use it, fork it, sell it, teach with it. Just build better products.
