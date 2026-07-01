# ValCo Claude Code — Enterprise Brain + UI DebugFix Integrated V3.1

## Critical Rule
Claude Code is builder only; FreeLLMAPI is runtime inference engine.

## V3.1 TSSS Candidate Pool Rule
```text
Raw candidate search up to 1,000 → dedup → FreeLLMAPI extraction/normalization → hard filter → eligible pool → Top 10 recommended → analyst/user selects final 3 → export/audit
```

## Strict build without unnecessary questions
```text
/project:valco-build-without-linh-tinh
```

## Build TSSS pool module
```text
/project:build-valco-tsss-candidate-pool
```

## Audit method
```text
/project:audit-tsss-candidate-pool-method
```

## Debug/Fix Gate
```text
/project:valco-debug-fix-audit
/project:run-full-quality-gate
/project:fix-backend-tests
/project:fix-ui-tests
/project:fix-runtime-errors
/project:fix-ui-component-library
```
