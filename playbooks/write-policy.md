# Write Policy (What should become memory?)

Memory is a liability unless you control what gets written.

## Default rule

Only write when one of these is true:
1) It will be useful **later** (cross-session), and
2) It is **stable enough** (won’t be invalid in a day), and
3) It can be **proven** (source, tool output, user-confirmed), or explicitly marked as uncertain.

## What to store (high ROI)
- User preferences (confirmed)
- Project state (decisions, constraints, links)
- Outcome summaries (what worked / failed)
- Durable facts with citations

## What not to store
- Raw conversation dumps
- Temporary guesses
- Secrets (tokens, passwords)
- Sensitive personal info unless explicitly requested

## Suggested schema (minimal)
- `type`: preference|decision|fact|episode|task_state
- `text`: the memory
- `source`: user|tool|doc|web
- `confidence`: low|med|high
- `ttl_days`: optional
- `updated_at`
