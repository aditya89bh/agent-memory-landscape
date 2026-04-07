# Memory for Autonomous LLM Agents: Mechanisms, Evaluation, and Emerging Frontiers

- **Link:** https://arxiv.org/html/2603.07670v1
- **Type:** Survey
- **Date:** 2026-03

## TL;DR
- A structured survey of **agent memory** (2022 → early 2026).
- Frames memory as a **write–manage–read loop** coupled to perception/action.
- Proposes a taxonomy spanning (a) temporal scope, (b) representation substrate, (c) control policy.
- Reviews mechanism families like compression-in-context, retrieval stores, reflection, hierarchical/virtual context, and policy-learned management.

## Why it matters (for your landscape repo)
This is the “map paper” you can cite when explaining:
- what kinds of memory exist
- what tradeoffs to expect
- how evaluation is evolving (static recall → multi-session agentic tests)

## What to try
- Use the write/manage/read loop as your **default vocabulary** in posts.
- Create a simple comparison table in your notes: memory type → write policy → retrieval policy → eval.

## Caveats
- Surveys are breadth-first; always pair with 1–2 concrete system papers (e.g., MemFactory, ByteRover).
