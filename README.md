<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0b1d3a,60:12294f,100:1f3864&height=200&section=header&text=Abhijeet%20Nag&fontSize=52&fontColor=F5C542&fontAlignY=36&desc=AI%20Engineer%20%E2%80%94%20Agentic%20Systems%20%C2%B7%20LLM%20Evaluation%20%C2%B7%20Voice%20AI&descSize=17&descAlignY=58&animation=fadeIn" width="100%" alt="Abhijeet Nag" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=19&duration=2800&pause=900&color=F5C542&center=true&vCenter=true&width=640&lines=I+build+AI+agents+that+pick+up+the+phone.;9-language+voice+agent+%E2%80%94+18%2C000+calls%2Fmonth;~1.2s+end-to-end+voice+latency;Solo-built+AgentLink+%E2%80%94+an+AI+recruiter+in+production" alt="Typing intro" />
</p>

<p align="center">
  <a href="https://www.agentlink.pro/demo"><img src="https://img.shields.io/badge/▶_Live_Demo-AgentLink-F5C542?style=for-the-badge&labelColor=0b1d3a" alt="AgentLink live demo" /></a>
  <a href="https://linkedin.com/in/abhijeet-nag"><img src="https://img.shields.io/badge/LinkedIn-abhijeet--nag-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0b1d3a" alt="LinkedIn" /></a>
  <a href="mailto:abhijeetnag0@gmail.com"><img src="https://img.shields.io/badge/Email-abhijeetnag0@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0b1d3a" alt="Email" /></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/📍_Lucknow,_India-Remote_·_UTC+5:30-1f3864?style=flat-square" alt="Location" />
  <img src="https://img.shields.io/badge/🕘_Overlaps-US_mornings-1f3864?style=flat-square" alt="Timezone overlap" />
  <img src="https://img.shields.io/badge/✅_Open_to-Remote_AI_Engineering_roles-2ea44f?style=flat-square" alt="Open to work" />
  <img src="https://komarev.com/ghpvc/?username=abhinag007&style=flat-square&color=F5C542&label=Profile+views" alt="Profile views" />
</p>

<p align="center">
  <img src="assets/voice-wave.svg" width="100%" alt="Voice agent: ~1.2s latency" />
</p>

## About

AI Engineer with **5 years** of software engineering experience, including **3 years** building production LLM and real-time voice AI systems. I lead engineering on **IntellyMind** at Intellylabs, a suite of autonomous voice agents for recruiting, sales and customer support. I also solo-built **AgentLink**, an AI recruiter that is live in production.

<p align="center">
  <img src="assets/metrics.svg" width="100%" alt="18,000 calls a month · 9 languages · ~1.2s latency · 57K+ LOC" />
</p>

---

## Flagship project: AgentLink

> **An AI recruiter that calls you.** Enter your phone number at **[agentlink.pro/demo](https://www.agentlink.pro/demo)** and it screens you by phone within ~30 seconds.

<p align="center">
  <a href="https://www.agentlink.pro/demo"><img src="assets/agentlink-flow.svg" width="100%" alt="AgentLink pipeline: JD → rubric → rank → AI phone screen → transcript scoring → interview booked" /></a>
</p>

- **End-to-end AI recruiter:** it parses a JD into a scoring rubric, ranks every applicant, phone-screens the shortlist with a Retell voice agent, scores the transcript, and books qualified candidates onto Google Calendar with Meet links.
- **Custom persisted workflow engine** (replacing LangGraph for reliability) with Postgres-backed runs, step retries and a crash-recovery sweep. Calls honor callback requests ("call me Sunday 5 PM"), resume dropped calls mid-screen, and cap retries.
- **Production hardening:** LLM cost guardrails (per-campaign budgets, prompt caching, model fallback), integrity-risk scoring, and pgvector for semantic talent rediscovery.

<p>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
  <img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white" />
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL_+_pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" />
  <img src="https://img.shields.io/badge/Retell_Voice-111827?style=flat-square" />
  <img src="https://img.shields.io/badge/57K_LOC_·_512_commits_·_75_tests-2ea44f?style=flat-square" />
</p>

---

## Experience

<details open>
<summary><b>Multilingual Inbound Voice AI Agent</b> (Intellylabs): 9 languages · 18,000 calls/month · ~INR 11.85 per call</summary>
<br/>

- Plivo streams bidirectional WSS audio into a **Pipecat** pipeline with VAD, turn detection and barge-in cancellation.
- **Language routing** auto-detects the caller's language on the first response and locks it. Sarvam covers 7 Indian languages and Azure Speech covers Filipino and Arabic.
- **Grounded reasoning:** Gemini 2.5 Flash tool calling with Pydantic validation, backed by read-only Postgres queries checked with SQLGlot.
- **Observability:** Langfuse tracing, LLM-as-judge scoring on a 5% call sample, and CloudWatch alerts, running on ECS Fargate.
</details>

<details>
<summary><b>Autonomous Voice Hiring Agent</b> (Intellylabs): built from scratch, no voice framework · ~1.2s latency</summary>
<br/>

- WebSocket audio streaming with STT → LLM → TTS orchestration and interruption handling in FastAPI.
- Latency budget: self-hosted FasterWhisper (300ms) + LLM (600ms) + TTS (300ms), with Silero VAD barge-in.
- A RAG pipeline (ChromaDB + BGE-Reranker) generates role-specific questions. It scored a **95% pass rate** on an LLM-as-judge eval over 500 JD/question pairs.
</details>

<details>
<summary><b>Sales & Lead Qualification Agent</b> (Intellylabs): BANT scoring · hybrid model routing</summary>
<br/>

- An outbound agent with Apollo.io enrichment and BANT lead scoring over call transcripts.
- Hybrid routing sends intent to local Ollama and reasoning to GPT-4o, which cut inference cost.
</details>

| When | Role | Highlights |
|---|---|---|
| **Mar 2025 – now** | AI Engineer & Product Developer, **Intellylabs** (Remote) | Lead engineer on IntellyMind voice agents |
| **Oct 2021 – Feb 2025** | Software Engineer, **Credex Technology** (Noida) | LLM MVPs with the OpenAI API (2023); mobile apps in Kotlin, Swift and Flutter; **−30%** dashboard load time; **−40%** deploy time |
| **2018 – 2022** | B.Tech, Computer Science, **GLA University** | |

---

## Tech stack

| Area | Tools |
|---|---|
| **LLM & agents** | ![OpenAI](https://img.shields.io/badge/GPT--4o-412991?style=flat-square&logo=openai&logoColor=white) ![Gemini](https://img.shields.io/badge/Gemini_2.5_Flash-8E75B2?style=flat-square&logo=googlegemini&logoColor=white) ![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white) ![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white) ![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square) ![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white) |
| **RAG & eval** | ![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6F00?style=flat-square) ![pgvector](https://img.shields.io/badge/pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![Langfuse](https://img.shields.io/badge/Langfuse-0A0A0A?style=flat-square) ![LLM-as-Judge](https://img.shields.io/badge/LLM--as--Judge-374151?style=flat-square) ![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white) |
| **Voice AI** | ![Pipecat](https://img.shields.io/badge/Pipecat-111827?style=flat-square) ![Retell](https://img.shields.io/badge/Retell-111827?style=flat-square) ![Plivo](https://img.shields.io/badge/Plivo-4FB848?style=flat-square) ![Twilio](https://img.shields.io/badge/Twilio-F22F46?style=flat-square&logo=twilio&logoColor=white) ![Whisper](https://img.shields.io/badge/FasterWhisper-412991?style=flat-square) ![Sarvam](https://img.shields.io/badge/Sarvam-FF6B00?style=flat-square) ![Azure Speech](https://img.shields.io/badge/Azure_Speech-0078D4?style=flat-square) |
| **Backend** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white) |
| **Cloud & DevOps** | ![AWS](https://img.shields.io/badge/AWS_(ECS,_S3,_CloudWatch)-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) |
| **Frontend & mobile** | ![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white) ![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white) ![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white) ![Swift](https://img.shields.io/badge/Swift-F05138?style=flat-square&logo=swift&logoColor=white) |

---

## GitHub activity

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=abhinag007&show_icons=true&hide_border=true&count_private=true&bg_color=0b1d3a&title_color=F5C542&icon_color=F5C542&text_color=E6EDF3" alt="GitHub stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=abhinag007&layout=compact&hide_border=true&bg_color=0b1d3a&title_color=F5C542&text_color=E6EDF3" alt="Top languages" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=abhinag007&hide_border=true&background=0b1d3a&ring=F5C542&fire=F5C542&currStreakLabel=F5C542&sideLabels=E6EDF3&currStreakNum=E6EDF3&sideNums=E6EDF3&dates=9BA9B4&stroke=1f3864" alt="GitHub streak" />
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/abhinag007/abhinag007/output/github-snake-dark.svg" />
    <img width="100%" src="https://raw.githubusercontent.com/abhinag007/abhinag007/output/github-snake.svg" alt="" />
  </picture>
</p>

---

<p align="center">
  <b>Hiring for AI agents, voice AI or LLM infrastructure?</b><br/>
  <a href="https://www.agentlink.pro/demo">Try AgentLink</a> · <a href="https://linkedin.com/in/abhijeet-nag">Connect on LinkedIn</a> · <a href="mailto:abhijeetnag0@gmail.com">Email me</a>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:1f3864,40:12294f,100:0b1d3a&height=110&section=footer" width="100%" alt="" />
</p>
