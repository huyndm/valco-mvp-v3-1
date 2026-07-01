# CLAUDE.md — ValCo Enterprise Brain + UI DebugFix Integrated V3.1

Always follow `.claude/rules/VALCO_MASTER_RULEBOOK.md`.

## Critical Rule
**Claude Code is builder only; FreeLLMAPI is runtime inference engine.**

## Anti-Linh-Tinh Clarification Protocol
Do not ask unnecessary broad questions. Proceed with safe MVP defaults when possible. Ask only for truly blocking decisions.

## TSSS Candidate Pool Rule V3.1
Do not assume 1,000 raw candidates are qualified. Build pipeline:
```text
raw candidate search up to 1,000 → deduplicate → FreeLLMAPI extraction/normalization → hard filter → eligible pool → Top 10 recommended → analyst/user final 3 → export/audit
```
FreeLLMAPI extracts and normalizes; deterministic code filters/scores; analyst/user selects final 3.

## Valuation Build Guardrail
Build valuation as deterministic pipeline + analyst review. LLM extracts and drafts; it does not decide final value. Preserve evidence, apply comparable-selection order, control adjustment under 40%, avoid double land-type adjustment, and expose all assumptions in config.

## DebugFix Gate
Every build/change must pass or report: backend lint/test, frontend test, UI component/E2E smoke, no-direct-provider checks, deterministic valuation guardrail tests, TSSS candidate pool tests, and runtime observability hooks.
