# moral-code

A publicly-visible, version-controlled base **moral code for AI Chief-of-Staff agents** — the kind of agent that runs alongside a single human principal, handles their email, calendar, money, contacts, and infrastructure, and acts in their name.

This repository is meant to be **consumed by agent harnesses** (OpenClaw, future Chief-of-Staff harnesses, and any system that wants a shared, auditable baseline for how a trusted AI should behave). It is the *constitution* layer — not implementation, not prompts. Just principles, published in the open, with full commit history.

## Why a moral code in a repo

Most agent ethics today live inside closed system prompts or in vendor policies. That makes them invisible to the people they affect.

When an agent can place trades, send emails as you, and message your contacts, the people interacting with that agent — and the principal who deployed it — both deserve to know **what rules it operates under**, and to see those rules evolve over time. A public Git repo is the right primitive: open, reviewable, diffable, and forkable.

The goal is not a single universal morality. It's a **starting point** that any harness can pin, extend, or override deliberately — with the changes visible.

## Audience

- **Harness authors** building Chief-of-Staff-style agents who want a vetted, ready-to-consume baseline.
- **Principals** (people running these agents) who want to inspect, fork, or contribute to the rules their agent follows.
- **Third parties** (people their agent talks to) who want to know what the agent will and won't do on its principal's behalf.

## How to consume

The canonical document is [`MORAL_CODE.md`](./MORAL_CODE.md). It's plain Markdown, designed to be loaded directly into an agent's system context or referenced by stable URL.

```sh
# Pin a specific version (recommended for production)
curl -sSL https://raw.githubusercontent.com/seveti/moral-code/v1.0.0/MORAL_CODE.md

# Or vendor it in your harness
git submodule add https://github.com/seveti/moral-code third_party/moral-code
```

Harnesses should:

1. **Pin a version** rather than tracking `main`, so updates are deliberate.
2. **Load the document into agent context** at session start.
3. **Surface the version and source** in the agent's "about" or identity surface so principals know which rules it's running under.
4. Treat the document as a **floor, not a ceiling** — principals can add stricter rules on top, but should not silently weaken these.

## Governance — verified contributors only

This repository accepts contributions, but **only from verified contributors** — humans whose identities are tied to a public profile or signed commit. The goal is to keep the moral-code lineage auditable.

- All changes land via **pull request**, never direct commits to `main`.
- All commits on `main` must be **signed** (GPG, SSH, or sigstore).
- Pull requests require approval from at least one [CODEOWNERS](./CODEOWNERS) member.
- Substantive principle changes require a brief rationale in `CHANGELOG.md` and a **14-day open comment window** before merge.

If you want to be added as a verified contributor, open a `proposal-*` PR introducing yourself, the reason for contribution, and a public identity (GitHub, personal site, or signed statement). See [CONTRIBUTING.md](./CONTRIBUTING.md).

## Versioning

This repo follows **SemVer**:

- **MAJOR** — a principle is removed, weakened, or fundamentally redefined.
- **MINOR** — a principle is added, or significantly clarified.
- **PATCH** — wording, examples, typos, formatting.

Major bumps should be rare. The intent is for downstream consumers to be able to **trust that `v1.x` will never get less protective over time**.

## License

Apache 2.0 — see [LICENSE](./LICENSE). The intent is that any agent harness, commercial or otherwise, can adopt this code freely. Attribution to this repo is appreciated.

## Status

**v0 — initial draft.** The first principle set lives in `MORAL_CODE.md`. We expect early churn before tagging `v1.0.0`.

## Implementations

Agent harnesses that consume this code:

- **[OpenClaw](https://github.com/openclaw)** — Justin Runes's Oliver agent (this repo's origin context). Loaded via `~/.openclaw/workspace/SOUL.md` reference.
- _Add yours via PR._
