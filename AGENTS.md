# workflows Agent Context

This file gives Codex and other agents enough repository context to work safely and to support later portfolio analysis.

<!-- BEGIN GENERATED PORTFOLIO CONTEXT -->

## Generated Repository Context

This section was generated from the GitHub repository inventory and local checkout to support future Codex work and portfolio analysis.

### Repository Metadata
- Remote: https://github.com/HavenDV/workflows
- Visibility: public
- Type: original; active
- Primary language: Not reported
- Topics: reusable-workflows, dotnet, msbuild, publish, nuget, conventional-commits, auto-release, release-notes, release-notes-generator, ci, cd, github-actions, continious-integration, continious-delivery
- Last pushed: 2026-05-21T10:40:03Z
- Local path: /Users/havendv/GitHub/HavenDV/workflows
- Local note: standard checkout
- Classification: Public developer tooling/library

### Working Summary
This workflow is for developing and releasing a NuGet package by a small number of people on the same branch. It is based on the Conventional Commits specification and will only release new releases if they contain fix/feat/perf commit types. It automatically generates a build number (BUILD_NUMBER environment variable). It also automatically generates Package Release Notes based on the latest commits (PACKAGE_RELEASE_NOTES environment variable).

### Detected Structure
- Top-level items: `.github/`, `.gitignore`, `README.md`
- Sampled file count: 2
- Common extensions: .md (1), [no extension] (1)

### Manifests And Commands
- .github/workflows

Suggested commands:
- Inspect project manifests before choosing build commands.

Testing signal:
- No automated test entry point was detected by the generator.

### Portfolio Signals
- Skills: GitHub Actions, reusable-workflows, dotnet, msbuild, publish, nuget, conventional-commits, auto-release, release-notes, release-notes-generator, ci, cd, github-actions, continious-integration, continious-delivery, NuGet packaging
- Portfolio angle: Useful evidence for automation, CI/CD, and repeatable release workflows.

### Agent Notes
- Prefer README and manifest instructions over generated assumptions when they disagree.
- Keep generated context current when build tooling, test commands, or project scope changes.
- Review private or client-specific details before copying portfolio claims into public material.

<!-- END GENERATED PORTFOLIO CONTEXT -->
