# Hi, I'm Santino Genta 👋

### AI Engineer · I build production-grade AI agents: multi-agent systems, RAG, tool calling (MCP) and evals

I design agents that are **reliable, not just impressive**: deterministic guardrails around the LLM,
human-in-the-loop for risky actions, automated evaluation in CI, and measured cost and latency.

**Open to AI Engineer / LLM Engineer roles.** → [LinkedIn](https://www.linkedin.com/in/santinogenta) · [santinogenta2325@gmail.com](mailto:santinogenta2325@gmail.com)

---

## ⭐ Featured projects

### 🏢 Enterprise Data AI: AI customer support agents that resolve requests
**Problem:** most support bots only answer from a FAQ. They can't touch business systems, guess when the answer
isn't in their data, and escalate without context, so customers repeat themselves.<br>
**Solution:** an agent that resolves the request end to end. It answers from company data with the source
attached, acts in business systems through MCP, asks a person before risky actions and hands off with full context,
on WhatsApp, email and web chat.

- **Hybrid RAG** (BM25 + vector search) over policies, tickets, emails, transcripts and scanned PDFs (OCR), with cited sources
- **Tool use via MCP:** orders, inventory, payments, helpdesk and CRM, with per-tool rules you control
- **Human-in-the-loop:** refunds above your limit wait for approval · no source, no guess: it hands off instead
- **Full audit trail:** every tool call logged with its time, result and approver

🌐 [**Website & demo**](https://www.enterprisedataai.com/) · 🎥 [Video](https://www.enterprisedataai.com/#demo) · 💻 [Code](https://github.com/santinogenta27/AI-Agents-for-Enterprise-Private-Data)

### ⚡ NexusAgent: multi-agent deep research system
**Problem:** competitive research is slow, and LLM reports invent facts.<br>
**Solution:** a supervisor, retrieval, sandbox, synthesizer and critic agent pipeline that tests hypotheses
against a company's live public pages and checks every claim against verbatim citations before reporting.

- **~19 s** per full report · **$0.0115** per query · **62/62** citations verified verbatim · **130/130** tests passing
- **Stack:** TypeScript · Gemini · Genkit · Express · React 19 · Tailwind

🌐 [**Live demo**](https://nexus-agent-rub3.onrender.com) · 🎥 [Video](https://youtu.be/h7WO4Wd5TJY) · 💻 [Code](https://github.com/santinogenta27/nexus-agent)

### 🏛️ SentinelOps: autonomous financial dispute resolution agent
**Problem:** automating refunds with an LLM is risky: one hallucination or prompt injection moves real money.<br>
**Solution:** a LangGraph agent where *the LLM understands language and code decides money*. Payouts come only
from the verified ledger; refunds over $200 or high-risk cases stop for human approval; an LLM judge scores
every reply before it is sent.

- Self-correction loops · Human-in-the-loop gate · LLM-as-a-Judge · circuit breaker with deterministic fallback
- **125 tests** · eval suite as a CI gate · `mypy --strict` · Stripe (test mode) integration
- **Stack:** Python · LangGraph · FastAPI · Pydantic v2 · Gemini / Groq

🌐 [**Live demo**](https://sentinelops-demo.onrender.com/) · 🎥 [Video demo](https://youtu.be/5cUCUeijuZU) · 💻 [Code](https://github.com/santinogenta27/sentinelops)

---

### 👻 GhostOperator: autonomous web agent
**Problem:** collecting data from websites by hand is slow, and classic scrapers break whenever a page changes.<br>
**Solution:** give the agent a goal in plain language. It opens a real Chromium browser and runs a
**perceive → reason → act → validate** loop until the mission is done, streaming every step live to a dashboard.

- Exports structured results to **JSON and CSV** plus a **video recording** of every mission
- Live dashboard over WebSockets: agent reasoning, actions, screenshots and metrics in real time
- Multi-provider (Gemini / Claude) with retries and backoff · labelled demo fallback when no API key is available
- **Stack:** Python · FastAPI · browser-use · Playwright · WebSockets · React 19 · Vite · Tailwind · Framer Motion

🎥 [Video](https://youtu.be/XUK7UIzj-vI) · 💻 [Code](https://github.com/santinogenta27/Autonomous-Web-Agent)

### 🏭 MCP Factory: production tool-calling infrastructure
**Problem:** every AI agent needs tools, and hand-written MCP servers drift out of spec, accept malformed<br>
inputs and have no retries, cost tracking or tests.
**Solution:** describe the tools once in a Pydantic-validated blueprint, and a Jinja2 compiler generates a typed,
documented, tested MCP server ready for Claude, GPT or Gemini agents.

- One blueprint → **stdio MCP, FastAPI HTTP and Docker image**, all identical
- Strict inputs (`extra="forbid"`) · `ToolCaller` with retries, timing and token-aware cost logging
- Built-in **accuracy and latency evals** that run on every commit · multi-stage, non-root Docker image
- **Stack:** Python · MCP SDK (FastMCP) · Pydantic v2 · Jinja2 · FastAPI · pytest · Docker

💻 [Code](https://github.com/santinogenta27/mcp-factory)

---

## 🛠️ Tech

**AI / LLM:** LangGraph · LangChain · Genkit · MCP · RAG · LLM-as-a-Judge · evals · Gemini · Claude · OpenAI · Groq<br>
**Backend:** Python · TypeScript · FastAPI · Express · Pydantic v2 · SQLite · ChromaDB · Docker<br>
**Frontend:** React 19 · Vite · Tailwind<br>
**Quality:** pytest · mypy --strict · CI eval gates · Playwright
