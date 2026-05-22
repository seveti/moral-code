# Contributing to moral-code

Thanks for considering a contribution. This repository is intentionally small, slow, and high-bar — the document it produces is meant to be loaded into AI agents acting on people's behalf, so the cost of churn is real.

## Verified contributors only

`main` accepts changes only from **verified contributors** — humans whose identity is tied to a public profile (GitHub, personal site, or a signed statement). The goal is auditable lineage: anyone reading this code should be able to trace every principle back to a real, named person.

### Becoming a verified contributor

Open a PR named `proposal-add-contributor-<your-handle>` adding yourself to `CODEOWNERS` with:

- Your GitHub handle (with verified email, signed commits set up).
- A one-paragraph bio: who you are, what work qualifies you to weigh in on agent ethics.
- A signed commit verifying control of the identity.

A current CODEOWNERS member reviews and approves. We'll grow the list deliberately.

## Branch + PR workflow

1. **Branch from `main`.** Name it `proposal-<short-slug>` for principle changes, or `chore-<slug>` for typos / formatting.
2. **Sign every commit.** GPG, SSH, or sigstore — all are accepted; commits without signatures will be rejected by branch protection.
3. **Open a PR.** Describe the change, the motivation, and any prior discussion.
4. **Update `CHANGELOG.md`** with a one-line entry under `[Unreleased]`.
5. For **substantive principle changes** (Tier 1 or Tier 2 additions, removals, or weakenings):
   - Tag the PR `principle-change`.
   - A 14-day open comment window starts when the PR is marked ready for review.
   - At least one CODEOWNERS approval is required.
   - The PR description must include a "Why now" rationale.

## What counts as substantive

- **Substantive (14-day window):** adding, removing, or weakening a principle in Tier 1 or Tier 2. Renumbering existing principles.
- **Non-substantive (faster merge):** typo fixes, formatting, example clarifications, README updates, link updates, CHANGELOG curation.

When in doubt, treat it as substantive.

## Tone and posture

- Principles should be **declarative and actionable**, not aspirational fluff.
- Keep the document something an agent can actually load and condition on. Avoid jargon, internal references, and language that requires external context to interpret.
- If a principle isn't already enforceable in real harnesses, mark it explicitly (e.g., *"aspirational — no harness currently enforces this"*). Don't pretend.

## Disclosure

If you find a security or safety issue with this document (e.g., a principle has a loophole that lets a bad agent slip through), **don't open a public issue**. Email a CODEOWNERS member directly.

## License

By contributing, you agree your contributions are licensed under Apache 2.0, same as the rest of the repo.
