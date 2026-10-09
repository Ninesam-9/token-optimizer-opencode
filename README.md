# Token-Optimizer V2 — Reduce 60–85% Token Usage Without Losing Productivity

![version](https://img.shields.io/badge/version-2.1.0-blue)
![license](https://img.shields.io/badge/license-MIT-green)
![platforms](https://img.shields.io/badge/platforms-OpenCode_%7C_Claude_%7C_Cursor_%7C_ChatGPT_%7C_Gemini_%7C_API-lightgrey)

A drop-in efficiency protocol for AI coding assistants and chat models. It forces **dense, structured, action-first output**: zero fluff, surgical diffs, batched tool calls, explicit success criteria.

- **OpenCode native skill:** `SKILL.md`
- **Universal prompt (any AI):** `UNIVERSAL.md`
- **Workspace rule (Cursor / Copilot / Windsurf / Claude Code):** `AGENTS.md`

## Why

| Problem | Token-Optimizer answer |
|---|---|
| Verbose preambles ("Sure, I'd be happy to help…") | Banned. Tools + code immediately. |
| Full-file echoes on every edit | Surgical diffs only. |
| Sequential one-tool-per-turn loops | Parallel batching mandated. |
| Vague "done" with no proof | Every answer ends with `[VERIFY]` command. |
| Explanations nobody reads | Code first, max 2 bullets. |

## Benchmarks (measured, Gemini 3.5 Flash-Lite)

| Task | Standard (words) | Optimizer (words) | Reduction |
|---|---|---|---|
| Dependency review | ~85 | ~28 | **−67%** |
| Config consolidation | ~180 tok | ~45 tok | **−75%** |
| Security audit | ~102 | ~22 | **−78%** |
| Mean | — | — | **~75%** |

> Real savings vary with base verbosity (typical range 60–85%). Accuracy held constant in all test runs.

## Quickstart (60 seconds)

**Any chat AI (ChatGPT, Gemini, Claude, Grok):**
1. Open `UNIVERSAL.md`, copy the fenced block.
2. Paste into Custom Instructions / System Prompt.
3. Ask anything — output follows `[GOAL]/[STATUS]/[ACTION]/[CAUTION]/[VERIFY]`.

**OpenCode (global, every session):**
1. Copy `SKILL.md` → `<config>/skills/token-optimizer/SKILL.md`.
2. Add to `opencode.json`: `"instructions": ["skills/token-optimizer/SKILL.md", ...]`.
3. Full steps: `INSTALL.md`.

**Cursor / Windsurf / Copilot / Claude Code:**
- Drop `AGENTS.md` in repo root (or merge into `CLAUDE.md` / `.cursorrules`).

## Output contract

```
[GOAL]: 1-line outcome.
[STATUS]: current state.
[ACTION]: steps + code.
[CAUTION]: 1. edge case. 2. edge case.
[VERIFY]: exact command/test to prove success.
```

## Repository layout

```
SKILL.md            OpenCode skill (V2 engine)
UNIVERSAL.md        Copy-paste system prompt for any AI
AGENTS.md           Workspace-level rule for coding agents
INSTALL.md          OpenCode global install guide
examples/before-after.md   Side-by-side comparisons
CHANGELOG.md        Version history
LICENSE             MIT
```

## Examples

See [`examples/before-after.md`](examples/before-after.md) for two full before/after tasks.

## Contributing

PRs welcome: new platform install notes, measured benchmarks (model + word counts), edge-case rules. Keep additions dense — dogfood the protocol.

## License

MIT © 2026 NINECODE. See [LICENSE](LICENSE).
