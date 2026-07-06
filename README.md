<div align="center">

**disclose.io · a sourced history of the terms**

# The Archeology of Safe Harbor

### Tracing the **disclose.io safe-harbor terms** to their earliest internet-verifiable ancestor, with every claim anchored to a live artifact. Read it at **[history.disclose.io](https://history.disclose.io)**.

<p>
<a href="LICENSE"><img src="https://img.shields.io/github/license/disclose/history.disclose.io?color=5B3AB6&label=license" alt="license"></a>
<a href="https://history.disclose.io"><img src="https://img.shields.io/badge/live-history.disclose.io-5B3AB6" alt="live · history.disclose.io"></a>
<a href=".github/workflows/link-check.yml"><img src="https://github.com/disclose/history.disclose.io/actions/workflows/link-check.yml/badge.svg" alt="link check"></a>
<img src="https://img.shields.io/badge/evidence-SHA--256%20%2B%20Wayback-5B3AB6" alt="evidence · SHA-256 + Wayback">
</p>

Part of **[the disclose.io Project](https://disclose.io)** — the infrastructure that powers vulnerability disclosure and security reporting, Internet-wide. [Browse the ecosystem →](https://github.com/disclose)

</div>

---

> [!NOTE]
> **disclose.io exists to be the infrastructure that powers vulnerability disclosure and security reporting, Internet-wide — safe, simple, and standardized for researchers and organizations everywhere.** Its canonical, lawyer-reviewed safe-harbor language — the **[dioterms](https://github.com/disclose/dioterms)** — was dedicated to the public domain under CC0 in 2020. **This repository is the sourced provenance of that language:** twelve years of it, verified commit-by-commit — **2014** lineage root → **2018** disclose.io founded → **2020** dioterms CC0 → **2026** scoreboard era. The standardized safe-harbor movement runs on rails this history documents.

## About

A sourced history of the disclose.io vulnerability-disclosure ("dioterms") safe-harbor terms — traced to their earliest internet-verifiable ancestor, with every claim anchored to a live artifact: a git commit, a Wayback snapshot, a published standard, or a court/legislative record. It is a **falsifiable** history — the earliest-root claim stands only until an earlier artifact surfaces.

### Quick links

| Purpose | Link |
| - | - |
| Read the live report | **[history.disclose.io](https://history.disclose.io)** |
| The chronological, sourced timeline (2000 → 2026) | [TIMELINE.md](TIMELINE.md) |
| Every dated claim — how its date was established, with a verified URL | [sources/LEDGER.md](sources/LEDGER.md) |
| The three-organization genealogy of the safe-harbor clause | [research/predecessor-language-lineage.md](research/predecessor-language-lineage.md) |
| The terms this history traces (dioterms · CC0) | [github.com/disclose/dioterms](https://github.com/disclose/dioterms) |
| Browse the disclose.io ecosystem | [github.com/disclose](https://github.com/disclose) |

## What's in this repository

- `report-site/` — the self-contained HTML report deployed to [history.disclose.io](https://history.disclose.io)
- `TIMELINE.md` — the chronological, sourced timeline (2000 → 2026)
- `sources/LEDGER.md` — every dated claim, how its date was established, and a verified URL
- `sources/*.md` — key primary-source captures, verbatim
- `research/predecessor-language-lineage.md` — the three-organization genealogy of the safe-harbor clause
- `evidence/` — **bit-rot protection**: local byte captures + SHA-256 hashes + Wayback snapshots of every source (see [`evidence/README.md`](evidence/README.md))

## Method

Ground-truth hierarchy: git commit author-dates and Wayback snapshot timestamps outrank publish dates and recollection. Every URL is verified live before it enters the timeline. The earliest root (2014-07-23, the first commit of `bugcrowd/disclosure-policy`) is a falsifiable conjecture — it stands until an earlier Bugcrowd artifact surfaces.

Because the whole point of this repository is that its links resolve, a [link-checker](.github/workflows/link-check.yml) runs in CI over the project's docs — the history dogfoods its own standard. (The historical source corpus is checked differently: it is expected to rot, so it is preserved in [`evidence/`](evidence/README.md) with byte captures, SHA-256 hashes, and Wayback snapshots rather than gated on live liveness.)

## Contributing

Corrections and additions are welcome — a history is only as good as its willingness to be corrected. The rule is simple: **every dated claim must be anchored to a verifiable source** (a git author-date, a Wayback snapshot, a published standard, or a court/legislative record), and that source outranks any publish date or recollection.

[**Open a correction or addition →**](https://github.com/disclose/history.disclose.io/issues/new/choose) &nbsp;·&nbsp; or read the [contribution guidelines](CONTRIBUTING.md).

## Security

This repository documents responsible disclosure — and practices it. See [SECURITY.md](SECURITY.md).

## License

<a rel="license" href="https://creativecommons.org/publicdomain/zero/1.0/"><img alt="CC0 1.0" style="border-width:0" src="https://licensebuttons.net/p/zero/1.0/88x31.png"></a>

Dedicated to the public domain under [**CC0 1.0 Universal**](LICENSE) — the same dedication as the [dioterms](https://github.com/disclose/dioterms) this history traces. To the extent possible under law, the disclose.io Project has waived all copyright and related rights to this work. Cited third-party material — quotations, snapshots, and referenced documents — remains under its own rights and is used here for reference and commentary.
