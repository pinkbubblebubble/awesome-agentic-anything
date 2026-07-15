# Awesome Agentic *Anything* [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of **agentic systems across every domain** — not "any AI", but *agentic* AI, wherever it shows up.

Agents are spreading into coding, science, browsing, robotics, finance, research, and beyond. This list tracks that spread. It collects the **systems that act autonomously toward a goal**, and the **infrastructure and research** that make them possible.

The organizing idea is simple: **any domain, but it must be agentic.** A coding assistant that plans, edits, runs tests, and iterates on its own belongs here. A single-turn chatbot does not.

## What Counts as "Agentic"?

We apply two layered standards.

**For a *system* to be listed** (the domain sections), it should exhibit most of:

| Trait | Meaning |
|-------|---------|
| **Autonomy** | Decides its own next step instead of following a hard-coded script. |
| **Tool use** | Calls external tools, APIs, or code execution to affect its environment. |
| **Perception–action loop** | Observes → reasons → acts → observes again, iterating toward a result. |
| **Goal-directedness** | Given a high-level goal, decomposes it into sub-tasks itself. |
| **Memory / state** | Carries state across steps and learns from outcomes. |

**We exclude:** base models (GPT, Claude, Llama), single-turn LLM apps, plain RAG Q&A, and pure DAG/workflow tools with no agentic decision-making.

**For *infrastructure* to be listed** (Building Blocks), the test is narrower: it must be **purpose-built for agents** — an agent framework, an agent protocol, an agent memory layer, an agent benchmark. A general-purpose vector database is not agentic infrastructure; an agent-to-agent protocol is.

See [CONTRIBUTING.md](CONTRIBUTING.md) before submitting.

## Contents

- [🏗️ Building Blocks & Infrastructure](#️-building-blocks--infrastructure)
  - [Frameworks & Libraries](#frameworks--libraries)
  - [Protocols & Interop](#protocols--interop)
  - [Memory & State](#memory--state)
  - [Evaluation & Benchmarks](#evaluation--benchmarks)
- [🌐 Agentic ∀ Domains](#-agentic--domains)
  - [General-Purpose Autonomous Agents](#general-purpose-autonomous-agents)
  - [💻 Agentic Coding](#-agentic-coding)
  - [🔬 Agentic Science](#-agentic-science)
  - [🖥️ Agentic Browser & Computer Use](#️-agentic-browser--computer-use)
  - [🔎 Agentic Research & Deep Research](#-agentic-research--deep-research)
  - [🤖 Agentic Robotics & Embodied](#-agentic-robotics--embodied)
  - [💰 Agentic Finance & Trading](#-agentic-finance--trading)
  - [📊 Agentic Data & Analytics](#-agentic-data--analytics)
- [📚 Learn](#-learn)
  - [Papers & Research](#papers--research)
  - [Articles & Blogs](#articles--blogs)
  - [Tutorials & Courses](#tutorials--courses)
- [Contributing](#contributing)
- [License](#license)

---

## 🏗️ Building Blocks & Infrastructure

> These aren't agents themselves — they're the frameworks, protocols, memory layers, and benchmarks you use to **build and evaluate** agentic systems.

### Frameworks & Libraries

- [LangGraph](https://github.com/langchain-ai/langgraph) — Low-level orchestration framework for stateful, multi-actor agent applications, built by the LangChain team.
- [LangChain](https://github.com/langchain-ai/langchain) — The most widely used toolkit for composing LLMs with tools, memory, and agent loops.
- [AutoGen](https://github.com/microsoft/autogen) — Microsoft framework for multi-agent conversation and orchestration.
- [CrewAI](https://github.com/crewAIInc/crewAI) — Role-playing autonomous agents that collaborate as a "crew" on tasks.
- [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) — Lightweight framework for multi-agent workflows from OpenAI (successor to Swarm).
- [Google ADK](https://github.com/google/adk-python) — Agent Development Kit for building and deploying agents, from Google.
- [LlamaIndex](https://github.com/run-llama/llama_index) — Data framework with strong agent and tool-calling support over your own data.
- [smolagents](https://github.com/huggingface/smolagents) — Minimal library from Hugging Face where agents write and run code as actions.
- [Pydantic AI](https://github.com/pydantic/pydantic-ai) — Type-safe agent framework built on Pydantic, with structured outputs and validation.
- [Semantic Kernel](https://github.com/microsoft/semantic-kernel) — Microsoft SDK for integrating agents and plugins into .NET / Python / Java apps.
- [Agno](https://github.com/agno-agi/agno) — Full-stack framework for multi-agent systems with memory, knowledge, and reasoning.
- [Mastra](https://github.com/mastra-ai/mastra) — TypeScript agent framework with workflows, RAG, and evals.
- [CAMEL](https://github.com/camel-ai/camel) — Research framework for studying the "society of mind" of communicating agents.

### Protocols & Interop

- [Model Context Protocol (MCP)](https://github.com/modelcontextprotocol) — Open standard from Anthropic for connecting agents to tools and data sources.
- [Agent2Agent (A2A)](https://github.com/a2aproject/A2A) — Open protocol for interoperability and communication between independent agents.
- [AGNTCY](https://github.com/agntcy) — Open collective building an interoperable "Internet of Agents" stack.

### Memory & State

- [Letta (MemGPT)](https://github.com/letta-ai/letta) — Framework for agents with long-term memory and persistent state ("agents as a service").
- [mem0](https://github.com/mem0ai/mem0) — Memory layer that gives agents personalized, persistent recall across sessions.
- [Zep](https://github.com/getzep/zep) — Long-term memory and context engineering service for agent applications.
- [cognee](https://github.com/topoteretes/cognee) — Memory for agents built on knowledge graphs plus vector retrieval.

### Evaluation & Benchmarks

- [SWE-bench](https://github.com/SWE-bench/SWE-bench) — Benchmark of real GitHub issues that agents must resolve by editing codebases.
- [GAIA](https://huggingface.co/datasets/gaia-benchmark/GAIA) — General AI Assistants benchmark of real-world questions requiring tool use and reasoning.
- [τ-bench (tau-bench)](https://github.com/sierra-research/tau-bench) — Benchmark for agents in dynamic, tool-using conversations with simulated users.
- [WebArena](https://github.com/web-arena-x/webarena) — Realistic, self-hostable web environment for evaluating web agents.
- [OSWorld](https://github.com/xlang-ai/OSWorld) — Benchmark for multimodal agents performing open-ended tasks in real computer environments.
- [AgentBench](https://github.com/THUDM/AgentBench) — Multi-environment benchmark evaluating LLMs as agents across 8 settings.
- [BrowserGym](https://github.com/ServiceNow/BrowserGym) — Gym environment for building and evaluating web agents.

---

## 🌐 Agentic ∀ Domains

> The core of "anything": agentic systems, organized by the domain they act in. Each must satisfy the agentic standard above.

### General-Purpose Autonomous Agents

- [AutoGPT](https://github.com/Significant-Gravitas/AutoGPT) — The project that popularized autonomous, goal-driven GPT agents; now a platform for building them.
- [MetaGPT](https://github.com/geekan/MetaGPT) — Multi-agent framework that simulates a software company (PM, architect, engineer) to build products.
- [BabyAGI](https://github.com/yoheinakajima/babyagi) — Minimal task-driven autonomous agent that spawns and prioritizes its own to-do list.
- [SuperAGI](https://github.com/TransformerOptimus/SuperAGI) — Dev-first framework to build, manage, and run autonomous agents with a GUI.
- [AgentGPT](https://github.com/reworkd/AgentGPT) — Assemble, configure, and deploy autonomous agents in the browser.
- [ChatDev](https://github.com/OpenBMB/ChatDev) — Virtual software company of communicative agents that design, code, and test together.

### 💻 Agentic Coding

- [OpenHands](https://github.com/All-Hands-AI/OpenHands) — Open platform (formerly OpenDevin) for AI software-development agents that write code and run commands.
- [Aider](https://github.com/Aider-AI/aider) — AI pair programmer in your terminal that edits code across your git repo.
- [SWE-agent](https://github.com/SWE-agent/SWE-agent) — Agent from Princeton that autonomously fixes GitHub issues; strong on SWE-bench.
- [Cline](https://github.com/cline/cline) — Autonomous coding agent in your IDE that plans, edits files, and runs terminal commands.
- [Devin](https://cognition.ai/) — Cognition's autonomous software engineer (commercial).
- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) — Anthropic's agentic coding tool that works in the terminal and edits your codebase.
- [OpenAI Codex CLI](https://github.com/openai/codex) — Lightweight coding agent that runs in your terminal.
- [Goose](https://github.com/block/goose) — Block's open-source, extensible on-machine coding agent.
- [GPT Engineer](https://github.com/gpt-engineer-org/gpt-engineer) — Specify what to build in natural language and the agent writes the codebase.

### 🔬 Agentic Science

- [The AI Scientist](https://github.com/SakanaAI/AI-Scientist) — Sakana AI's system for fully automated, end-to-end scientific discovery and paper writing.
- [ChemCrow](https://github.com/ur-whitelab/chemcrow-public) — LLM chemistry agent that plans and executes syntheses using expert-designed tools.
- [Agent Laboratory](https://github.com/SamuelSchmidgall/AgentLaboratory) — Autonomous LLM agents that run the full research workflow from idea to report.
- [Coscientist](https://github.com/gomesgroup/coscientist) — Autonomous agent that designs, plans, and executes chemistry experiments (Nature 2023).
- [Agents4Science](https://agents4science.stanford.edu/) — Initiative and conference exploring AI agents as autonomous participants in the scientific process.

### 🖥️ Agentic Browser & Computer Use

- [browser-use](https://github.com/browser-use/browser-use) — Make websites accessible to agents; drives a real browser to complete tasks.
- [Anthropic Computer Use](https://docs.anthropic.com/en/docs/build-with-claude/computer-use) — Claude's ability to see the screen and control mouse/keyboard like a person.
- [Skyvern](https://github.com/Skyvern-AI/skyvern) — Automates browser-based workflows with LLMs and computer vision.
- [Stagehand](https://github.com/browserbase/stagehand) — AI browser automation framework that mixes natural-language and code control.
- [LaVague](https://github.com/lavague-ai/LaVague) — Framework for building web agents that turn instructions into browser actions.

### 🔎 Agentic Research & Deep Research

- [GPT Researcher](https://github.com/assafelovic/gpt-researcher) — Autonomous agent that conducts multi-source web research and produces cited reports.
- [STORM](https://github.com/stanford-oval/storm) — Stanford system that researches a topic and writes a Wikipedia-style article with citations.
- [Local Deep Research](https://github.com/LearningCircuit/local-deep-research) — Privacy-focused deep-research agent that runs iterative search-and-synthesize loops locally.

### 🤖 Agentic Robotics & Embodied

- [Voyager](https://github.com/MineDojo/Voyager) — LLM-powered lifelong-learning agent that autonomously explores and gains skills in Minecraft.
- [Eureka](https://github.com/eureka-research/Eureka) — Uses LLMs to write reward functions for reinforcement-learning robotic skills.

### 💰 Agentic Finance & Trading

- [FinRobot](https://github.com/AI4Finance-Foundation/FinRobot) — Open-source AI agent platform for financial analysis using LLMs.
- [TradingAgents](https://github.com/TauricResearch/TradingAgents) — Multi-agent LLM framework that simulates a trading firm's roles to make decisions.
- [ai-hedge-fund](https://github.com/virattt/ai-hedge-fund) — Proof-of-concept multi-agent system that mimics famous investors to trade.

### 📊 Agentic Data & Analytics

- [PandasAI](https://github.com/sinaptik-ai/pandas-ai) — Conversational agent that queries and analyzes dataframes and databases in natural language.

---

## 📚 Learn

### Papers & Research

- [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629) — The reason-then-act loop underpinning most modern agents.
- [Reflexion: Language Agents with Verbal Reinforcement Learning](https://arxiv.org/abs/2303.11366) — Agents that self-reflect on failures to improve on later attempts.
- [Toolformer: Language Models Can Teach Themselves to Use Tools](https://arxiv.org/abs/2302.04761) — Self-supervised learning of when and how to call APIs.
- [Generative Agents: Interactive Simulacra of Human Behavior](https://arxiv.org/abs/2304.03442) — Believable agents with memory, reflection, and planning in a simulated town.
- [Tree of Thoughts: Deliberate Problem Solving with LLMs](https://arxiv.org/abs/2305.10601) — Search over reasoning paths for deliberate planning.
- [Voyager: An Open-Ended Embodied Agent with LLMs](https://arxiv.org/abs/2305.16291) — Lifelong learning and skill acquisition in an open world.
- [HuggingGPT: Solving AI Tasks with ChatGPT and its Friends](https://arxiv.org/abs/2303.17580) — An LLM controller orchestrating specialist models as tools.

### Articles & Blogs

- [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) — Lilian Weng's foundational overview of agent architecture (planning, memory, tools).
- [Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) — Anthropic's practical guide to agent vs. workflow patterns.
- [Agents](https://huyenchip.com/2025/01/07/agents.html) — Chip Huyen's deep dive on how agents plan, use tools, and fail.
- [Don't Build Multi-Agents](https://cognition.ai/blog/dont-build-multi-agents) — Cognition's contrarian take on context and reliability in agent design.

### Tutorials & Courses

- [Hugging Face Agents Course](https://github.com/huggingface/agents-course) — Free, hands-on course from fundamentals to deploying agents.
- [LangChain Academy: Introduction to LangGraph](https://academy.langchain.com/courses/intro-to-langgraph) — Official course on building stateful agents with LangGraph.
- [DeepLearning.AI Short Courses](https://www.deeplearning.ai/short-courses/) — Multiple free short courses on agents, tool use, and multi-agent systems.

---

## Contributing

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first — especially the "What counts as agentic" bar. In short: open a PR that keeps entries in the right layer, one line each, with an honest one-sentence description.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](LICENSE)

To the extent possible under law, the contributors have waived all copyright and related rights to this work. See [LICENSE](LICENSE).
