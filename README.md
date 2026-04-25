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

