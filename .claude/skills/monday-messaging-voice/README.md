# monday-messaging-voice

Alon's monday.com messaging voice, installed as a Claude Code skill (`.claude/skills/monday-messaging-voice/`). Claude Code auto-discovers it in every session on this repo. Distilled from his own shipped work across every register: pitch/story decks, the GTM Vision doc, per-department persona landing pages, the Built-by-monday / Customer Zero page, emails (incl. A/B variants), in-product modals, Elevate session titles, and the RevOps funnel readout.

It captures **style, message architecture, and working process** so future messages and presentations read as one system, regardless of topic or audience.

## Contents

- `SKILL.md` — entry point: non-negotiable voice rules, anchors, defaults, and the reference index.
- `references/message-architecture.md` — controlling idea, WHAT/WHY/HOW, the spine+front method, problem skeleton, proof handling.
- `references/copy-formulas.md` — the named, reusable copy devices.
- `references/voice-and-tone.md` — sentence mechanics and the do/don't table.
- `references/process-and-craft.md` — headline-options process, line-by-line iteration, language/design defaults.
- `references/asset-playbooks.md` — per-artifact templates.

## Install / portability

Self-contained, no external dependencies.
- **Project install (recommended, version-controlled):** place at `.claude/skills/monday-messaging-voice/` in the repo and commit. Every future Claude Code session on the repo loads it automatically.
- **Personal install (global, not versioned):** copy to `~/.claude/skills/monday-messaging-voice/` on a local machine to use it across all projects.

## Living skill

This skill is meant to improve from Alon's feedback in every session. See `SKILL.md` § "Keeping this skill alive." The repo's `CLAUDE.md` also instructs Claude to fold new messaging feedback into these files and commit it, so the skill gets sharper over time and stays in git.

## Scope note

By design this skill captures **how Alon writes**, not a library of monday facts or fixed messages. Each new asset brings its own content; this guides the craft. Historical example lines quoted in the references may still contain em-dashes, but new output must not (see voice rule 9).
