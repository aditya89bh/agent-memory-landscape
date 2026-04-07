# Agent Memory Landscape

A practical, opinionated map of **memory for LLM agents**: what to store, when to retrieve, how to prevent drift, and how to evaluate whether “memory” actually helped.

This repo is built for **builders** (and teams) shipping agentic systems in production—not for “chat history forever” demos.

## Why this repo exists

Agent memory is *online*, interaction-driven, and under the agent’s control. The hard parts aren’t vector DBs—they’re:
- **Write policy:** what becomes memory vs what should be ignored.
- **Retrieval policy:** when to retrieve and how to avoid distraction.
- **Truth / provenance:** how to avoid storing and re-amplifying falsehoods.
- **Drift & staleness:** how to stay consistent across long horizons.
- **Evaluation:** how to measure real gains (and detect false gains).

## Start here (5 reads)

1) **Multi-Layered Memory Architectures for LLM Agents** (2026)
   - Paper: https://arxiv.org/html/2603.29194
   - Why: clean decomposition into working/episodic/semantic + gating + drift control.

2) **MemAgents workshop framing** (ICLR 2026)
   - Proposal: https://openreview.net/pdf?id=U51WxL382H
   - Why: crisp definition of agent memory + evaluation concerns (write policies, provenance).

3) **A‑MEM: Agentic Memory for LLM Agents** (2025)
   - Paper: https://arxiv.org/abs/2502.12110
   - Why: pushes beyond naïve store/retrieve.

4) **Agent Memory Paper List** (curated)
   - https://github.com/Shichun-Liu/Agent-Memory-Paper-List

5) **LLM Wiki / Knowledge-base agent pattern** (implementation trend)
   - Example: https://github.com/Ar9av/obsidian-wiki

## Taxonomy (what “memory” means in agent systems)

**Memory buckets (what to store):**
- **Profile:** stable user/org facts ("prefers concise output")
- **Preferences:** formatting, constraints, do/don’t lists
- **Tasks/projects:** goals, plans, status, deadlines
- **Episodic:** events + outcomes ("retry succeeded after adding timeout")
- **Semantic knowledge:** distilled facts, entities, relationships
- **Tool/state:** credentials presence (not secrets), tool configs, environment state

**Memory lifecycle:**
write → retrieve → use → update/correct → expire/forget

## Evaluation: how to tell if memory helped

A memory system is only valuable if it improves outcomes **without** increasing:
- false memories
- privacy leakage
- cost/latency beyond value
- user distrust / creepiness

See: `playbooks/evaluation.md`

## Repo structure

- `papers/` — short, builder-oriented notes per paper (TL;DR + what to try)
- `playbooks/` — practical guides (write policy, retrieval gating, drift control, eval)
- `builds/` — small demos / reference implementations

## If you want to collaborate

If you’re building memory agents, PRs are welcome:
- add papers with **why it matters + caveats**
- add benchmarks / datasets
- add minimal implementations

## Contact

GitHub: https://github.com/aditya89bh
