# Memory in the LLM Era: Modular Architectures and Strategies in a Unified Framework

- **Link:** https://arxiv.org/abs/2604.01707
- **HTML:** https://arxiv.org/html/2604.01707v1
- **Date:** 2026-04-02

## TL;DR
- Argues memory is the core module for long-horizon agents.
- Provides a **unified framework** to compare many memory methods under consistent settings.
- Runs comparative experiments on representative methods and benchmarks.
- Claims a new hybrid method (composed from existing modules) that outperforms prior SOTA.

## Why it matters
Builders need “which memory method should I pick?” guidance. This paper’s value is:
- apples-to-apples comparisons
- identifying which modules actually move the needle

## What to try
- Treat memory as a set of modules: write policy, store, retrieve policy, summarize/compress, forget.
- Reproduce the “simple baselines” first; many systems win by better write policies, not fancier stores.

## Caveats
- Always check what benchmarks were used; performance can be benchmark-specific.
