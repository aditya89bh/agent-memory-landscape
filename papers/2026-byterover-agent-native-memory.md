# ByteRover: Agent-Native Memory Through LLM-Curated Hierarchical Context

- **Link:** https://arxiv.org/html/2604.01599
- **Date:** 2026-04 (early)

## TL;DR
- Argues that the usual “external memory service” (chunk/embed/graph) creates **semantic drift**.
- Proposes making memory **agent-native**: the *same LLM* curates, structures, and retrieves what it stores.
- Represents knowledge as a hierarchical **Context Tree** (curated structure, not just vectors).

## Why it matters
This matches what builders see: memory isn’t just retrieval—it’s **what you wrote**. If a pipeline stores the wrong thing, retrieval can’t save you.

## What to try
1) Replace raw chunking with an LLM “curation” step:
   - store: (claim, source, time, entity)
2) Build a simple tree/hierarchy (topic → entity → facts) and retrieve top branches.

## Caveats
- Agent-native curation adds extra LLM calls; caching/latency can dominate.
- Quality depends heavily on the backbone model.
