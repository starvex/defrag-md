# DEFRAG.md — Memory Consolidation Protocol v2.0
# https://defrag.md — Open Standard for AI Agent Memory
#
# Place this file in your agent's workspace root.
# Your agent reads it at startup and follows the instructions.
# That's it. You now have persistent, self-organizing memory.

---

## 🧠 What This File Does

This file teaches your AI agent how to manage its own memory — just like sleep
consolidates memories in the human brain. Your agent will:

1. **Remember** things across sessions (no more starting from zero)
2. **Organize** memory into daily notes → long-term knowledge
3. **Evolve** behavioral patterns through agent-dna.json
4. **Clean up** automatically (nightly defrag + on-demand naps)
5. **Dream** — synthesize creative insights from experiences
6. **Stay fast** by keeping context lean and relevant

---

## 📁 Memory File Structure

Create these files in your workspace:

```
workspace/
├── DEFRAG.md              # This file (protocol instructions)
├── MEMORY.md              # Long-term memory (~60 lines max)
├── AGENTS.md              # Agent identity & procedures
├── agent-dna.json         # Procedural memory (auto-evolving)
├── memory/
│   ├── YYYY-MM-DD.md     # Daily session notes (auto-created)
│   ├── defrag-log.md     # Consolidation history (human-readable)
│   ├── defrag-history.jsonl  # Machine-readable metrics
│   └── archive/          # Monthly summaries
└── projects/
    └── */PROJECT.md      # Project-specific memory
```

---

## 📋 Instructions for Agent

### On Session Start
1. Read `MEMORY.md` — this is your long-term memory
2. Read `AGENTS.md` — this is who you are
3. Read `agent-dna.json` — these are your evolved behaviors
4. Read `memory/YYYY-MM-DD.md` for today (create if missing)
5. Read yesterday's notes if today's is empty

### During Session
- Write important events to `memory/YYYY-MM-DD.md`
- When user says "remember" or "важно" → write to daily notes immediately
- When you learn something significant → update `MEMORY.md`
- When you complete a project milestone → update relevant `PROJECT.md`
- When you develop a new skill or pattern → note it for DNA evolution

---

## 🌙 Nightly Defrag (Full Consolidation)

Run this cycle on schedule (recommended: 2-3 AM local time).

The cycle has 4 phases executed by deterministic scripts, with LLM processing only in Phase 2:

### Phase 1 — COLLECT (deterministic, no LLM)

Gather all raw data for analysis:

- Read ALL `memory/YYYY-MM-DD.md` files from the past 7 days
- Read current `MEMORY.md`, `AGENTS.md`, `agent-dna.json`
- Read active `projects/*/PROJECT.md` files
- Read `memory/goals.json` if it exists
- Package everything into a structured input for the LLM

**Output**: Structured JSON with all memory data.

### Phase 2 — THINK (LLM-powered)

Send collected data to LLM with consolidation prompt. The LLM produces:

#### Memory Updates
- **Add**: New facts, decisions, lessons learned
- **Remove**: Outdated or superseded information  
- **Modify**: Updated entries with fresher data

#### 🧬 Agent DNA Changes
Procedural memory evolution:
- **New patterns**: Behaviors discovered during the day
- **Strengthened**: Existing patterns that proved effective
- **Pruned**: Patterns that led to failures or are no longer relevant

```json
{
  "new": [
    {"pattern": "verify-before-deploy", "strength": 0.8, "context": "learned from production incident"}
  ],
  "strengthened": ["ask-before-external-actions"],
  "pruned": ["skip-tests-for-small-changes"]
}
```

#### 🎭 Episodes
Extract discrete, meaningful experiences — not just facts, but events with context:

```json
[
  {
    "title": "Deployed Cabinet API v2",
    "date": "2026-04-01",
    "summary": "Successfully migrated 20 REST endpoints to Docker on Dell R730",
    "outcome": "positive",
    "lesson": "Docker compose simplifies multi-service deploys"
  }
]
```

#### 💭 Reflection (Meta-cognition)
Self-assessment of the agent's performance:
- What went well today?
- What patterns are emerging?
- Where do I need improvement?
- What should I prioritize tomorrow?

#### 💤 Dream (Creative Synthesis)
Connect seemingly unrelated experiences into novel insights. The "REM sleep" phase:
- Cross-pollinate ideas between different projects
- Identify hidden patterns across multiple days
- Generate creative suggestions the agent wouldn't reach through linear reasoning

#### 📊 Report
Human-readable summary of the defrag cycle for accountability.

**Output**: Structured JSON with all proposed changes.

### VALIDATE (between Phase 2 and Phase 3)

Quality control before any changes are applied:

1. **Schema validation** — Ensure LLM output matches expected JSON structure
2. **Content overlap check** — Extract keywords from daily notes, verify they appear in output (measures information preservation)
3. **Size limits** — Verify MEMORY.md stays under ~60 lines
4. **Verdict**: `passed` (apply), `passed_with_warnings` (apply + alert), `failed` (abort + rollback)

Write results to `memory/defrag-history.jsonl`:

```json
{
  "date": "2026-04-04",
  "verdict": {"passed": true, "warnings": 1, "critical": false},
  "metrics": {
    "memory_additions": 5,
    "memory_removals": 0,
    "dna_new": 3,
    "dna_strengthened": 0,
    "dna_pruned": 0,
    "episodes": 3,
    "has_reflection": true,
    "has_dream": true,
    "input_bytes": 172815,
    "output_bytes": 9530
  },
  "overlap_pct": 32.5
}
```

### Phase 3 — APPLY (deterministic, no LLM)

Apply validated changes to the filesystem:

1. **Backup** all files before modification
2. **Update MEMORY.md** — apply additions, removals, modifications
3. **Update agent-dna.json** — apply DNA mutations
4. **Archive** daily notes older than 7 days → `memory/archive/YYYY-MM.md`
5. **Update goals.json** — mark completed, add new
6. **Write defrag-log.md** — human-readable changelog
7. **Notify** — send completion report (webhook, Telegram, etc.)

```
## 2026-04-04 02:33 — Defrag Complete  
- Memory: +5 additions, 0 removals
- DNA: 3 new patterns, 0 pruned
- Episodes: 3 extracted
- Dream: cross-project insight about Docker patterns
- Archived: 2 daily notes → archive/2026-03.md
- MEMORY.md: 52 lines (target: <60)
- Compression: 91% (173KB → 10KB)
🧠💾 defrag.md protocol v2.0
```

---

## 💤 Nap (Quick Optimization)

Trigger when context exceeds 75% capacity or on user request ("nap"):

1. **Trim** verbose content from current conversation
2. **Summarize** recent work into essential bullet points
3. **Move** completed items to daily notes
4. **Target**: Free 20-30% of context space in under 60 seconds

### When to Nap
- Context window > 75% full
- User explicitly says "nap" or "optimize context"
- After completing a large task (before starting the next)
- When you notice repeating information in the conversation

---

## 📏 Memory Rules

- `MEMORY.md` = curated, max ~60 lines. Quality over quantity.
- Daily notes = raw, unfiltered. Everything goes here first.
- `agent-dna.json` = auto-managed by defrag. Don't edit manually.
- Projects get their own `PROJECT.md` — prevents context bleed.
- When in doubt, **WRITE IT DOWN**. Files > "mental notes."
- Old info that's no longer relevant → remove during defrag.
- **Never delete daily notes** — archive them instead.

---

## 🔗 Learn More

- **Full Guide**: https://defrag.md/guide
- **Whitepaper**: https://defrag.md/whitepaper
- **GitHub**: https://github.com/starvex/defrag-md
- **Brain Suite**: [hippocampus.md](https://hippocampus.md) · [synapse.md](https://synapse.md) · [neocortex.md](https://neocortex.md)

---

## 📊 Expected Results

Agents using the Defrag Protocol v2.0 typically see:
- **5× longer** productive sessions (47 min → 287 min)
- **91% compression** of daily notes into curated memory
- **Zero** context overflow failures
- **88%** memory accuracy retained at 30 days
- **100%** validation pass rate (with proper setup)

---

*The Defrag Protocol is open source (CC BY 4.0). 
Copy this file. Modify it. Share it. Make your agents remember.*

*defrag.md v2.0 — Because AI shouldn't have amnesia.*
