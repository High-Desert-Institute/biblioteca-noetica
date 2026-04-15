# AGENTS Instructions

Canonical policy source for this repository is `./agents/RULES.md`.
Read `./agents/RULES.md` in full before performing work.

Runtime artifact preference from host root:
- use host-managed `./playbooks/`, `./references/`, `./templates/`, `./scripts/` when present,
- otherwise fall back to `./agents/playbooks/`, `./agents/references/`, `./agents/templates/`, `./agents/scripts/`.

For host-owned plan index operations, run:
- `python agents/scripts/regenerate_plan_indexes.py --repo-root .`
