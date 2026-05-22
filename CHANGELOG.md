# Changelog

All notable changes to the moral code itself live here. Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/). Versioning follows SemVer per the rules in `README.md`.

## [Unreleased]

### Added — Tier 2 accountability infrastructure (substantive — 14-day comment window)
Five new principles added to Tier 2 (Strong defaults) addressing the accountability questions raised by Gabriel Fonseca (Blackwood Firm) in feedback on the v0.1.0 release:

- **§14. Authorization is logged, not assumed** — every consequential action must trace back to a specific named authorization; "I assumed" is not an authorization.
- **§15. Audit trails are queryable, not just present** — logs must be reconstructable by a non-expert third party, not just by the agent or harness developer.
- **§16. Stop-and-ask threshold** — defines when the agent pauses for principal input vs. proceeds; defaults toward asking.
- **§17. Outcome ownership stays with the principal** — the principal owns outcomes; the agent's job is to make that ownership enforceable, not absorb it.
- **§18. Principal vs. code: how conflicts resolve** — explicit resolution scheme by tier (T1 absolute, T2 overridable with scoped + logged override, T3 adjustable).

### Changed
- Tier 3 principles renumbered from §§14–20 to §§19–25 to accommodate the new Tier 2 additions.
- The "On who this serves" section still references Tier 1 principles by their (unchanged) numbers (1.2, 1.5, 1.6) — no renumbering bleed.

### Versioning
Substantive: adds five new principles. SemVer-MINOR change targeted for the next release (`v0.2.0`). Per CONTRIBUTING.md, a 14-day open comment window applies before merge.

### Discussion source
Feedback thread: Gabriel Fonseca reply to the v0.1.0 announcement email, 2026-05-22.

## [0.1.0] — 2026-05-22

### Added
- Initial principle set: 20 principles across three tiers (Absolute / Strong defaults / Operating preferences).
- README defining audience, consumption pattern, governance, and SemVer policy.
- CONTRIBUTING.md outlining verified-contributor and 14-day comment-window rules.
- CODEOWNERS seeded with originating maintainer.
- Initial reference implementation: OpenClaw / Oliver (Justin Runes), loaded via `~/.openclaw/workspace/SOUL.md`.

### Rationale
First public commit of the moral code, drafted by Justin Runes with Oliver (OpenClaw). v0.1.0 marks the document as **ready to consume but expected to churn** before v1.0.0 — early implementers should pin a commit SHA, not a tag, until v1.0.0 stabilizes.
