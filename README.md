<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F172A,50:7C3AED,100:22D3EE&height=170&section=header&text=Abhijeet%20Nag&fontSize=44&fontColor=ffffff&fontAlignY=32&desc=Agentic%20Systems%20%C2%B7%20LLM%20Evaluation%20%C2%B7%20Voice%20AI&descAlignY=52&descSize=16" width="100%" alt="banner"/>

<p align="center">
  <a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=3000&pause=900&color=22D3EE&center=true&vCenter=true&width=650&lines=Code+owns+control+flow.+Models+do+bounded+reasoning.;Every+LLM+call+has+a+schema%2C+a+budget%2C+and+a+fallback.;Evals+over+vibes.+ROC-AUC+gates+every+promotion." alt="typing"/></a>
</p>

<p align="center">
  <a href="https://agentlink.pro"><img src="https://img.shields.io/badge/AgentLink-live_product-22D3EE?style=for-the-badge&labelColor=0F172A" alt="AgentLink"/></a>
  <a href="https://linkedin.com/in/abhijeet-nag"><img src="https://img.shields.io/badge/LinkedIn-connect-7C3AED?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0F172A" alt="LinkedIn"/></a>
  <a href="mailto:abhijeetnag0@gmail.com"><img src="https://img.shields.io/badge/Email-reach_out-EC4899?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0F172A" alt="Email"/></a>
  <img src="https://img.shields.io/badge/Remote-UTC%2B5:30_·_US_mornings-16A34A?style=for-the-badge&labelColor=0F172A" alt="Remote"/>
</p>

---

**4.5 years of software engineering — the last 1.5 building production LLM systems.**

I build agentic products where **code owns control flow** and models do bounded reasoning under strict JSON contracts — then I measure them: ROC-AUC evaluation loops, per-run cost budgets, and a non-LLM fallback behind every model call.

- 🚀 Shipped **[AgentLink](https://agentlink.pro)** — a live AI recruiting platform — solo, from schema to deploy
- 🎙️ Voice AI at **~1.2s end-to-end latency** (STT 300ms → LLM 600ms → TTS 300ms) with VAD barge-in
- 📊 I care about **evals over vibes** — champion/challenger, offline replay, LLM-as-judge, selection-bias analysis
- 📫 Reach me at **abhijeetnag0@gmail.com**

---

### 🚀 Flagship — AgentLink · Sole Engineer & Architect

> Live AI recruiting platform: JD parsing → resume scoring → AI voice screening → transcript evaluation → calendar booking, with usage-based billing.
> **~60K LOC · 462 commits · 39-table Postgres schema**

| Decision | Why it matters |
|---|---|
| **Deterministic workflow engine** over an agent framework — step graph is data in Postgres (2 templates, 18 steps, 15 agent types) | Reproducible runs + per-step audit trail a regulated hiring domain requires |
| **Single LLM gateway** — prompt-hash cache (12h TTL), primary→fallback cascade, schema validation, token/cost accounting | Per-campaign USD budget whose hard stop *pauses* the campaign instead of failing it |
| **Two-pass adversarial scoring ensemble** (hiring manager vs. skeptical recruiter) + 8-gate deterministic policy override | Tuned for precision — a wasted screening call costs far more than two LLM calls |
| **Closed eval loop** on a free downstream label (did the candidate pass the voice screen) | ROC-AUC (Mann–Whitney) gates promotion at +0.01, n ≥ 40; promotion is a reversible row flip |
| **pgvector** instead of a dedicated vector DB (text-embedding-3-small, 1536-dim, cosine) | Consent, do-not-contact and dedup filters run in the *same atomic query* |
| **Version-controlled Retell conversation-flow state graph**, reconciled on boot | Deterministic transcript analysis runs before the LLM; every AI path degrades to a non-LLM fallback |

---

### 💼 Experience

**AI Engineer & Product Developer — Intellylabs** · *Mar 2025 — Present · Remote*
Lead engineer on **IntellyMind**, an ecosystem of autonomous voice AI agents for recruiting, sales and visa workflows.
- Real-time voice interviewing system (FastAPI + WebSockets) with a RAG pipeline (ChromaDB + BGE-Reranker) generating context-aware technical questions — **95% pass rate** on an LLM-as-judge eval over 500 JD/question pairs
- ~**1.2s** end-to-end voice latency (FasterWhisper float16 on GPU, Silero VAD barge-in)
- Outbound sales agent with Apollo.io enrichment + BANT lead scoring; **hybrid routing** (local Ollama for intent, GPT-4o for reasoning) to cut inference cost
- **9-language** visa voice backend with human-in-the-loop fallback on low-confidence turns and centralized ELK observability

**Software Engineer — Credex Technology** · *Oct 2021 — Feb 2025 · Noida*
- Shipped production mobile apps — native Android (Kotlin), iOS (Swift), Flutter (MPOS, agri-tech) — owned architecture → release
- Optimized MongoDB aggregation pipelines: **-30%** dashboard load time; GitHub Actions CI/CD: **-40%** deploy time

---

### 🛠️ Tech

**LLM Engineering** — Structured outputs & schema validation · prompt-hash caching · model cascading · per-run cost budgeting · adversarial multi-pass ensembles · prompt-injection guardrails · LangChain / LangGraph

**Evaluation** — ROC-AUC · champion/challenger · offline replay · LLM-as-judge · selection-bias analysis · regression suites

**RAG & Retrieval** — pgvector · ChromaDB · BGE-Reranker · text-embedding-3-small · semantic dedup · peer-fit ranking

**Voice AI** — Retell AI · Twilio Voice · FasterWhisper · Silero VAD · Google Cloud TTS · WebSocket audio streaming · latency budgeting

**Backend & Infra** — TypeScript/Node · Python/FastAPI · PostgreSQL + Prisma · Redis · Docker · Kubernetes · Celery · ELK · React/Next.js · Flutter

---

<p align="center">
  🎓 <b>B.Tech, Computer Science</b> — GLA University (2018–2022) &nbsp;·&nbsp; 📍 Lucknow, India
</p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:22D3EE,50:7C3AED,100:0F172A&height=110&section=footer" width="100%" alt="footer"/>
