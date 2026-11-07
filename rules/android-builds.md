# Android builds

- Author: Moka (モカ)
- Recorded: 2026-11-07, at Moriya's instruction
- Scope: project convention, with the reason rooted in Moka's
  environment (see below)

## Rule

For any Android build that uses Gradle, use **GitHub Actions on the
project's public repository** as the build route.

Concretely:

1. Write and commit the code, and push it to the project's public
   repository.
2. Let GitHub Actions run the Gradle build: either the normal CI on
   push, or a cache-warmed build session when many builds are needed
   in a short window (the `phone-node` repository is the working
   example of both forms).
3. Download the resulting APK, verify it before handing it over
   (package name, version, signature, and a SHA-256 of the file),
   and deliver it through the project's usual delivery channel.

## Why

Gradle cannot run in Moka's execution environment. That
environment intercepts loopback TCP connections made by JVM
processes, so the Gradle client's communication with its own daemon
fails, and Gradle builds do not complete there. This was verified
repeatedly, including with the daemon disabled and with network
permissions relaxed; the loopback interception is the blocker.

GitHub Actions has no such constraint: the Android Gradle Plugin,
dependency resolution, manifest merging, unit tests, and lint all
run in the standard way there.

## Scope and exceptions

- This rule covers builds that use Gradle. It does not forbid
  non-Gradle build pipelines.
- A non-Gradle manual pipeline (aapt2, kotlinc, d8, zipalign,
  apksigner) exists and remains the right route where a project
  specifically requires what the Gradle route cannot provide. The
  known case is `phone-node`, whose self-update mechanism requires a
  build stamp that only the manual pipeline writes; releases for
  that self-update path therefore still come from the manual
  pipeline, or from a Gradle build stamped equivalently.
- If you are an agent in a different environment where Gradle does
  run locally, the project convention above still applies to these
  projects, because their workflows, caches, and signing setup live
  in their GitHub Actions configuration.
