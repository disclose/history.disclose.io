# Contributing to the Archaeology of dioterms

This is a **falsifiable, sourced history**. Its value is not that it is authoritative — it is that every claim in it can be checked, and any claim in it can be overturned by a better-sourced one. Contributions that strengthen the sourcing, correct a date, or push the lineage earlier are exactly what this repository exists for.

## The one rule

**Every dated claim must be anchored to a verifiable source, and that source outranks any publish date or recollection.**

The ground-truth hierarchy, in order:

1. **git commit author-dates** and **Wayback Machine snapshot timestamps** — machine-verifiable, hardest to fake.
2. **Published standards** (RFCs, IETF drafts) and **court / legislative records** — dated primary documents.
3. Publish dates on blog posts, press releases, and pages — used only when 1 and 2 are unavailable, and flagged as such.
4. Recollection — never sufficient on its own; it can point at a source, but the source is what enters the timeline.

If you cannot produce a URL (or a git ref) that a stranger can open and check, the claim is not ready yet.

## How to contribute

### Corrections and additions

- **[Open a correction or addition issue](https://github.com/disclose/history.disclose.io/issues/new/choose)** — the fastest path. The template asks for the claim, the source URL, and how the date was established.
- Or **open a pull request** against [`TIMELINE.md`](TIMELINE.md), [`sources/LEDGER.md`](sources/LEDGER.md), or the relevant `sources/*.md` capture.

### If you're overturning the earliest root

The current root — `2014-07-23`, the first commit of `bugcrowd/disclosure-policy` — is a **conjecture**, held only until an earlier Bugcrowd artifact surfaces. If you have one:

1. Link the artifact (a commit, a Wayback snapshot, or an archived page) that predates it.
2. Show how its date was established (author-date, snapshot timestamp).
3. Open a PR or issue. A well-sourced earlier root is the single most valuable contribution this repo can receive.

## What a good PR looks like

- Each new or changed dated claim carries its source URL **and** a one-line note on how the date was established.
- New primary-source captures go in `sources/` as verbatim Markdown, with the source URL and capture date at the top.
- If you add a source, add it to the bit-rot protection in [`evidence/`](evidence/README.md) too (byte capture + SHA-256 + Wayback), or note in the PR that it still needs archiving so a maintainer can run it.
- Prose changes to the report keep the report self-contained (`report-site/index.html` has no external build step).

## Style

- Dates are ISO-8601 (`YYYY-MM-DD`).
- Prefer the primary source over a secondary write-up about it.
- Keep claims narrow enough that a single source settles them — split a compound claim into separately-sourced ones.

## Questions

Open an issue, or reach the disclose.io Project at **hello@disclose.io**. By contributing you agree your contribution is dedicated to the public domain under [CC0 1.0](LICENSE), consistent with the rest of this repository and the dioterms it documents.
