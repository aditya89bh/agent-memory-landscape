# MemoryCD: Benchmarking Long-Context User Memory of LLM Agents for Lifelong Cross-Domain Personalization

- **Link:** https://arxiv.org/html/2603.25973
- **Date:** 2026-03
- **Code:** https://github.com/AgentMemoryWorld/MemoryCD

## TL;DR
- Introduces a user-centric benchmark for **lifelong, cross-domain personalization** memory.
- Built from real long-horizon behavior (Amazon Reviews) across multiple domains.
- Evaluates LLMs + memory baselines on personalization tasks over long histories.

## Why it matters
Most “memory” eval is synthetic dialogue. MemoryCD is closer to what real assistants need: preferences and history across time + domains.

## What to try
1) Adopt MemoryCD-style tasks for your own eval: preference recall, cross-domain consistency, staleness.
2) Track failure types separately: wrong recall vs stale recall vs over-personalization.

## Caveats
- Benchmark ≠ solution; it mainly tells you what breaks.
- Real user data introduces bias; interpret scores carefully.
