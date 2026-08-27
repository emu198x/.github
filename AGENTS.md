# Emu198x — org container

This folder is the org container for the **`emu198x` GitHub organisation**. It is not the flagship repo itself; each child folder is an independent repo with its own remote. Commit inside the repo that owns the file.

Emu198x is the emulator sibling of the 198x family: a multi-platform retro
emulator suite and reusable Rust hardware-core workspace. See the umbrella
context at [`../CLAUDE.md`](../CLAUDE.md), the sibling coordination decision at
[`../decisions/sibling-project-coordination.md`](../decisions/sibling-project-coordination.md),
and the skeleton/layout decision at
[`../decisions/project-skeleton-standard.md`](../decisions/project-skeleton-standard.md).

## Repos in this org

| Folder | GitHub repo | Role |
|--------|-------------|------|
| [`emu198x/`](emu198x/) | `emu198x/emu198x` | **Flagship** Rust workspace: emulator cores, reusable chip/CPU crates, tools, knowledge base, and release configuration. |
| [`docs/`](docs/) | `emu198x/docs` | Emu198x documentation and current status summaries. |
| [`emu198x.github.io/`](emu198x.github.io/) | `emu198x/emu198x.github.io` | Public GitHub Pages site for Emu198x. |
| [`roms/`](roms/) | local workspace | Local ROM/media workspace; not a repo unless explicitly created. |

## Working here

- **Commit in the right subfolder.** The active emulator repo is
  [`emu198x/`](emu198x/); the docs/status repo is [`docs/`](docs/); the public
  site repo is [`emu198x.github.io/`](emu198x.github.io/). Run Git commands
  inside the repo you are changing.
- **Read the repo-level rules before code changes:**
  [`emu198x/RULES.md`](emu198x/RULES.md) and
  [`emu198x/CLAUDE.md`](emu198x/CLAUDE.md).
- **Cross-project decisions** live in the umbrella [`../decisions/`](../decisions/);
  Emu198x-only decisions live in [`emu198x/knowledge/decisions/`](emu198x/knowledge/decisions/).
- **Hardware facts cite the shared reference layers.** The repo-level
  [`emu198x/knowledge/`](emu198x/knowledge/) tree is codebase-tied distillation,
  not the primary source library.
- **ROM/media files are local inputs.** Keep them in `roms/` and do not commit
  them unless a dedicated repo and provenance policy are created.
