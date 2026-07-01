# ValCo TSSS Candidate Pool Method V3.1

## Core Principle
The system does not search for 1,000 already-qualified TSSS. It collects up to 1,000 raw candidates, then deduplicates, extracts, normalizes, hard-filters, scores, and ranks.

## Pipeline
```text
TSĐG input → raw candidate search up to 1,000 records → deduplicate → extraction/normalization → hard filter → eligible pool → Top 10 recommended → analyst selects final 3 → export/audit
```

## Roles
- FreeLLMAPI: extraction, classification, normalization, draft notes.
- Deterministic code: hard filters, scoring, ranking, adjustment control.
- Analyst/user: final 3 TSSS selection and override approval.

## Classes
RAW_CANDIDATE, DUPLICATE, REJECT, REFERENCE, BACKUP, RECOMMENDED_TOP_10, MAIN_SELECTED_3.

## Insufficient Data Rule
- eligible >= 10: present Top 10.
- eligible 6–9: present all eligible and flag limitation.
- eligible 3–5: provisional final 3 only with limitation note.
- eligible < 3: do not force table; expand search or request analyst decision.
