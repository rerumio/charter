# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

The charter of Rerumio — the platform's law, in prose. There is no code here, and no build, test,
lint or run command. The whole toolchain is git and a text editor. The product-level context lives
one level up in `../CLAUDE.md`.

## The two codes

Every text belongs to exactly one code, and a text never blends them:

- **`principles/`** — what the platform is and promises. No figures, no states, no screens.
- **`mechanics/`** — how a thing works: what it is counted from, what states it moves between, who
  may act on it. Figures and tables live here.

`principles/CONSTITUTION.md` sits above everything. Its eleven guarantees are amendable only by
addition — see `principles/.claude/rules/leave-the-guarantees-alone.md`. When a mechanic collides
with a guarantee, the mechanic is wrong.

Each code divides the same way: `users/`, `publications/`, `platform/`.

## The one machine

The mechanics are not independent documents. Reputation, ranks and medals each feed vote weight;
vote weight feeds admission to the catalog and the order of Trends; admission decides what is
listed at all. Domains scope reputation, access and admission. A post locks after its editing
window, and only a locked post is admitted.

Change what feeds vote weight and you have changed what enters the catalog. Read the neighbouring
files before editing one — `mechanics/users/reputation.md`, `ranks.md`, `medals.md`,
`mechanics/publications/votes.md`, `mechanics/platform/admission-to-catalog.md`,
`trends-algorithm.md`.

Access (`admit`, `moderate`, `medals`, and the rest) is granted by a person and never earned; it
stands apart from rank and reputation, which are earned and grant no access.

## How the texts are written

Read the rules in `.claude/rules/` before writing. In short:

- Files under `mechanics/` follow `mechanics/.claude/TEMPLATE.md` exactly — same headings, same
  order. **Definition** is written to survive three rebuilds; **Implementation** holds every figure,
  table and formula and is expected to change. A figure never appears above Implementation.
- Law states, it never argues. No justification, no examples, no second person, no hedging.
- One word per term, always the same one. A synonym that reads better breaks the ability to quote
  the law against itself.
- Point across, never restate. A text names the other text that governs the other half — by its
  subject ("stands in voting", "stands in ranks"), not by file path. Two copies of a rule are one
  rule and one lie waiting.
- Every grant states its inverse: granted and revoked, admitted and refused.

## Checking work

There is nothing to run. A change is verified by reading: the file still matches the template, the
terms match the ones already in use elsewhere, no figure sits outside Implementation, and every
neighbouring mechanic the change touches still reads true.
