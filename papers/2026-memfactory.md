# MemFactory: Unified Inference & Training Framework for Agent Memory

- **Link:** https://arxiv.org/html/2603.29493
- **Date:** 2026-04-02

## TL;DR
- Proposes a modular, “Lego-like” framework to assemble **memory agent pipelines** from atomic components.
- Treats memory as a lifecycle: **extract → update → retrieve → use** (and potentially train each step).
- Integrates RL-style optimization (e.g., GRPO) to learn memory management policies instead of hand-tuned heuristics.

## Why it matters (builder view)
If memory agents are going to be real products, we need:
- standardized components
- reproducible evaluation
- trainable write/retrieve policies

MemFactory is trying to be the “LLaMA-Factory” layer for memory agents.

## What to try
1) Implement your memory system as explicit modules (writer, retriever, verifier) with clear interfaces.
2) Start with offline evaluation + ablations before any RL fine-tuning.

## Caveats
- Framework papers often look clean; the hard part is **good reward signals** and **robust eval**.
