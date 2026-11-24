# Hi, I'm Karan Sharma 👋

I'm an Agentic AI Engineer with 4+ years of experience shipping agentic AI systems at **Zensar Technologies** and **ZS Associates**, including enterprise IT triage agents and LLM platforms used by U.S. clients.

- 🎓 Doing an **MS in Artificial Intelligence at Texas A&M**
- 🔭 Working on **eval-driven agent engineering**: measuring long-horizon agent reliability
- 💼 Open to **Summer 2027 AI Engineering internships**

---

## 🏗️ Featured Projects

### [Multi-Agent Research & Action Platform (MARA)](https://github.com/KaranSharma18/multi-agent-research-platform)
`Python` `TypeScript` `LangGraph` `MCP` `A2A` `Claude Agent SDK` `Qdrant` `Postgres` `Braintrust`

A supervisor–worker agent network that answers multi-hop operational questions across documents, a SQL warehouse, live APIs and a remote research agent. It can also take actions, but only after a human approves them.

- A LangGraph supervisor plans the work and fans tasks out in parallel waves. Workers load tools on demand from **4 MCP servers**, using a hash-pinned tool catalog.
- **Zero-trust tool access:** each task gets its own token, exchanged under RFC 8693 for a single audience with least-privilege scopes. Document ACLs and row-level security are enforced at the servers.
- **Human approval for writes:** an approval signs a one-time token bound to the exact action arguments. A separate executor holds the only write credentials.
- An **A2A** handoff goes to a remote web-research agent with a signed Agent Card.
- **120 adversarial eval cases** cover injection, PII exfiltration, scope escalation, tool faults and budget stress, with trace replay. Results: **76% multi-step task completion at ~$0.03/run**.

### [Fixloop: Sandboxed Autonomous Coding & SQL Verification Agent](https://github.com/KaranSharma18/sandboxed-coding-sql-agent)
`Python` `FastAPI` `Docker / gVisor` `Redis Streams` `Postgres` `Pydantic` `Gemini`

A coding agent that only returns what it has proven. It takes a failing test or a SQL question, then plans, patches, runs the code in a locked-down sandbox, reads the trace and repairs, within a strict retry budget.

- A **plan → execute → verify** loop runs in an isolated sandbox with no network, a read-only root and a non-root user, on gVisor in production.
- **Verification is done by execution, not by the model.** Target tests must pass with no regressions, protected tests must be untouched, and hidden tests must pass on a shuffled rerun. For SQL, the query has to match an oracle on the real data *and* on mutated copies of it.
- **Production plumbing:** Redis Streams work queues, Postgres as the source of truth with a transactional outbox, and fencing tokens. Budgets are enforced atomically in Redis Lua.
- Strict JSON-schema outputs, token/cost caps and layered caching remove **~20% of redundant model calls** on recurring workloads.
- It integrates with a GitHub App: it responds to a `/fixloop fix` PR comment by opening a **draft** PR.

### Earlier work: RAG
- [Production-Ready RAG Pipeline](https://github.com/KaranSharma18/Production-ready-RAG-pipeline-with-Deployment): multi-user RAG with Kubernetes and CI/CD deployment.
- [RAG Agent: Document Q&A](https://github.com/KaranSharma18/rag-agent): a local-first RAG agent using Ollama, Chroma and Docker.
- [Advanced RAG Techniques](https://github.com/KaranSharma18/Depth_and_Breadth_of_rag_techniques): semantic chunking, multi-query fusion, hybrid search and self-reflection.

---

## 🛠️ Stack

| | |
|---|---|
| **Agents & Protocols** | LangGraph, OpenAI Agents SDK, Claude Agent SDK, Google ADK, MCP, A2A, Temporal |
| **Retrieval & Models** | Hybrid RAG (dense + BM25 + reranking), Qdrant, FAISS, Pinecone, OpenAI, Claude, Gemini, Llama, vLLM, LoRA/QLoRA |
| **Evals & Safety** | Trajectory & tool-use evals, LLM-as-a-judge, LangSmith, Langfuse, Braintrust, OpenTelemetry, prompt-injection/PII guardrails, red-teaming |
| **Backend & Infra** | Python (asyncio), TypeScript, FastAPI, SSE, PostgreSQL, Redis, Docker, Kubernetes (GKE, EKS), AWS, GCP, GitHub Actions |

---

## 📊 GitHub Stats
![GitHub Stats](https://github-readme-stats.vercel.app/api?username=KaranSharma18&show_icons=true&theme=radical)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=KaranSharma18&layout=compact&theme=radical)

## 🤝 Let's Connect
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/karansharma18/)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:karansharma.professional@gmail.com)
