# Contributing to W.A.Y?

Thanks for considering a contribution. W.A.Y? ("Who Are You? — I'm not a developer")
is a personal AI collaboration harness built on one premise: the most personal
environment is the best-fitting one. Contributions that keep the harness durable,
honest, and approachable to non-developers are the most welcome.

This document is the English-default contributor guide. Localized notes may follow in
`docs/i18n/` over time.

---

## The one rule that overrides everything

**Never commit operational data or personal information (PII).**

W.A.Y? holds only **meta-information** — events, patterns, definitions, statistics.
Real operational data (revenue figures, approval contents, API responses, customer
data, real names, private identifiers) lives isolated in separate project repos. This
is the P6 one-way isolation principle: **data doesn't leak; lessons do.**

Before you open a pull request, check your diff for:

- real names, email addresses, phone numbers, account or document IDs
- company names, private project names, internal hostnames
- API keys, tokens, secrets, or credentials of any kind
- operational numbers (real revenue, real metrics, real transaction values)
- anything pulled from a private memory store, log, or external repo

A quick self-check before pushing:

```bash
git diff --staged    # read every changed line with your own eyes
```

If you need an example, **tokenize it** (use a placeholder like `<project>`,
`example.com`, `123-456`) rather than a real value. When in doubt, leave it out. A
contribution that leaks PII will be declined regardless of its other merits — and if you
spot a leak already in the repo, see [`SECURITY.md`](SECURITY.md) for how to report it
privately.

---

## What you can contribute

| Type | Where it lands | Notes |
|------|----------------|-------|
| **Language-pack translation** | `docs/i18n/` | Translate or improve a localized README / CONCEPT / ONBOARDING. Keep the source structure and section order; translate meaning, not word-for-word. |
| **Skill / rule proposal** | `skills/`, `rules/` | Propose a new skill module or operating rule, or refine an existing one. Explain the principle it serves (P1–P6) and why it never breaks across tasks/machines/models. |
| **Bug / issue** | GitHub Issues | A broken instruction, a rule that contradicts another, a doc that no longer matches behavior. A minimal repro or the exact file:line helps. |
| **Documentation improvement** | any `*.md` | Clarity, accuracy, fixing drift between docs and behavior. Honest "this doesn't actually work yet" notes are valued — the harness marks unbuilt features explicitly rather than hiding them. |

Not sure where your idea fits? Open an issue first and we'll point it at the right
place.

---

## Procedure: fork → branch → PR

1. **Fork** the repository to your own GitHub account.
2. **Branch** from `main` with a descriptive name:
   - `feat/...` for new skills, rules, or features
   - `fix/...` for bug fixes
   - `docs/...` for documentation or translation
   - `i18n/...` for language packs
3. **Make your change**, keeping it focused — one logical change per pull request is
   easier to review and reason about.
4. **Self-check for PII** (see the rule above) — read your full staged diff.
5. **Open a pull request** against `main`. In the description, say what changed and why,
   and note which principle (P1–P6) or trust mechanism it touches if relevant.
6. **Review** — a maintainer reviews for correctness, fit with the harness philosophy,
   and the no-PII guarantee. Expect questions; the goal is a structure that stays
   durable, not a fast merge.

For substantial changes (a new skill, a rule that alters core behavior), please open an
issue to discuss the approach **before** investing in the implementation. This mirrors
the harness's own P1 Plan-First / P2 Sync-Before-Execute stance — align on the outcome,
then build.

---

## Style and formatting

The harness follows a few hard formatting rules. Please match them in any file you add
or edit.

- **No diamond / section-sign symbols.** Do not use the section-sign (silcrow) mark or
  decorative diamond glyphs as section markers. Use plain section numbering instead — `1.`, `2.`, `3.` for
  document sections.
- **No circled / enclosed numerals or letters.** Characters like the circled-1 through
  circled-20 range, or circled letters, render inconsistently across fonts and
  terminals. Use `(1)`, `(2)`, `(3)` instead.
- **English is the default** for repository-level docs (`CONTRIBUTING`, `SECURITY`,
  `CODE_OF_CONDUCT`, top-level README/CONCEPT/ONBOARDING). Localized versions live in
  `docs/i18n/`.
- **Prefer tables and explicit trade-offs** when comparing options — it matches the
  harness's documentation voice.
- **Be honest about state.** If a feature is described but not yet built, mark it
  explicitly (for example `[not built]`) rather than implying it works. The harness
  treats hidden, unbuilt automation as a defect, not a convenience.

---

## Philosophy check (the short version)

A contribution fits W.A.Y? when it:

- keeps the harness **honest** (SVOP — sources over guesses, unknowns surfaced not
  smoothed over),
- keeps it **durable** (a small set of load-bearing rules that work identically across
  environments and models),
- keeps it **approachable** to non-developers (the "I'm not a developer" premise), and
- never lets **operational data leak** (P6 one-way isolation).

If your change does those things, it belongs here.

---

## License

By contributing, you agree that your contributions are licensed under the project's MIT
License — see [`LICENSE`](LICENSE).
