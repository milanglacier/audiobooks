# audiobooks

Monorepo for my audiobook projects. Each top-level directory is a git
submodule pointing at its own GitHub repo; these are the real dev checkouts.
`CLAUDE.md` is a symlink to this file.

## Submodules

Format: submodule | GitHub repo | has AGENTS.md. Before working on a
submodule, you MUST read its local AGENTS.md if it has one.

- rust-audiobook | github.com/milanglacier/rust-audiobook | yes

## Agent rules

- Read the submodule's local AGENTS.md first (if it has one, see list above);
  it overrides this file for work in that submodule.
- Submodules are independent repos: edit/test inside the submodule, commit there
  first (all submodules use `main`), then update the gitlink in this monorepo
  (`git add <submodule>` + commit). Don't mix submodules in one commit.
- Don't commit a submodule with a dirty working tree unless intentional.
- Run a project's own commands (e.g. `uv run --project
  .claude/skills/make-audiobook audiobook-build ...`) with the submodule as
  cwd; each keeps its own `.env`, skill venv and caches.
