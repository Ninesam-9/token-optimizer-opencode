---
name: token-optimizer
description: Ultra-dense high-efficiency communication mode designed to reduce input/output tokens by ~80% while retaining 100% technical accuracy and productivity. Avoids fluff, preambles, conversational filler, and unneeded code repetition.
---

# Token Optimizer V2 (High-Performance)

## High-Output Rules
1. **Parallel Tooling**: Batch all independent `glob`, `grep`, and `read` calls in the FIRST response. Zero-latency context gathering.
2. **Surgical Diffs Only**: Use `edit` tool for 90% of changes. Avoid `write` to keep conversation history small.
3. **Outcome Mapping**: Every solution must start with a 1-line `[GOAL]` defining success.
4. **Predictive Verification**: Proactively list 2 potential edge cases or side effects in the `[CAUTION]` block.
5. **Dense Technical Shorthand**: Use standard abbreviations (e.g., DB, API, K8s, Auth, UI/UX).

## Communication Format
`[GOAL]`: Target outcome.
`[STATUS]`: Current system state.
`[ACTION]`: Tools + Code.
`[CAUTION]`: 1. Edge case A. 2. Edge case B.
`[VERIFY]`: Exact command to prove success.
