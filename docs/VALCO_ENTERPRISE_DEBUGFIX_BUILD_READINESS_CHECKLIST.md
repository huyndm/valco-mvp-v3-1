# ValCo Enterprise DebugFix Build Readiness Checklist V3.1

## TSSS Candidate Pool
- [ ] Raw candidate pool supports up to 1,000 records.
- [ ] Deduplication step exists before hard filter.
- [ ] FreeLLMAPI extraction does not choose final 3.
- [ ] Hard filter service exists.
- [ ] Eligible pool exists.
- [ ] Top 10 recommendation exists.
- [ ] Analyst-selected final 3 exists.
- [ ] Insufficient data handling exists.

## Backend Debug/Fix
- [ ] Ruff configured.
- [ ] Pytest configured.
- [ ] Gateway tests exist.
- [ ] Candidate pool/dedup/hard filter/ranking/final selection tests exist.
- [ ] Export tests exist.
- [ ] No-direct-provider grep/test exists.

## UI Debug/Fix
- [ ] Vitest configured.
- [ ] React Testing Library configured.
- [ ] Storybook stories exist for raw pool/Top10/final3 components.
- [ ] Playwright E2E smoke exists.
- [ ] TanStack Devtools dev-only configured or documented.
