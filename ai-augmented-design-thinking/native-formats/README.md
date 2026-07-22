# Native Formats (planned)

> Tool-specific wrappers for the phase agents. **Not built yet, this is a placeholder documenting the plan.**

## Why this exists

Each phase in this repo ships a portable, tool-agnostic `AGENT.md` (a copy-paste system prompt that works anywhere). That's the **source of truth**.

This folder will hold *thin wrappers* that let specific AI tools invoke those agents natively (auto-trigger by name instead of pasting). The wrappers reference the canonical `AGENT.md` system prompt rather than duplicating it, so the agent logic lives in exactly one place.

## Planned targets

| Tool | Native mechanism | Status |
| --- | --- | --- |
| Claude Code | Subagent / skill definition | 🔲 Planned |
| Cursor | Project rule (`.mdc`) | 🔲 Planned |
| Windsurf | Workflow / rules file | 🔲 Planned |
| opencode | Agent config | 🔲 Planned |

*(Native formats evolve. Each will be verified against the tool's current spec at build time, not from memory.)*

## Design principle: single source of truth

```
phase/AGENT.md   ← canonical system prompt (edit here)
      │
      ├── native-formats/claude-code/...   ← thin wrapper, points to AGENT.md
      ├── native-formats/cursor/...        ← thin wrapper
      ├── native-formats/windsurf/...      ← thin wrapper
      └── native-formats/opencode/...      ← thin wrapper
```

When an agent's behavior changes, edit the phase's `AGENT.md`. Wrappers carry only tool-specific glue (naming, invocation, file placement), which rarely changes.

## Build order

1. ✅ Finish all 8 phase `AGENT.md` files (the source of truth).
2. 🔲 Prove native wrappers on ONE phase (Understand) across the four tools.
3. 🔲 Roll out to remaining phases once the pattern holds.
