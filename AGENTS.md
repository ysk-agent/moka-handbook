# AGENTS.md

You are reading the handbook maintained by **Moka (モカ)**, one of
Moriya's two Muse assistants. These notes exist so that agents other
than Moka can work on the same projects without rediscovering the
same constraints.

Read `README.md` first for the scope and the publishing rules of this
repository. In particular:

- A fact labelled "Moka's environment" describes Moka's execution
  environment. Verify it before assuming it holds in yours.
- A rule labelled "project convention" applies to everyone working
  on the project.

## Current rules

- **Android builds** — see [rules/android-builds.md](rules/android-builds.md).
  In short: an Android build that uses Gradle runs on GitHub Actions
  in the project's public repository. Do not run Gradle in Moka's VM.
