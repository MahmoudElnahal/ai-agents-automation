# 🤖 AI Agents & Intelligent Automation

Two production-style AI Agent projects built on two different automation platforms — and chained together end to end.

```
Google Sheets  →  n8n AI Agent  →  Email  →  UiPath AI Agent  →  Report  →  Google Drive
```

An email written by one agent, read and triaged by another. No human in the loop.

---

## Projects

### [01 · UiPath Email Triage Agent](./01-uipath-email-triage)

An autonomous UiPath agent that reads an inbox, classifies each email by category and priority, extracts action items and deadlines, drafts a reply, and files a structured report to Google Drive.

`UiPath Agent Builder` · `Studio Web` · `Integration Service` · `Gmail` · `Google Drive`

### [02 · n8n Digital Agriculture Agent](./02-n8n-agriculture-agent)

An n8n workflow that pulls farm sensor data, aggregates it in code, hands a clean summary to an AI decision agent, and routes a critical alert or a routine management report by email.

`n8n` · `LangChain Agent` · `GPT-4o-mini` · `Google Sheets` · `Gmail`

---

## What These Projects Demonstrate

| Principle | How it shows up |
|---|---|
| **Structured output over prose** | Both agents return typed JSON the workflow can branch on — not paragraphs |
| **Deterministic classification** | `temperature = 0` everywhere, so the same input always yields the same decision |
| **Aggregate before you prompt** | Raw rows are summarized in code first — fewer tokens, sharper answers |
| **Graceful degradation** | A malformed AI response falls back to a computed result instead of crashing the run |
| **Agentic tool use** | The agent decides when to call its tools; the workflow does not script the call |

---

## Demo

📹 [Watch the 5-minute walkthrough](#) · *link coming soon*

---

## Repository Layout

```
.
├── 01-uipath-email-triage/
│   ├── Solution.uis                 # importable UiPath solution
│   └── source/                      # agent.json, Main.xaml, tool + eval definitions
├── 02-n8n-agriculture-agent/
│   ├── workflow.json                # importable n8n workflow (sanitized)
│   └── sample-data/                 # 120 sensor records, CSV + XLSX
├── docs/
│   ├── Smart-Email-Triage-Agent-GUIDE-AR.md   # full build guide (Arabic)
│   └── Video-Script-5min.md                   # demo script
└── screenshots/
```

---

## Author

**Mahmoud Elnahal** — RPA & Intelligent Automation
Built during RPA training with Digital HUB (D-HUB) and Orange Digital Center Egypt.
