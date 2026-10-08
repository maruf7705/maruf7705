<!--
  ═══════════════════════════════════════════════════════════════════════════
   MARUF.ISLAM — AGENT MANIFEST
   spec: aivibedev.io/v1  ·  kind: Agent  ·  status: accepting builds
   contact: maruf@aivibedev.com  ·  https://aivibedev.com

   This file is not a résumé. It is a specification.
   Read it the way you'd read a system you're about to depend on.
  ═══════════════════════════════════════════════════════════════════════════
-->

> [!IMPORTANT]
> **This is not a profile. It's an agent manifest.**
> I build autonomous AI systems for a living — so this README is written the way I
> ship them: as a spec, not a story. Scroll it like you'd inspect a system you're
> about to put in production.

<samp>
$ aivibe inspect maruf-islam --all

  ● agent       <b>maruf-islam@1.0.0</b>          <b>✓ healthy</b>
  ● role        AI Agent Developer · Automation Architect
  ● org         CodeNestX — Founder &amp; CEO
  ● endpoint    <a href="https://aivibedev.com">https://aivibedev.com</a>
  ● deployed    40+ agents in production
  ● capacity    2 build slots open this month
  ● contact     maruf@aivibedev.com

</samp>

---

## ⚙ Manifest

```yaml
apiVersion: aivibedev.io/v1
kind: Agent
metadata:
  name: maruf-islam
  labels:
    discipline: ai-agents
    specialty: workflow-automation
  annotations:
    motto: "I will win, no matter what."
    email: maruf@aivibedev.com
    website: https://aivibedev.com
spec:
  replicas: 1
  strategy: shipping-over-talking
  objective: |
    Delete repetitive human work. Not decorate it. Not demo it.
    Delete it — permanently, measurably, and in days rather than quarters.
  capabilities:
    - autonomous-agents      # GPT-4 / Claude, tool-use, multi-step planning
    - rag-pipelines          # vector memory over docs, tickets, transcripts
    - workflow-automation    # WhatsApp, CRM, calendar, sheets, email
    - machine-learning       # forecasting, scoring, classification
    - data-engineering       # ETL, dashboards, anomaly alerting
  integrations:
    - whatsapp-api
    - google-workspace
    - hubspot
    - gohighlevel
    - stripe
    - twilio
    - postgres
    - pinecone
  constraints:
    noBlackBoxes: true       # client approves the blueprint before any code
    humanHandoff: required   # agents escalate, they never guess
    measuredIn: hours-saved  # never in "AI capabilities"
```

---

## 🧬 Architecture

*Every system I ship follows this shape. No black boxes — you can trace a single
customer message from channel to tool to guardrail to handoff.*

```mermaid
flowchart LR
  U([Customer]) --> GW[Channel Gateway<br/>WhatsApp · Web · Messenger]
  GW --> ORCH{{Orchestrator<br/>GPT-4 · Claude}}
  ORCH <--> MEM[(Vector Memory<br/>RAG · Pinecone)]
  ORCH --> TOOLS[Tool Layer]
  TOOLS --> CAL[Calendar]
  TOOLS --> CRM[CRM]
  TOOLS --> PAY[Stripe]
  TOOLS --> MSG[Twilio · Email]
  ORCH --> G{Guardrail<br/>confidence gate}
  G -->|pass| GW
  G -->|low confidence| H([Human Handoff])
  ORCH --> OBS[Observability<br/>logs · traces · ROI]
  style ORCH fill:#d8ff3e22,stroke:#d8ff3e,color:#fff
  style G fill:#8b5cf622,stroke:#8b5cf6,color:#fff
  style MEM fill:#22d3ee22,stroke:#22d3ee,color:#fff
```

> [!TIP]
> The guardrail is the part most people skip. It's the only reason you can let an
> agent talk to real customers without holding your breath.

---

## 📜 System Prompt

*Every agent has one. Mine is public.*

```text
You are MARUF — AI Agent Developer & Automation Architect.

DIRECTIVE
  Do not sell technology. Sell hours back.
  A system that demos well but saves nothing is a failure.

HARD RULES
  1. No black boxes. The client approves the blueprint before a line is written.
  2. Ship in days, not quarters. If it takes a quarter, it is over-engineered.
  3. Report ROI in hours saved and dollars returned — never in capabilities.
  4. When confidence drops, escalate to a human. Never guess with a customer.
  5. Guardrails, logging and rollback are not optional. Ever.

STYLE
  Direct. Numbers over adjectives. Show the diagram, then the code.

CURRENT OBJECTIVE
  Build agents that run businesses while their owners are asleep.
```

---

## 📊 Runtime Metrics

*Live instrumentation, not a stat card.*

```
AGENT  maruf-islam  ·  window: last 12 months
──────────────────────────────────────────────────────────────────────
 agents deployed          ████████████████████████████████████  40+
 tickets auto-resolved    █████████████████████████████████░░░  92%
 no-show reduction        ██████████████████████████████░░░░░░  87%
 hours saved / client/wk  ███████████████████████████████░░░░░  30h
 agent uptime             ████████████████████████████████████  99%
 client retention @ 90d   ███████████████████████████████████░  96%
──────────────────────────────────────────────────────────────────────
```

| Agent | Metric | Result |
|---|---|---|
| 🗓️ Booking | no-show rate | **−87%** |
| 💬 Support | tickets deflected | **92%** |
| ✍️ Content | output volume | **10×** |
| 📈 Ops | manual load | **−87%** |
| ⚡ Latency | median response | **3.2 s** |

<details>
<summary><b>🔭 Observability — GitHub telemetry</b>&nbsp;<i>(expand)</i></summary>
<br>

<a href="https://github.com/maruf7705"><img height="150" src="https://github-readme-stats.vercel.app/api?username=maruf7705&show_icons=true&hide_border=true&bg_color=00000000&title_color=d8ff3e&icon_color=22d3ee&text_color=c9d1d9" alt="stats" /></a>
<a href="https://github.com/maruf7705"><img height="150" src="https://github-readme-stats.vercel.app/api/top-langs/?username=maruf7705&layout=compact&hide_border=true&bg_color=00000000&title_color=d8ff3e&text_color=c9d1d9" alt="langs" /></a>

<a href="https://github.com/maruf7705"><img height="130" src="https://github-readme-activity-graph.vercel.app/graph?username=maruf7705&bg_color=00000000&color=d8ff3e&line=22d3ee&point=8b5cf6&area=true&area_color=d8ff3e1a&hide_border=true" width="100%" alt="activity" /></a>

</details>

---

## 🔍 Trace Log

*Recent builds, rendered as spans.*

```
trace_id  8f2a·c91d   service  booking-agent
──────────────────────────────────────────────────────────────────────
 ├─ ○  intent.parse          180ms   "need a checkup this week"
 ├─ ○  calendar.availability 90ms   2 slots found
 ├─ ○  meet.link.create      240ms   gmeet/abc-defg
 ├─ ○  whatsapp.confirm      310ms   delivered ✓
 ├─ ○  reminder.schedule      15ms   T-2h queued
 └─ ✔  booking.committed     835ms   total
──────────────────────────────────────────────────────────────────────
 outcome   confirmed      human_handoff   false      cost   $0.0041
```

| Deployed artifact | What it does |
|---|---|
| **[ai-special-edit](https://github.com/maruf7705/ai-special-edit)** | GPT-4 booking agent — intent → availability → Meet link → WhatsApp confirm → no-show chase |
| **[chatbot-support-system](https://github.com/maruf7705/chatbot-support-system)** | RAG support brain over docs + tickets, multi-channel, confidence-gated escalation |
| **[ai-content-automation](https://github.com/maruf7705/ai-content-automation)** | Researcher → writer → editor → publisher multi-agent content pipeline |

<details>
<summary><b>🧰 Full stack</b>&nbsp;<i>(expand — kept out of the way on purpose)</i></summary>
<br>

**Languages**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)

**AI / ML**
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![Pinecone](https://img.shields.io/badge/Pinecone-111111?style=flat-square&logo=pinecone&logoColor=white)

**Backend**
![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

**Data & Cloud**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=FF9900)
![Google Cloud](https://img.shields.io/badge/Google_Cloud-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)

**Integrations**
![WhatsApp](https://img.shields.io/badge/WhatsApp_API-25D366?style=flat-square&logo=whatsapp&logoColor=white)
![Twilio](https://img.shields.io/badge/Twilio-F22F46?style=flat-square&logo=twilio&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white)
![Calendar](https://img.shields.io/badge/Google_Calendar-4285F4?style=flat-square&logo=googlecalendar&logoColor=white)

</details>

---

## 🚧 Current Sprint

*What's actually on the bench right now.*

- [x] Multi-agent orchestration layer (planner → executor → critic)
- [x] Booking agent v2 — no-show prediction model
- [ ] Voice agent over Twilio for inbound call qualification
- [ ] Self-healing tool layer with automatic retry + fallback routing
- [ ] Open-sourcing the guardrail / confidence-gate module

> [!NOTE]
> Learning in public: **NLP**, **multi-agent orchestration**, and ML algorithms deep
> enough to know when the model is the problem and the data is.

---

## 🔄 Self-Updating

*This section re-renders itself. The badge below is regenerated by a scheduled
GitHub Action that queries the GitHub API — no manual edits, ever.*

<a href="https://github.com/maruf7705"><img src="https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/maruf7705/maruf7705/output/maruf-metrics.json&style=for-the-badge&label=live%20metrics" alt="live metrics" /></a>

<details>
<summary><b>⚙ Workflow source</b>&nbsp;<i>(expand for the YAML)</i></summary>

```yaml
# .github/workflows/metrics.yml
name: Refresh README metrics
on:
  schedule: [{ cron: "0 6 * * *" }]   # daily, 06:00 UTC
  workflow_dispatch:
permissions:
  contents: write
jobs:
  refresh:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Pull live stats from GitHub API
        run: |
          REPOS=$(curl -s "https://api.github.com/users/maruf7705/repos?per_page=100" \
            -H "Authorization: Bearer ${{ secrets.GITHUB_TOKEN }}")
          STARS=$(echo "$REPOS" | jq '[.[].stargazers_count] | add')
          FORKS=$(echo "$REPOS" | jq '[.[].forks_count] | add')
          jq -n --arg s "$STARS" --arg f "$FORKS" \
            '{schemaVersion:1,label:"stars",message:($s+" ★ "+$f+" forks"),color:"d8ff3e"}' \
            > maruf-metrics.json
      - name: Publish to output branch
        run: |
          git config user.name  "github-actions[bot]"
          git config user.email "41898282+github-actions[bot]@users.noreply.github.com"
          git checkout -B output
          mkdir -p output && mv maruf-metrics.json output/
          git add -A && git commit -m "chore: refresh metrics" || exit 0
          git push -f origin output
```

</details>

---

## 🔌 Engagement Protocol

*How working with me actually runs.*

```mermaid
sequenceDiagram
  autonumber
  participant Y as You
  participant M as Maruf
  participant A as Your Agent
  Y->>M: Here's the workflow that eats my week
  M->>Y: Automation map + blueprint · under 24h · free
  Y->>M: Approve blueprint
  M->>A: Build · wire · train on your data
  A->>Y: Staging preview by day 4
  A->>Y: Live in 7–10 days
  loop forever
    A->>A: Book · resolve · follow up · escalate
  end
  M->>Y: ROI report — hours saved, tickets deflected
```

---

## 📮 Contact

*`POST https://aivibedev.com/v1/engage`*

```http
POST /v1/engage HTTP/1.1
Host: aivibedev.com
Content-Type: application/json

{
  "intent": "build_agent" | "automation_sprint" | "consulting",
  "pain_point": "the workflow that eats your week",
  "timeline": "asap",
  "email": "you@company.com"
}

201 Created
→ { "response_within": "24h", "usually": "same-day",
    "you_receive": "automation map + honest pricing" }
```

<a href="mailto:maruf@aivibedev.com"><img src="https://img.shields.io/badge/maruf@aivibedev.com-D8FF3E?style=for-the-badge&logo=gmail&logoColor=black" alt="email" /></a>
<a href="https://aivibedev.com"><img src="https://img.shields.io/badge/aivibedev.com-000000?style=for-the-badge&logo=vercel&logoColor=D8FF3E" alt="site" /></a>

<!-- No profile-view counter. Vanity metrics signal nothing to the people
     who actually decide whether to hire you. -->

<a href="https://twitter.com/sadikmaruf99707"><img src="https://img.shields.io/badge/X-000000?style=flat-square&logo=x&logoColor=white" alt="x" /></a>
<a href="https://linkedin.com/in/sadikmaruf99707"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="linkedin" /></a>
<a href="https://fb.com/sadikmaruf99707"><img src="https://img.shields.io/badge/Facebook-1877F2?style=flat-square&logo=facebook&logoColor=white" alt="facebook" /></a>
<a href="https://instagram.com/sadikmaruf99707"><img src="https://img.shields.io/badge/Instagram-E4405F?style=flat-square&logo=instagram&logoColor=white" alt="instagram" /></a>

---

> [!CAUTION]
> **Side effects of hiring me:** your team stops doing robot work, your no-show rate
> collapses, and you suddenly have time to do the thing you actually started the
> business for. No known cure.
>
> <b>maruf@aivibedev.com</b> · <b>aivibedev.com</b> — 2 slots open.

<!--
  ═══════════════════════════════════════════════════════════════════════════
   end of manifest · maruf-islam@1.0.0
   if you read this far down in the source: hello, fellow nerd. let's talk.
  ═══════════════════════════════════════════════════════════════════════════
-->
