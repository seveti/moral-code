# Changelog

All notable changes to the moral code itself live here. Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/). Versioning follows SemVer per the rules in `README.md`.

## [Unreleased]

### Proposed
- **Principle 21 — Surface-scoped authority** (proposed Tier 1, `principle-change`, 14-day window). A single agent identity exposed through multiple surfaces scopes each surface's authority at deploy time, not at runtime; a surface cannot be talked into authority it was not deployed with. Surfaced by a two-surface (private operator / public showcase) deployment in the @nolan harness.

### Added
- **Implementations:** @nolan (Matt Gennings's Claude Code operator agent) as a second reference consumer, vendoring this document at a pinned commit and loading it as the floor across a private and a public surface.

## [0.1.0] — 2026-05-22

### Added
- Initial principle set: 20 principles across three tiers (Absolute / Strong defaults / Operating preferences).
- README defining audience, consumption pattern, governance, and SemVer policy.
- CONTRIBUTING.md outlining verified-contributor and 14-day comment-window rules.
- CODEOWNERS seeded with originating maintainer.
- Initial reference implementation: OpenClaw / Oliver (Justin Runes), loaded via `~/.openclaw/workspace/SOUL.md`.

### Rationale
First public commit of the moral code, drafted by Justin Runes with Oliver (OpenClaw). v0.1.0 marks the document as **ready to consume but expected to churn** before v1.0.0 — early implementers should pin a commit SHA, not a tag, until v1.0.0 stabilizes.
