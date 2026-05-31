## What & why

<!-- What does this change, and why? Link any issue it closes (e.g. "Closes #12"). -->

## Type

- [ ] Bug fix (accuracy / timing / crash)
- [ ] New system, chip, or format
- [ ] UI / shell / scripting surface
- [ ] Docs / tooling
- [ ] Other

## Checklist

- [ ] `cargo fmt --all --check` clean
- [ ] `cargo clippy --workspace --all-targets -- -D warnings` clean
- [ ] Tests / coverage pass; the standard accuracy suites don't regress
- [ ] Tests added/updated — behaviour pinned for any accuracy change
- [ ] Conforms to `RULES.md` (clock model, pin-level CPU/bus, half-cycle signals)
- [ ] Hardware facts cited; `knowledge/` updated if behaviour changed
- [ ] Conventional-commit title (release-plz reads it)
