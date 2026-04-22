# AGENTS.md — Superpowers for Knowledge Work

Canonical repo instructions for `superpowers-knowledge-plugin`.

## Project Identity

- **Name:** superpowers-knowledge
- **Type:** Host-agnostic methodology skills repo with Claude plugin packaging compatibility
- **Version:** 0.5.0
- **Stack:** Markdown skills + upstream-tracking docs + lightweight install scripts

## Canonical Structure

```
superpowers-knowledge-plugin/
├── .claude-plugin/
│   ├── plugin.json          # Claude plugin packaging metadata
│   └── marketplace.json     # Claude marketplace listing
├── skills/
│   ├── brainstorming/
│   ├── executing-plans/
│   ├── feedback-reception/
│   ├── parallel-work/
│   ├── systematic-problem-solving/
│   ├── two-stage-review/
│   ├── using-superpowers/
│   ├── verification-before-completion/
│   ├── writing-plans/
│   └── writing-skills/
├── scripts/
│   ├── install_codex_skills.sh
│   └── update_codex_skills.sh
├── AGENTS.md                # Canonical repo instructions
├── CLAUDE.md                # Claude compatibility wrapper
├── CHANGELOG.md
├── DECISIONS.md
├── ROADMAP.md
├── README.md
└── UPSTREAM.md
```

## Canonical Rules

- `AGENTS.md` is the canonical instruction file for this repo.
- `CLAUDE.md` is a thin compatibility wrapper that points Claude-family hosts back to `AGENTS.md`.
- `skills/` is the canonical source of shared methodology.
- `.claude-plugin/` is Claude-specific packaging metadata, not the source of truth for the skills themselves.
- Preserve coexistence with official Superpowers by keeping domain-routing language intact.

## Runtime Conventions

- Resolve repo-local reference files from a portable root variable:
  `SUPERPOWERS_KNOWLEDGE_ROOT="${SUPERPOWERS_KNOWLEDGE_ROOT:-${CLAUDE_PLUGIN_ROOT:-${CODEX_HOME:-$HOME/.codex}/vendor_imports/repos/superpowers-knowledge-plugin}}"`
- Use that root for `skills/.../references/` lookups instead of assuming Claude-only runtime paths.
- Keep skills pure markdown with no runtime code requirements.

## Documentation Rules

- README.md is human-facing.
- AGENTS.md is the canonical agent-facing document.
- CLAUDE.md exists for compatibility only and should stay short.
- DECISIONS.md logs major structural choices before implementation.
- ROADMAP.md holds future ideas until they become decisions.
- CHANGELOG.md records narrative milestones after significant work.
- UPSTREAM.md is the source of truth for upstream sync history and adoption logic.

## Design Principles

1. **Methodology over improvisation** — preserve the Iron Laws and verification discipline.
2. **Compatibility layers, not duplicate sources** — host-specific files should point to canonical files.
3. **Cross-host portability** — the same methodology should work in Claude, Codex, Cursor, and similar hosts.
4. **Coexistence by domain** — upstream Superpowers handles code work; this plugin handles knowledge work.
5. **Deliberate fork maintenance** — upstream changes should be reviewed, not blindly mirrored.

## Boundaries

### Do
- Keep skill descriptions domain-scoped for knowledge work
- Update UPSTREAM.md when syncing with upstream
- Update docs and metadata together when conventions change
- Preserve references that explain fork rationale and coexistence

### Don't
- Reintroduce `CLAUDE.md` as the canonical repo instruction file
- Collapse this plugin back into a host-specific identity
- Remove the coexistence framing with official Superpowers
- Add runtime dependencies for packaging or skill execution
