# DEFRAG.md — Memory Consolidation Protocol
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
3. **Clean up** automatically (nightly defrag + on-demand naps)
4. **Stay fast** by keeping context lean and relevant

---

## 📁 Memory File Structure

Create these files in your workspace:

```
workspace/
├── DEFRAG.md              # This file (protocol instructions)
├── MEMORY.md              # Long-term memory (~60 lines max)
├── AGENTS.md              # Agent identity & procedures
├── memory/
│   ├── YYYY-MM-DD.md     # Daily session notes (auto-created)
│   ├── defrag-log.md     # Consolidation history
│   └── archive/          # Monthly summaries
└── projects/
    └── */PROJECT.md      # Project-specific memory
```

---

## 📋 Instructions for Agent

### On Session Start
1. Read `MEMORY.md` — this is your long-term memory
2. Read `AGENTS.md` — this is who you are
3. Read `memory/YYYY-MM-DD.md` for today (create if missing)
4. Read yesterday's notes if today's is empty

### During Session
- Write important events to `memory/YYYY-MM-DD.md`
- When user says "remember" or "важно" → write to daily notes immediately
- When you learn something significant → update `MEMORY.md`
- When you complete a project milestone → update relevant `PROJECT.md`

### 🌙 Nightly Defrag (Full Consolidation)

Run this cycle on schedule (recommended: 2-3 AM local time):

**Phase 1 — Scan**: Read ALL `memory/*.md` files from the past 7 days.

**Phase 2 — Consolidate**: Extract important patterns, decisions, and lessons.
Move significant findings to `MEMORY.md`.

**Phase 3 — Archive**: Compress daily notes older than 7 days into
`memory/archive/YYYY-MM.md` monthly summaries.

**Phase 4 — Clean**: Remove duplicates, outdated info, and verbose details
from `MEMORY.md`. Keep it under 60 lines.

**Phase 5 — Structure**: Ensure all memory files are well-organized.
`MEMORY.md` should have clear sections: User Context, Projects, Lessons Learned.

**Phase 6 — Log**: Append what changed to `memory/defrag-log.md`:
```
## YYYY-MM-DD HH:MM — Defrag Complete
- Consolidated: [what was moved to MEMORY.md]
- Archived: [which daily notes were compressed]
- Cleaned: [what was removed/updated]
- MEMORY.md: XX lines (target: <60)
🧠💾 defrag.md protocol
```

### 💤 Nap (Quick Optimization)

Trigger when context exceeds 75% capacity or on user request:

1. **Trim** verbose content from current conversation
2. **Summarize** recent work into essential bullet points
3. **Move** completed items to daily notes
4. **Target**: Free 20-30% of context space in under 60 seconds

### Memory Rules
- `MEMORY.md` = curated, max ~60 lines. Quality over quantity.
- Daily notes = raw, unfiltered. Everything goes here first.
- Projects get their own `PROJECT.md` — prevents context bleed.
- When in doubt, WRITE IT DOWN. Files > "mental notes."
- Old info that's no longer relevant → remove during defrag.

---

## 🔗 Learn More

- **Full Whitepaper**: https://defrag.md/whitepaper
- **GitHub**: https://github.com/defrag-protocol
- **Sister Protocol**: https://synapse.md (multi-agent memory sharing)

---

## 📊 Expected Results

Agents using the Defrag Protocol typically see:
- **5× longer** productive sessions
- **Zero** context overflow failures  
- **88%** memory accuracy retained at 30 days
- **85%** reduction in token waste

---

*The Defrag Protocol is open source (CC BY 4.0). 
Copy this file. Modify it. Share it. Make your agents remember.*

*defrag.md — Because AI shouldn't have amnesia.*
