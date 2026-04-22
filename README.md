# Superpowers for Knowledge Work

Structured workflow discipline for creative, business, and strategic knowledge work. A deliberate fork of Jesse Vincent's [Superpowers](https://github.com/obra/superpowers), adapted for non-code contexts and designed to coexist cleanly with the upstream plugin by routing on domain.

## What It Does

Stops agents from winging knowledge work. Enforces a disciplined pipeline:

`brainstorm -> plan -> execute -> review -> verify`

Every deliverable gets explored before execution, planned before work begins, reviewed against its brief, and verified with evidence before being called done.

## Skills

| Skill | Purpose |
|---|---|
| `using-superpowers` | Meta-skill backbone governing the whole system |
| `brainstorming` | Explore before execution |
| `writing-plans` | Break work into concrete tasks |
| `executing-plans` | Execute approved plans with checkpoints |
| `verification-before-completion` | Evidence gate before any done claim |
| `systematic-problem-solving` | Root-cause analysis for stuck situations |
| `two-stage-review` | Spec compliance first, quality second |
| `feedback-reception` | Evaluate feedback before implementing it |
| `parallel-work` | Dispatch independent tasks concurrently |
| `writing-skills` | Create or refine skills using hypothesis-driven methodology |

## Coexistence with Official Superpowers

This plugin can be installed alongside the official [Superpowers](https://github.com/obra/superpowers) plugin.

- **Official Superpowers** handles software development workflows
- **This plugin** handles creative, strategic, and business knowledge work

The skills are already domain-scoped so the host can route by context. Three skills remain uniquely valuable regardless of configuration:

- `systematic-problem-solving`
- `two-stage-review`
- `feedback-reception`

## Installation

### Claude Code CLI

```bash
claude plugins install github.com/montymerlin/superpowers-knowledge-plugin
```

### Claude Desktop (Cowork)

Install from the marketplace or package the repo for upload:

```bash
zip -r superpowers-knowledge.plugin . -x ".git/*" ".DS_Store"
```

### Codex

```bash
bash scripts/install_codex_skills.sh --from-github
```

### Other Hosts

Clone the repo and load the skill folders according to the host's skill/plugin conventions.

## Upstream Tracking

See [UPSTREAM.md](UPSTREAM.md) for upstream sync history, fork rationale, and adoption criteria.

## Repo Conventions

- `AGENTS.md` is canonical for this repo.
- `CLAUDE.md` is a compatibility wrapper.
- `.claude-plugin/` is packaging metadata, not the source of truth for skill behaviour.
- `UPSTREAM.md` is the source of truth for sync status and lineage decisions.

## License

MIT
