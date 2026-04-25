# InterviewSync — The Panel Orchestrator

> An agentic AI system that orchestrates interview "Super Days" — coordinating panels, handling real-time disruptions (no-shows, delays, swaps), and keeping HR, interviewers, and candidates in sync.

[![Status](https://img.shields.io/badge/status-Hackathon%20Submission-blue)]()
[![Event](https://img.shields.io/badge/built%20for-AgenticX%20Hackathon-7C3AED)]()
[![Workflow](https://img.shields.io/badge/backend-n8n-EA4B71)]()
[![License](https://img.shields.io/badge/license-MIT-lightgrey)]()

---

## 🎯 The Problem

At high-growth startups like TechScale, HR leads run "Super Days" with **8+ candidates** and **12+ interviewers on a panel**. The day is a minefield of live disruptions:

- 🚫 Interviewer no-shows or last-minute delays
- 🔄 Panel swaps required mid-schedule
- ⏰ Candidate arrival delays cascading across slots
- 📞 Manual coordination across Slack, calendar, email
- 🧠 Cognitive overload — HR becomes a human dispatcher

The result: **late decisions, frustrated candidates, and missed hires.**

---

## 💡 The Solution

**InterviewSync** is an AI-powered orchestration layer that:

1. 📅 **Ingests** the Super Day schedule (candidates × interviewers × slots)
2. 👀 **Monitors** real-time signals (arrivals, delays, no-shows)
3. 🤖 **Decides** — reschedule, swap, re-slot, or escalate using agentic logic
4. 📣 **Notifies** all stakeholders instantly across channels
5. 📊 **Logs** every decision for audit and post-day analytics

---

## 🎬 Live Artifacts

| Artifact | Preview |
|---|---|
| **Main UI** | [interviewsync.html](./interviewsync.html) |
| **Alternate UI** | [interivewsyncUI.html](./interivewsyncUI.html) |
| **Integrated Build** | [Final/interviewsync_integrated.html](./Final/interviewsync_integrated.html) |
| **HR Persona — Aditi** | [aditi_hr_persona.html](./aditi_hr_persona.html) |
| **n8n Node Guide** | [InterviewSync_n8n_NodeGuide.html](./InterviewSync_n8n_NodeGuide.html) |

---

## 🗺️ Flow Diagrams

### ✅ Happy Path
![Happy Path](./InterviewSync%20Happy%20Path.png)

### ⚠️ Disruption Handling
![Disruption Flow](./InterviewSync%20Disruption%20Handling%20Flow.png)

---

## ⚙️ n8n Workflows

| Workflow | File |
|---|---|
| **Complete Workflow (Happy Path + Edge Cases)** | [`InterviewSync - Complete Workflow (Happy Path + All Edge Cases) (1).json`](./InterviewSync%20-%20Complete%20Workflow%20%28Happy%20Path%20%2B%20All%20Edge%20Cases%29%20%281%29.json) |
| **Panel Orchestrator** | [`InterviewSync_ Panel Orchestrator.json`](./InterviewSync_%20Panel%20Orchestrator.json) |
| **Panel Orchestration (alt)** | [`The Panel Orchestration.json`](./The%20Panel%20Orchestration.json) |
| **Complete Workflow (alt)** | [`interviewsync_complete_workflow.json`](./interviewsync_complete_workflow.json) |

> 💡 **To try it yourself:** Import the JSON into a self-hosted or cloud n8n instance via *Workflows → Import from File*.

---

## 👤 Target Persona — Aditi Sharma

| Attribute | Detail |
|---|---|
| **Role** | HR Lead @ TechScale (Series B, Bengaluru) |
| **Experience** | 5 years in HR operations |
| **Responsibilities** | Super Day Coordinator, People Ops |
| **Scale** | 8 candidates · 12 interviewers · 1 day |
| **Biggest pain** | Real-time disruption handling |

See the full interactive persona: [aditi_hr_persona.html](./aditi_hr_persona.html)

---

## 🏗️ Architecture

┌──────────────────┐      ┌───────────────────────┐      ┌────────────────┐
│  HR Dashboard    │ ◀──▶ │   n8n Orchestrator    │ ◀──▶ │   LLM Agent    │
│  (HTML UI)       │      │ (Panel Orchestrator)  │      │ (Decisions)    │
└──────────────────┘      └───────────────────────┘      └────────────────┘
▲                          │      │                      │
│                          ▼      ▼                      ▼
│               ┌──────────────┐  ┌─────────────┐  ┌─────────────┐
│               │  Scheduler   │  │ Notifier    │  │ Disruption  │
│               │ (Calendar)   │  │ (Slack/Email│  │ Detector    │
│               └──────────────┘  │  /SMS)      │  └─────────────┘
│                                 └─────────────┘
└───────────────── Real-time status updates ───────────┘



---

## 🧠 Agent Logic — How Disruptions Are Handled

| Event | Agent Decision |
|---|---|
| Interviewer 5+ min late | Notify HR + attempt silent reslot |
| Interviewer no-show | Find next-best interviewer with matching skills + availability |
| Candidate delayed | Ripple-shift subsequent slots, notify affected interviewers |
| Panel swap requested | Re-balance load across remaining panelists |
| Cascading conflicts | Escalate to HR with ranked resolution options |

Full edge-case mapping: [`Use Cases/InterviewSync Full Edge Case Map.pdf`](./Use%20Cases/InterviewSync%20Full%20Edge%20Case%20Map.pdf)

---

## 📂 Repository Structure

interview-sync/
├── README.md
├── LICENSE
├── The-Panel-Orchestrator (1).pdf          ← Full project writeup
├── AgenticX_ Hackathon Briefing - 28th March.pdf
├── AgenticX_ Hackathon - Sample Data - 28th-29th March.pdf
│
├── interviewsync.html                       ← Main orchestrator UI
├── interivewsyncUI.html                     ← Alternate UI
├── aditi_hr_persona.html                    ← Interactive persona
├── InterviewSync_n8n_NodeGuide.html         ← Node-by-node guide
│
├── InterviewSync Happy Path.png             ← Flow diagrams
├── InterviewSync Disruption Handling Flow.png
│
├── InterviewSync - Complete Workflow (...) .json   ← n8n workflows
├── InterviewSync_ Panel Orchestrator.json
├── The Panel Orchestration.json
├── interviewsync_complete_workflow.json
│
├── Final/
│   └── interviewsync_integrated.html        ← Final integrated build
│
├── Use Cases/
│   ├── InterviewSync Happy Path.pdf
│   ├── InterviewSync Disruption Handling Flow.pdf
│   └── InterviewSync Full Edge Case Map.pdf
│
└── n8n work flow/                           ← Alternate workflow exports
├── InterviewSync - Complete Workflow (1).json
├── InterviewSync - Complete Workflow (2).json
├── InterviewSync_ Panel Orchestrator.json
├── The Panel Orchestration.json
└── interviewsync_complete_workflow.json



---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Orchestration** | n8n (visual agentic workflow) |
| **Frontend** | HTML + CSS (custom dashboards, Sora + DM Mono fonts) |
| **AI Layer** | LLM-backed decisioning for disruption resolution |
| **Integrations** | Calendar, Slack/Email (via n8n nodes) |
| **Format** | Browser-viewable — no build step |

---

## 🏆 Hackathon Context

Built for the **AgenticX Hackathon** (28th–29th March).

- 📄 [Hackathon Briefing](./AgenticX_%20Hackathon%20Briefing%20-%2028th%20March.pdf)
- 📊 [Sample Data](./AgenticX_%20Hackathon%20-%20Sample%20Data%20-%2028th-29th%20March.pdf)
- 📘 [Full Project Writeup](./The-Panel-Orchestrator%20%281%29.pdf)

---

## 🗺️ Roadmap

- [x] Persona research (Aditi, HR Lead)
- [x] Happy-path flow mapping
- [x] Full edge-case disruption map
- [x] n8n agentic workflow (happy path + all edge cases)
- [x] HR dashboard UI
- [x] Interactive persona deck
- [ ] Real-time calendar sync (Google + Outlook)
- [ ] Slack-native HR notifications
- [ ] Post-day analytics dashboard
- [ ] Multi-tenant SaaS deployment

---

## 🚀 Getting Started

### View the UIs
Clone and open any HTML file directly in your browser — no build step required.

```bash
git clone https://github.com/MadarSaheb100/interview-sync.git
cd interview-sync
# Open in browser
start interviewsync.html            # Windows
open interviewsync.html             # macOS
xdg-open interviewsync.html         # Linux
Run the n8n Workflow
Install n8n (self-hosted or n8n.cloud)
Go to Workflows → Import from File
Select InterviewSync - Complete Workflow (Happy Path + All Edge Cases) (1).json
Configure credentials (Calendar, Slack, LLM provider)
Activate and trigger with sample data
👨‍💻 Author
Mohammed Madar Saheb
AgenticX Hackathon · Panel Orchestration Track

📜 License
This project is licensed under the MIT License — see the LICENSE file for details.



---

## Suggested repo metadata

### Topics (add via ⚙️ next to About)
n8n  ai-agent  agentic-workflow  interview-scheduling  hr-tech
panel-orchestration  hackathon  agenticx  automation  workflow
llm  orchestration  super-day  disruption-handling



### Slightly tighter About-box (optional)
> Agentic AI system that orchestrates interview Super Days — coordinating panels, handling no-shows/delays/swaps in real time, and keeping HR, interviewers, and candidates in sync. Built with n8n + HTML dashboards for the AgenticX Hackathon.

---

## Recommended cleanup (do after the README update)

Your root is a bit cluttered with 14 files. Optional reorganization:

interview-sync/
├── README.md
├── LICENSE
├── .gitignore
├── docs/              ← all PDFs go here
├── ui/                ← all HTML files go here
├── workflows/         ← all JSON files go here
├── diagrams/          ← PNG flow diagrams
└── Final/             ← keep as is (integrated build)



⚠️ **If you reorganize, remember to update every link in the README** — the ones I wrote assume the current root-level layout. Easiest approach: update the README *after* moving files, swapping each `./filename.ext` for `./folder/filename.ext`.

---

## Heads-up: check your n8n JSONs for secrets

Before anything else, **open each `.json` workflow in a text editor** and scan for:
- API keys (OpenAI, Anthropic, Google)
- Webhook URLs with tokens
- Credential IDs tied to your personal n8n account
- Email addresses / phone numbers from sample data

Replace anything sensitive with placeholders like `"YOUR_OPENAI_KEY"`. These files are already public — if anything leaked, **rotate those keys immediately** (not just delete from the repo; GitHub caches forever).

---
