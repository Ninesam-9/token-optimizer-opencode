# Installation (any platform)

## Option A — Any chat AI (ChatGPT, Gemini, Claude, Grok)
1. Copy the fenced block from `UNIVERSAL.md`.
2. Paste into Custom Instructions / System Prompt.
3. Done — output follows `[GOAL]/[STATUS]/[ACTION]/[CAUTION]/[VERIFY]`.

## Option B — Coding agent with workspace rules (Cursor, Windsurf, Copilot, Claude Code)
- Drop `AGENTS.md` in repo root, or merge its content into `CLAUDE.md` / `.cursorrules`.

## Option C — OpenCode (global, every session)
1. Copy `SKILL.md` to your skills folder, e.g. `<opencode-config>/skills/token-optimizer/SKILL.md`.
2. Register it in `opencode.json`:
```json
"instructions": [
  "skills/token-optimizer/SKILL.md",
  ...
]
```
3. (Optional) Force persistence in your core instructions file:
```markdown
> ALWAYS load and adhere to `skills/token-optimizer/SKILL.md`.
```

## Option D — API (any model)
- Send the `UNIVERSAL.md` block as the `system` message.
