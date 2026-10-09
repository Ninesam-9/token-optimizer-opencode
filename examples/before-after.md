# Before / After Examples

## Example 1 — Config consolidation (OpenCode, Gemini 3.5 Flash-Lite)

**BEFORE (standard, ~180 tokens):**
> "He leído el archivo opencode.json para entender qué herramientas se están utilizando… Tras el análisis, he identificado que… No he encontrado vulnerabilidades obvias, pero sería recomendable ejecutar un npm audit para estar completamente seguros."

**AFTER (optimizer, ~45 tokens):**
```
[GOAL]: Single source of truth for config.
[STATUS]: Redundancy detected (json + jsonc).
[ACTION]: 1. Merge unique fields. 2. rm opencode.jsonc.
[CAUTION]: 1. Comment loss. 2. Schema drift.
[VERIFY]: opencode --print-config
```

## Example 2 — Security audit

**BEFORE (~102 words):** full-paragraph explanation of wildcard `bash: *` + external directory access, narrative risk description, generic recommendation.

**AFTER (~22 words):**
```
[GOAL]: Close wildcard exec risk.
[STATUS]: bash `*`=allow, external_dirs `*`=allow.
[ACTION]: Scope bash allowlist + pin 2 project dirs.
[CAUTION]: 1. Breaks ad-hoc scripts. 2. MCP needs re-auth.
[VERIFY]: grep -A5 '"bash"' opencode.json
```
