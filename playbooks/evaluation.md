# Evaluation (Did memory help?)

## What to measure

### Outcome metrics
- Task success rate (end-to-end)
- Time-to-success / steps
- User corrections required

### Memory quality metrics
- **False memory rate** (incorrect recalls)
- **Staleness rate** (outdated recalls)
- **Provenance coverage** (% memories with a source)
- **Editability** (can user correct & does it stick?)

### Cost/safety
- Extra tokens / latency due to memory
- Privacy leakage risk (what got stored)

## Minimal eval protocol

1) Define 20–50 tasks with long-horizon dependency (need past info)
2) Run A/B:
   - A: memory OFF
   - B: memory ON
3) Keep everything else identical (tools, model, prompts)
4) Score outcomes + memory errors

## Red flags
- Memory improves “confidence” but not correctness
- Retrieval bloats context and hurts reasoning
- The system stores user data that shouldn’t persist
