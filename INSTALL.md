# Global Installation

To activate `token-optimizer` globally in every session:

1. Copy `SKILL.md` to your skills folder: `C:\Users\Usuario\.config\opencode\skills\token-optimizer\SKILL.md`.
2. Update `opencode.json`:
```json
"instructions": [
  "skills/token-optimizer/SKILL.md",
  ...
]
```
3. (Optional) Force persistence in `INSTRUCTIONS.md`:
```markdown
> PERSISTENCIA NINECODE: ALWAYS load and adhere to `skills/token-optimizer/SKILL.md`.
```
