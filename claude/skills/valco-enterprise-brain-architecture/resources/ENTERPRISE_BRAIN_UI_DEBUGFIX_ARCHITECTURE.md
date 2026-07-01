# ValCo Enterprise Brain + UI DebugFix Architecture V3.1

## Purpose
Build full internal ValCo system supporting TSSS processing, TSSS raw candidate pool up to 1,000 records, evidence collection, FS checking, document/RAG knowledge base, export review, analyst-facing UI, and repeatable debug/fix loop.

## TSSS Candidate Pipeline V3.1
```text
TSĐG input
→ raw candidate search up to 1,000 records
→ deduplicate
→ FreeLLMAPI-assisted extraction/normalization
→ hard filter
→ eligible pool
→ deterministic scoring/ranking
→ Top 10 recommended TSSS
→ analyst/user selects final 3 main TSSS
→ export/audit
```

## Target Architecture
```text
Claude Code Builder Layer
→ ValCo app source code
→ FastAPI backend
→ SQLModel ORM
→ SQLite MVP / PostgreSQL production
→ FreeLLMAPI runtime gateway
→ Crawler layer: Crawl4AI + Playwright Python fallback
→ Enterprise Brain: PydanticAI structured extraction + LangGraph-style workflow + LlamaIndex/RAGFlow-style RAG
→ Optional vector store: Qdrant/Chroma
→ Export layer: Excel/Word/audit markdown
→ Observability: Langfuse + OpenTelemetry + optional Sentry
→ Backend QA: pytest + ruff + gateway/scoring/export tests
→ React dashboard: shadcn-admin + TanStack Query/Router/Table/Form/Virtual + React Flow workflow editor
→ Frontend QA: Vitest + React Testing Library + Storybook + Playwright E2E + TanStack Devtools
```
