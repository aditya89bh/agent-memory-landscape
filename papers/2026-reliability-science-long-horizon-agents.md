# Beyond pass@1: A Reliability Science Framework for Long-Horizon LLM Agents

- **Link:** https://arxiv.org/html/2603.29231v1
- **Date:** 2026-03

## TL;DR
- Distinguishes **capability** (pass@1) from **reliability** (consistent success over repeated runs).
- Shows reliability degrades with task duration and existing benchmarks miss this.
- Proposes reliability metrics for long-horizon agents (e.g., reliability decay, variance amplification, partial credit, meltdown onset).
- Builds a benchmark across task-duration buckets and evaluates multiple models/scaffolds.

## Why it matters for memory agents
Many “memory scaffolds” look good in short demos but:
- accumulate errors
- retrieve stale/wrong memories
- eventually collapse tool behavior

Reliability metrics are how you prove your memory system is not just a highlight reel.

## What to try
- Evaluate your agent by running the same long task N times and measure variance.
- Track “meltdown” signals: tool-call entropy spikes, repeated loops, unrecoverable state.

## Caveats
- Not exclusively about memory, but it’s foundational for any long-horizon memory agent product.
