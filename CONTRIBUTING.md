# Contributing to Awesome Agentic *Anything*

Thanks for helping curate this list! The value of an awesome list is its **standards**, not its length. Please read the bar below before opening a PR.

## The Bar: What Counts as "Agentic"?

This list is **"any domain, but it must be agentic"** — not a catalog of every AI project.

### For a *system* (any section under 🌐 Agentic ∀ Domains)

It should exhibit **most** of these traits:

- **Autonomy** — decides its own next step rather than following a hard-coded script.
- **Tool use** — calls tools, APIs, or code execution to affect its environment.
- **Perception–action loop** — observes → reasons → acts → observes again.
- **Goal-directedness** — decomposes a high-level goal into sub-tasks itself.
- **Memory / state** — carries state across steps.

**Not accepted:** base models (GPT, Claude, Llama), single-turn LLM apps, plain RAG Q&A, and pure DAG/workflow tools with no agentic decision-making.

### For *infrastructure* (🏗️ Building Blocks & Infrastructure)

These are not agents themselves, so the test is different: the project must be **purpose-built for agents** — an agent framework, an agent protocol, an agent memory layer, or an agent-focused benchmark. A general-purpose tool that agents happen to use (a generic vector DB, a generic HTTP client) does **not** qualify.

## Format

Every entry is a single line:

```markdown
- [Name](https://link) — One honest sentence describing what it does.
```

Guidelines:

- **One sentence, honest.** No marketing. Say what it actually does.
- **Put it in the right layer.** A framework goes under Building Blocks; a working agent goes under a Domain.
- **Pick the most specific domain.** If it's a coding agent, it goes under Agentic Coding, not General-Purpose.
- **Rough ordering by relevance/adoption** within each section, but don't agonize over it.
- **Link to the canonical source** — the GitHub repo, or the official site/docs for closed-source products.
- **No dead links.** Check the link resolves before submitting.

## Finding Entries

Don't rank purely by stars — that systematically hides new and niche projects. When curating, also search **by name and concept** (e.g. `agent-native`, `*-anything`, protocol/benchmark names), not just "top agent frameworks". Small but conceptually central projects belong here too.

## Adding a New Domain

"Anything" means the domain list grows. If you're adding an agentic system in a domain we don't have yet (legal, medical, gaming, security, DevOps…), feel free to propose a new `### 🔖 Agentic X` subsection. Add at least one solid entry with it, and update the [Contents](README.md#contents) table.

## Process

1. Fork and create a branch.
2. Edit `README.md` (and the Contents list if you added/renamed a section).
3. Open a PR with a short rationale: which section, and why it meets the bar.
4. One project per line; group related PRs where it makes sense.

Maintainers may ask for edits to descriptions or move an entry to a better-fitting section. Borderline cases will be discussed in the PR — err toward "is this actually agentic?"
