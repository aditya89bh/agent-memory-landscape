# Multi-Layered Memory Architectures for LLM Agents: An Experimental Evaluation of Long-Term Context Retention

- **Link:** https://arxiv.org/html/2603.29194
- **Year:** 2026

## TL;DR (3 bullets)
- Splits memory into **working / episodic / semantic** layers to keep context bounded but retain long-horizon info.
- Uses **adaptive retrieval gating** so the model doesn’t always pull everything.
- Adds a **retention regularization** objective to reduce semantic drift and false memories across sessions.

## What’s actually new
- A concrete *experimental* framing for multi-layer memory with drift control + retrieval gating (not just “store summaries”).
- Explicit attention to **false memory rate** + context usage, not just accuracy.

## Key mechanism (concept)
- Working memory: recent turns (small window)
- Episodic memory: per-session summaries
- Semantic memory: entity/fact abstractions
- Gating: weighted mix of layers at retrieval time

## What to try (1–2 experiments)
1) Implement a 3-layer store in your agent and compare:
   - retrieve from all layers vs gated retrieval
2) Track **false memory rate** by inserting “trap facts” that should never be recalled.

## Failure modes / caveats
- If write policies are weak, episodic/semantic layers can become a garbage amplifier.
- Benchmarks are dialogue-centric; tool-using agents may behave differently.
