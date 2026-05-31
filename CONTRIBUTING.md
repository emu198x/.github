# Contributing to Emu198x

Thanks for taking a look. Emu198x builds cycle-accurate retro emulators in Rust;
help is welcome, especially from people who know a machine's hardware quirks
first-hand.

This file applies to every repo in the [emu198x](https://github.com/emu198x)
org. The main one is [`emu198x`](https://github.com/emu198x/emu198x).

## Read the rules first

The emulator has **binding architectural constraints** — the clock model, the
pin-level CPU/bus interface (no `Bus` trait, no callbacks), half-cycle signals,
and more. Read [`RULES.md`](https://github.com/emu198x/emu198x/blob/main/RULES.md)
before writing code. Suggestions that contradict it will be sent back to it.

## Build and check

```sh
cargo build
cargo test
cargo fmt --all --check
cargo clippy --workspace --all-targets -- -D warnings
```

All must pass. The workspace forbids `unsafe` and denies `dbg!`/`.unwrap()` in
committed code; keep library code panic-free and return errors instead.

## The accuracy bar

Accuracy is the whole point, so correctness regressions are the bugs that matter
most:

- Validate against the standard suites — Tom Harte SingleStepTests (6502 / Z80 /
  68000), ZEXDOC/ZEXALL, Klaus Dormann's 6502 functional tests, Wolfgang
  Lorenz, mooneye, and the others wired into CI. **Don't regress them.**
- A correctness fix should come with the test vector that pins the behaviour.
- Hardware facts come with provenance — cite a datasheet or the family's
  reference library, and record durable findings in the repo's `knowledge/`.

## Commits and PRs

- Use **conventional-commit** prefixes (`feat:`, `fix:`, `chore:`…). release-plz
  reads them to bump the version and write the CHANGELOG.
- Clear subjects describing the effect; explain the *why* in the body.
- One concern per PR; fill in the PR checklist.

## Reporting issues

Use the issue templates — a **bug report** (please name the system and include
the ROM/disk/tape or test vector, plus expected vs actual behaviour) or a
**feature request**.
