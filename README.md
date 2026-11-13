# ArriaOne — Unified Delivery Shell

> **One window. One context. Nine capabilities. No context switches.**

A single-file concept prototype demonstrating what a **unified developer experience** across the full software delivery lifecycle could look like.

---

## The problem

Modern software teams juggle 7–10 separate tools to ship a single change — a planning tool, a diagramming tool, an IDE, a Git host, a CI/CD platform, a test management system, a release tracker, a deployment dashboard, and an observability tool. Each has its own login, its own navigation, its own mental model of "project" or "team", and its own way of representing the same underlying work item.

**ArriaOne** is a UI concept that challenges this fragmented reality. It proposes a persistent shell that wraps all nine delivery capabilities — Plan, Architect, Code, Control, Build, Test, Release, Deploy, Observe — in a single, context-aware window.

---

## What ArriaOne demonstrates

### 1 — One window
A fixed shell (header + side navigation + Arria assistant drawer) stays in place. Each of the nine capabilities renders inside it. No new tabs, no re-authentication, no empty landing pages.

### 2 — One context
Switch the **delivery stream** (e.g. "Payments Platform / Checkout") once in the header. Every capability instantly reflects that context — the sprint board, the repos, the pipelines, the environments, the metrics — all scoped to the same team and product.

### 3 — One thread
Any work item ID (e.g. `PAY-148`) is a hyperlink everywhere. Clicking it opens a **Trace** view that follows that single change through every stage: when it was planned, which dev container was used, which PR, which build, which test run, which release gate, which deploy, what the latency impact was.

### 4 — Arria (AI assistant)
An AI assistant drawer that understands the full stream context. It surfaces stage-specific insights — blocked items, flaky tests, bottlenecks — and proposes actions. Every stage has a scripted, context-aware Arria response in this prototype.

### 5 — Arria Pilot (multi-agent orchestrator)
The most ambitious piece of the concept. Describe a delivery goal (e.g. *"Fix defect DL-4821 and release to staging"*). Arria Pilot:

1. Generates a step-by-step plan across four AI agents: **Stream Arria**, **Code Arria**, **Test Arria**, **Ship Arria**
2. Shows a reasoning panel explaining why each step is included
3. Runs the plan live — animated swimlane view shows each agent working and passing context artifacts to the next
4. Self-corrects when Test Arria finds failures — routes back to Code Arria for a revised diff (retry 1 of 3)
5. Pauses at a human approval gate before releasing
6. Produces an audit trail of every decision, who made it, and the evidence

Each step has a configurable autonomy setting: **Auto**, **Ask me**, or **Manual**.

### 6 — Before vs ArriaOne
A side-by-side comparison of today's fragmented UX (each capability has its own context model and landing page) vs the unified shell approach.

---

## Capability map

| Capability | What it covers |
|---|---|
| **Plan** | Kanban sprint board, work item backlog |
| **Architect** | System design diagram, component graph |
| **Code** | Dev containers started from work items |
| **Control** | Pull requests linked to work items |
| **Build** | Pipeline runs, build history, failure drill-down |
| **Test** | Test suites, verdicts, flaky test tracking |
| **Release** | Release gates (automated + human approval) |
| **Deploy** | Environment promotion, deployment history |
| **Observe** | DORA metrics, value stream, bottleneck analysis |

---

## Arria Agent roster

| Agent | Covers | Role |
|---|---|---|
| **Stream Arria** | Plan · Architect · Observe | Scopes work, creates follow-ups, closes the stream |
| **Code Arria** | Code · Control · Build | Generates code changes, opens PRs, runs builds |
| **Test Arria** | Test | Generates tests, runs suites, quarantines flaky tests |
| **Ship Arria** | Release · Deploy | Assembles release candidates, verifies deployments |
| **Arria Pilot** | — | Orchestrates all agents, routes failures, holds human gates |

---

## Technical notes

- **100% single-file** — `index.html` only. No framework, no build step, no server, no dependencies beyond two Google Fonts.
- **Fonts** — [Inter](https://fonts.google.com/specimen/Inter) (UI) + [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) (code/IDs)
- **Routing** — hash-based (`#/plan`, `#/trace/PAY-148`, `#/pilot/run`, etc.)
- **Responsive** — collapses nav at ≤760 px, reflows grids at ≤1100 px
- **Command palette** — `⌘K` / `Ctrl+K` to jump anywhere
- **All data is fictional** — teams, work items, builds, PRs, and AI responses are hardcoded for demonstration purposes

---

## How to run

```bash
open index.html
# or just drag index.html into any browser
```

No install. No build. Works offline (except Google Fonts, which degrade gracefully to system fonts).

---

## Concepts explored

- **Unified context propagation** — one "stream + team" selection applied to all nine tools simultaneously
- **Cross-capability linking** — a work item ID is the primary key that threads through every capability
- **Progressive automation** — per-step autonomy controls (Auto / Ask me / Manual) on AI-driven workflows
- **Self-correcting agents** — retry loops with root-cause handoff between agents before escalating to a human
- **Audit by default** — every decision in an orchestrated run is logged with timestamp, actor, and evidence

---

## Status

⚠️ **Concept prototype only.** All data is fictional. All AI responses are scripted. This is a design exploration and conversation starter, not a product commitment or roadmap.

---

*ArriaOne — forward-thinking DevOps UX concept.*
