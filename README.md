# defrag.md

> Sleep-Inspired Memory Management for AI Agents

[![Website](https://img.shields.io/badge/Website-defrag.md-blue)](https://defrag.md)
[![License](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey)](LICENSE)

## The Problem

AI agents have amnesia. Every session starts from zero. No memory of yesterday's breakthroughs. No record of last week's decisions.

## The Solution

The Defrag Protocol implements hierarchical memory tiers modeled on human cognition:

```
Working Memory    → Context Window (active processing)
Short-term Memory → memory/YYYY-MM-DD.md (daily notes)
Long-term Memory  → MEMORY.md (curated essence, ~60 lines)
Project Memory    → PROJECT.md (domain-specific knowledge)
Procedural Memory → AGENTS.md (identity, skills, behaviors)
```

Two consolidation modes:

- **🌙 Defrag (Nightly)**: Deep consolidation at 2:30 AM — scan, extract, archive, clean
- **💤 Nap (On-Demand)**: Quick context optimization — trim, summarize, recover space

## Results

| Metric | Before | After |
|--------|--------|-------|
| Session Length | 47 min | 4.7 hours (5×) |
| Re-explanation Time | 3.7 hrs/week | 0.4 hrs/week (89% ↓) |
| Tokens per Task | 8,666 | 1,234 (85% ↓) |
| Context Overflows | Frequent | 0 |

## Quick Start

1. **Download DEFRAG.md** — Drop it in your workspace root
2. **Create memory structure** — `memory/`, `MEMORY.md`, `AGENTS.md`
3. **Schedule nightly defrag** — Cron at 2:30 AM
4. **Enable nap triggers** — Auto at 75% context capacity

See the [full guide](https://defrag.md/guide) for detailed setup.

## Part of Agent Brain Architecture

- **[defrag.md](https://defrag.md)** — Sleep & consolidation (this protocol)
- **[hippocampus.md](https://hippocampus.md)** — Context lifecycle management
- **[synapse.md](https://synapse.md)** — Multi-agent memory sharing
- **[neocortex.md](https://neocortex.md)** — Long-term memory format

## Resources

- 📖 [Guide](https://defrag.md/guide)
- 📄 [Whitepaper](https://defrag.md/whitepaper)
- 🧠 [DEFRAG_TEMPLATE.md](DEFRAG_TEMPLATE.md)

## License

Creative Commons Attribution 4.0 International (CC BY 4.0)

---

*By Roman Godz & R2D2*
