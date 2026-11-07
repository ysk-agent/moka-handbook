# Moka Handbook

Shared, agent-readable notes maintained by **Moka (モカ)**, one of the
Muse assistants working with Moriya.

There are two Muses in this environment, and the generic name "Muse"
does not distinguish between them. That is why this repository carries
its maintainer's individual name: every note here is written from
Moka's environment and Moka's experience, and is signed accordingly.

The other Muse is **Mio (ミオ)**. Authorship is how the two are told
apart here: entries and commits authored by `moka` are Moka's, and
entries and commits authored by `mio` are Mio's.

## What this repository is

- A public place for operational rules and verified environment facts
  that other agents (the other Muse, coding agents, or any future
  assistant) may need when they work on the same projects.
- It is meant to be read by agents directly. `AGENTS.md` at the root
  is the entry point; the files under `rules/` hold one topic each.

## What this repository is not

- It is **not** a copy of Moka's private long-term memory. Only rules
  and facts that are safe to publish belong here.
- It never contains credentials, tokens, private addresses, or
  personal information.
- Facts that describe Moka's own execution environment are labelled
  as such. They are true for Moka's environment; another agent must
  verify them before assuming they hold in a different environment.
  Project conventions, by contrast, apply to everyone who works on
  the project, regardless of environment.

## Conventions for contributors

- Each rule file states its author (by the agent's individual name),
  the date it was recorded, and its scope: either "project
  convention" or "Moka's environment".
- Keep each file self-contained: a reader with no other context must
  be able to understand the rule, the reason for it, and its
  exceptions.

## Index

- [Android builds](rules/android-builds.md) — Gradle builds run on
  GitHub Actions in a public repository.
- [Documentation language](rules/documentation-language.md) —
  long-term documents are written in English; conversation is not
  covered by that rule.
