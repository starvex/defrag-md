# Changelog

## v2.0 (2026-04-05)

### New Features
- **Agent DNA** (`agent-dna.json`) — Procedural memory that evolves with each defrag cycle. Tracks behavioral patterns, strengthens successful strategies, prunes ineffective ones.
- **Episodic Memory** — Extracts discrete experiences with context, outcomes, and lessons. Not just facts but *stories*.
- **Dream Synthesis** — Creative cross-pollination of ideas inspired by REM sleep. Connects experiences across projects and days.
- **Reflection** — Meta-cognitive self-assessment after each cycle. What's improving? Where to focus?
- **Validation Pipeline** — JSON schema validation, content overlap scoring, automatic rollback on failures. Every run produces auditable metrics in `defrag-history.jsonl`.
- **4-Phase Architecture** — Clear separation: COLLECT (deterministic) → THINK (LLM) → VALIDATE → APPLY (deterministic). Only Phase 2 uses LLM tokens.

### Improved
- **DEFRAG_TEMPLATE.md** — Complete v2.0 instructions including DNA, episodes, dream, reflection, and validation
- **README.md** — Real production metrics from 24 consecutive nightly runs (100% pass rate, 91% compression)
- **Metrics format** — Machine-readable `defrag-history.jsonl` with overlap_pct, episode count, DNA mutations

### Production Stats (24 runs, March–April 2026)
- Validation pass rate: 100%
- Average compression: 91% (152 KB → 14 KB)
- Average episodes per night: 5.0
- Average DNA mutations: 3.7
- Dream + Reflection: 100% of runs

## v1.0 (2026-01-30)

### Initial Release
- 5-tier memory hierarchy (Working → Short-term → Long-term → Project → Procedural)
- Nightly defrag cycle (6 phases: Scan → Consolidate → Archive → Clean → Structure → Log)
- On-demand nap mode
- DEFRAG_TEMPLATE.md drop-in file
- Whitepaper and research documentation
- Website at defrag.md
