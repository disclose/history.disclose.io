# The Archaeology of dioterms — A Sourced Historical Timeline

> **history.disclose.io** · assembled 2026-05-31 · every date traces to a verified artifact in
> [`sources/LEDGER.md`](sources/LEDGER.md). Ground-truth hierarchy: git commit author-dates +
> Wayback snapshot timestamps **>** publish dates **>** recollection.


---

## 🏆 Earliest provenance root of the dioterms lineage: **2014-07-23**

> ⚠️ **Precise framing (matters):** a "dioterm" is a *disclose.io* term, and disclose.io did not
> exist until 2018. So the 2014 artifact below is **not itself a dioterm** — it is the earliest
> internet-traceable **ancestor** that the dioterms are directly, repo-documentedly descended
> from. The claim is about *provenance*, not about the brand existing in 2014.

The earliest traceable root of the dioterms is the **first commit of
[`bugcrowd/disclosure-policy`](https://github.com/bugcrowd/disclosure-policy/commit/10ea3e10c26f237cd8eca3453d816bedf251d640)** — hash `10ea3e1`, message *"first commit"*, authored by
**Chris Raethke** (Bugcrowd's founding CTO) on **2014-07-23 23:02:41 -0700**. That repo's own
GitHub description draws the inheritance explicitly:

> *"Open Source Vulnerability Disclosure Framework. Maintained by Bugcrowd and Cipherlaw.
> **Merged with https://github.com/disclose/dioterms.**"*

And the **defining feature of dioterms — bilateral safe harbor — is already present in that very
first 2014 file** (`responsible_disclosure_policy.md`):

> *"If you follow these guidelines… we commit to: **Not pursue or support any legal action
> related to your research**…"*

**So the dioterms language is ~4 years older than the disclose.io brand it later fed into.** Note
this proves a *Bugcrowd disclosure-policy repo* existed in 2014 — it does **not** prove
disclose.io was co-founded in 2014 (a separate, bio-sourced claim). Keep those two facts apart.

**Why this date is [HIGH] — the corroborating evidence:**
- **Author date == committer date** (`2014-07-23 23:02:41 -0700`) — no rebase/backdate divergence.
- **Root commit** — `rev-list --parents` shows no parent → a genuine initial commit, not an
  imported/migrated history.
- **Clean initial commit** — 3 files / 105 insertions (one policy + one guide + README), not a
  bulk import that would make the date suspect.
- **Independent corroboration** — the Wayback Machine captured the live repo on **2014-10-16**
  (HTTP 200) and 2015-03-17, ~3 months after the commit. Git **and** Wayback agree.

This is a falsifiable claim: it stands until an earlier Bugcrowd template, gist, or
snapshot surfaces. The refutation hunt found nothing earlier in Bugcrowd's repos.

---

## 🧬 The lineage chain

Solid arrows (`──▶`) = **documented inheritance** (repo says it merged X; X is a direct
ancestor). Dashed (`╌╌▶`) = **conceptual antecedent only** — same problem space, no sourced
derivation.

```
  CONCEPTUAL ANTECEDENTS          DOCUMENTED-INHERITANCE CHAIN                  CONFLUENCE            CANONICAL HOME
  (no sourced derivation)
 ┌──────────────────┐
 │ 2000  RFPolicy v1│╌╌┐
 │  (Rain Forest    │  ╎
 │   Puppy)         │  ╎   ┌─────────────────────────────────┐
 └──────────────────┘  ╎ ╌▶│ 2014-07-23  Bugcrowd + CipherLaw │──┐  (repo: "Merged with disclose/dioterms")
 ┌──────────────────┐  ╎   │  "Open Source Vuln Disclosure   │  │
 │ 2002 IETF resp.  │╌╌┤   │   Framework" (disclosure-policy)│  │   ┌──────────────────┐   ┌─────────────────┐
 │  disclosure draft│  ╎   │  → bilateral safe-harbor clause │  ├──▶│ 2018-08-02       │──▶│ 2020-06-30      │
 ├──────────────────┤  ╎   └─────────────────────────────────┘  │   │ disclose.io      │   │ disclose/       │
 │ 2014-02 ISO 29147│╌╌┘                                         │   │ LAUNCHES         │   │ dioterms repo   │
 └──────────────────┘      ┌─────────────────────────────────┐  │   │ (Bugcrowd +      │   │ → generic-core- │
                           │ 2017-18  Amit Elazari            │  │   │  Elazari) merges │   │   terms.md      │
                           │  #LegalBugBounty / "Hacking the  │──┘   │  3 predecessors  │   │ (2020-07-15)    │
                           │  Law" safe-harbor scholarship    │      └──────────────────┘   └─────────────────┘
                           │  + Dropbox researcher protection │
                           └─────────────────────────────────┘
```

The solid chain is sourced: disclose.io's **own 2018 launch page** names the three tributaries it
merged (Bugcrowd+CipherLaw's 2014 framework, Elazari's #legalbugbounty, Dropbox's
researcher-protection language), and `bugcrowd/disclosure-policy`'s description states it merged
into `disclose/dioterms`. The 2000–2014 norms (RFPolicy, IETF draft, ISO 29147) are dashed:
they shaped the *problem space* of standardized disclosure, but no document shows Bugcrowd's
framework deriving its text from them — they are antecedents, not parents.

---

## 🗓️ Timeline

Each entry: **date** — milestone *(project goal/intent active then)* — `[confidence]` — source.

### Platform pre-history — the crowdsourced-security market (the *demand* soil)
- **2012** — **Bugcrowd & HackerOne both founded; Bugcrowd launched first.** Primary source: HackerOne
  co-founder/CTO **Alex Rice** on the record — *"Both founded 2012, @Bugcrowd launched first!
  @Hacker0x01 kickoff 2/2012, 1st commit 4/2012, 1st private 1/2013, 1st public 10/2013."* *Why it
  matters: crowdsourced security **as a service** put researchers and orgs into at-scale, ongoing
  engagement — which is exactly what made **standardized** safe-harbor terms necessary by 2014.*
  `[HIGH — founder on record]` — https://x.com/senorarroz/status/779402727885410304
- **2013-03-05** — **Bugcrowd's "The List"**: earliest Wayback capture of a community-maintained
  public directory of bug-bounty programs ("Last update: 2nd March 2013") — a functional antecedent of
  diodb (2018) on the *directory* axis (conceptual only). `[MED]` —
  http://web.archive.org/web/20130305011641/http://bugcrowd.com/list-of-bug-bounty-programs

### Pre-history — disclosure norms (the *supply* soil)
- **2000-08-19** — **RFPolicy v1.1** (Rain Forest Puppy) live on wiretrip.net — first formalized
  vulnerability-disclosure *policy template*. **v2.0** ("5 working days") went live between
  2000-08-19 and its first capture on **2000-10-17** (bracketed by Wayback snapshots). *Goal: give
  researchers a repeatable, fair disclosure process.* `[HIGH — upgraded from MED 2026-07-01 on
  primary Wayback fetches]` —
  http://web.archive.org/web/20000819053824/http://www.wiretrip.net/rfp/policy.html
- **2002-02-15** — IETF draft *"Responsible Vulnerability Disclosure Process"* (Christey/MITRE +
  Wysopal/@stake), rev 00 submitted. *Goal: standardize "responsible disclosure" terminology.*
  `[HIGH — upgraded from MED 2026-07-01, datatracker primary]` —
  https://datatracker.ietf.org/doc/draft-christey-wysopal-vuln-disclosure/
- **2010-07-22** — **Microsoft (MSRC) reframes "Responsible Disclosure" → "Coordinated Vulnerability
  Disclosure"** — the neutrality pivot between "responsible" (2002) and the ISO-era vocabulary. `[HIGH]`
  — https://web.archive.org/web/20100724135757/http://blogs.technet.com/b/msrc/archive/2010/07/22/announcing-coordinated-vulnerability-disclosure.aspx
- **2013-11** — ISO/IEC 30111 first edition (*vulnerability handling processes*) — the vendor-internal
  handling standard, ~3 months before ISO/IEC 29147. `[HIGH]` —
  https://web.archive.org/web/20171220083905/https://www.iso.org/standard/53231.html
- **2014-02** — ISO/IEC 29147 first edition (vulnerability disclosure). *Goal: formal
  international standard.* `[MED]` — https://www.iso.org/standard/45170.html

### 2014 — the earliest provenance root (Bugcrowd precursor, not yet a "dioterm")
- **2014-03-31** — **Bugcrowd "Standard Disclosure Terms"**: platform-wide terms with
  researcher-protection *intent* but **no legal safe-harbor clause** — an earlier Bugcrowd terms
  artifact that is *not* the provenance root. `[HIGH capture / MED release-day]` —
  http://web.archive.org/web/20140411213116/http://blog.bugcrowd.com:80/standard-disclosure-terms/
- **2014-07-15** — Google announces **Project Zero** (8 days before the root commit); its **90-day**
  deadline (+14-day grace) is formalized 2015-02-13. Conceptual antecedent on the disclosure-clock
  axis. `[HIGH]` — https://projectzero.google/2014/07/announcing-project-zero.html
- **2014-07-23** — 🏆 **`bugcrowd/disclosure-policy` first commit** (`10ea3e1`, Chris Raethke).
  Files: `responsible_disclosure_policy.md`, `setting_up_a_responsible_disclosure_program.md`.
  *Goal: an open-source, copy-pasteable disclosure framework with built-in legal safe harbor for
  researchers.* `[HIGH]` — https://github.com/bugcrowd/disclosure-policy/commit/10ea3e10c26f237cd8eca3453d816bedf251d640
- **2014-07-24** — **launch press** (~15h after the commit): PRNewswire *"Bugcrowd Releases Open Source
  Responsible Disclosure Framework"* + Threatpost, both pointing at the repo, quoting CipherLaw's Jim
  Denaro. `[HIGH]` — https://www.prnewswire.com/news-releases/bugcrowd-releases-open-source-responsible-disclosure-framework-268435072.html
- **2014-10-16** — earliest Wayback capture of the Bugcrowd framework repo. `[HIGH]` — Wayback

### 2017–2018 — the legal-safe-harbor idea crystallizes
- **2017** — Amit Elazari's safe-harbor scholarship begins (DEF CON Skytalks / BSidesLV,
  unrecorded). *Goal: make legal safe harbor a standardized norm, not a per-program favor.*
  `[MED — stage unconfirmed]`
- **2017-07** — U.S. **DOJ Criminal Division** publishes *"A Framework for a Vulnerability Disclosure
  Program for Online Systems," v1.0* — the guidance Elazari's template README credits. `[HIGH]` —
  https://www.justice.gov/criminal-ccips/page/file/983996/download
- **2017-08** — **CERT/CC** publishes *The CERT Guide to Coordinated Vulnerability Disclosure*
  (CMU/SEI-2017-SR-022). `[HIGH]` — https://www.sei.cmu.edu/library/the-cert-guide-to-coordinated-vulnerability-disclosure-2/
- **2018-01-16/18** — Enigma 2018 talk *"Hacking the Law: Are Bug Bounties a True Safe Harbor?"*
  `[HIGH]` — https://www.usenix.org/conference/enigma2018/presentation/elazari
- **2018-03-21** — **Dropbox "Protecting Security Researchers"**: the first "'authorized' conduct under
  the CFAA" + DMCA-waiver safe-harbor language in this corpus (Wayback-pinned; corrects an earlier
  "March 2017"). `[HIGH]` — https://web.archive.org/web/20180321173139/https://blogs.dropbox.com/tech/2018/03/protecting-security-researchers/
- **2018-03-29** — `EdOverflow/legal-bug-bounty` templates repo created. `[HIGH]` —
  https://github.com/EdOverflow/legal-bug-bounty
- **2018-04-12** — SSRN paper *"Private Ordering Shaping Cybersecurity Policy: The Case of Bug
  Bounties"* (SSRN ID **3161758** — no DOI exists; cite the ID). `[HIGH, page bot-blocks curl but
  renders in-browser]` — https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3161758

### 2018 — disclose.io is born
- **2018-05-16** — `disclose/diodb` first commit (`0158e3b`) — oldest repo in the disclose org.
  `[HIGH]` — https://github.com/disclose/diodb
- **2018-08-02** — 🚀 **disclose.io launches** (Bugcrowd + Amit Elazari), explicitly merging the
  three predecessors. *Goal (2018 launch-day, verbatim): "a collaborative and vendor-agnostic project to
  standardize best practices around safe harbour for good-faith security research."* `[HIGH]` —
  https://web.archive.org/web/20180802132142/https://disclose.io
- **2018-08-02** — the **launch-day** Wayback capture already shows the full **terms project** ("Read
  the core terms," three tributaries named, "so our hacker friends don't go to jail"). Corrects the
  earlier "first terms capture = 2018-08-29". `[HIGH]` — https://web.archive.org/web/20180802132142/https://disclose.io
- **2018-10** — ISO/IEC 29147 **second edition** (supersedes the 2014 1st ed.) — two months after
  disclose.io's launch. `[HIGH]` — https://web.archive.org/web/20181215190313/https://www.iso.org/standard/72311.html
- **2018-12-07** — diodb's first real program list: **426 organizations** (`698675f`). *Goal:
  track who has adopted safe-harbor terms.* `[HIGH]` — https://github.com/disclose/diodb

### 2020 — the terms get a canonical home + the adoption engine
- **2020-06-30** — `disclose/dioterms` repo first commit (`851a906`). `[HIGH]` —
  https://github.com/disclose/dioterms
- **2020-07-15** — first canonical terms text in the disclose org (`be213be`,
  `generic-core-terms.md`) with an explicit **"Safe Harbor"** section. `[HIGH]`
- **2020-08-12** — `disclose/diosts` (Go security.txt scraper) created — the future adoption
  engine. `[HIGH]` — https://github.com/disclose/diosts
- **2020-09-02** — **CISA BOD 20-01** finalized: every U.S. federal civilian agency must publish
  a VDP. `[HIGH]` — https://www.cisa.gov/news-events/directives/bod-20-01-develop-and-publish-vulnerability-disclosure-policy
- **2020-10-31 → 11-15** — Wayback captures the actual dioterms text + the **2020 mission,
  verbatim**: *"To drive vulnerability disclosure adoption through safety, simplicity, and
  standardization."* `[HIGH]` — https://web.archive.org/web/20201115224220/https://github.com/disclose/dioterms/blob/master/generic-core-terms.md
- **2020-11-16** — 📈 **Adoption inflection**: the `diosts` bot auto-imports security.txt-discovered
  programs, jumping diodb **981 → 3,524 entries in one commit** (`aee74f1`). The spike is
  *automation riding CISA BOD 20-01*, not a conference. `[HIGH]` — https://github.com/disclose/diodb

### 2021–2022 — the vision broadens
- **2021-04-11** — **dioterms licensed CC0-1.0** (public domain): LICENSE file added in commit
  `365c5f86` — *"Change to CC0 1.0 Per recommendation in issues/2."* Note the nuance: the repo is
  2020-06-30, but CC0 adoption is 2021-04-11 — the "2020 CC0 dioterms" shorthand conflates the
  two. *Goal: remove every reuse barrier — the terms become genuinely public infrastructure.*
  `[HIGH]` — https://github.com/disclose/dioterms/commit/365c5f863a633b3e118e566c2b926b84c9c9852a
- **2021** — supporting-standards repos spin out: `dnssecuritytxt` (2021-03), `policymaker`
  (2021-07). *Goal expands toward an ecosystem.* `[HIGH]`
- **2022-04-27** — RFC 9116 (security.txt) published; co-author EdOverflow was an early diodb
  contributor — the two efforts are intertwined. `[HIGH]` — https://www.rfc-editor.org/rfc/rfc9116
- **2022-07-14** — Wayback captures the **2022 mission, verbatim**: *"a cross-industry,
  vendor-agnostic standardization project for safe harbor best practices to enable good-faith
  security research… a straightforward maturity model."* `[HIGH]` —
  https://web.archive.org/web/20220714165017/https://disclose.io/

### 2021–2024 — the surrounding legal landscape (context, not dioterms lineage)
*Parallel developments — not descendants of the dioterms. The safe-harbor norm disclose.io helped
popularize turns up in courts and statutes; no textual derivation is claimed.*
- **2021-06-03** — **Van Buren v. United States** (SCOTUS, No. 19-783) narrows the CFAA's "exceeds
  authorized access," reducing — though expressly *not settling* — researcher exposure (the Court left
  the researcher question open). `[HIGH]` —
  https://www.supremecourt.gov/opinions/20pdf/19-783_k53l.pdf
- **2022-05-19** — **DOJ** revises CFAA charging policy: "good-faith security research should not be
  charged." `[HIGH]` — https://www.justice.gov/archives/opa/pr/department-justice-announces-new-policy-charging-cases-under-computer-fraud-and-abuse-act
- **2022-11-16** — **HackerOne "Gold Standard Safe Harbor"** — platform-level standardization (does not
  cite disclose.io). `[HIGH]` — https://www.hackerone.com/press-release/hackerone-announces-gold-standard-safe-harbor-improve-protections-good-faith-security
- **2022-12-27** — **EU NIS2** (Dir. (EU) 2022/2555), Art. 12 requires a national CVD policy in every
  Member State. `[HIGH]` — https://eur-lex.europa.eu/eli/dir/2022/2555/oj
- **2023-02-15** — **Belgium** — first EU nationwide statutory safe harbor for good-faith research.
  `[HIGH]` — https://web.archive.org/web/20230215171904/https://ccb.belgium.be/en/vulnerability-reporting-ccb
- **2024-12-10** — **EU Cyber Resilience Act** (Reg. (EU) 2024/2847) enters into force — manufacturers
  must have "a policy on coordinated vulnerability disclosure." `[HIGH]` —
  https://eur-lex.europa.eu/eli/reg/2024/2847/oj

### Mainstream adoption (one pre-org outlier, shown out of strict order)
- **2016-11-21** — U.S. DoD VDP / Hack the Pentagon. *The largest adopter that **predates
  disclose.io itself** — placed here because it belongs to the adoption story, not the founding
  chronology. It is NOT evidence the org existed in 2016.* `[HIGH]` — https://hackerone.com/deptofdefense
- **2023-11-03** Target (`f71528c`) · **2024-03-10** Dell (`ddf2f8e`) · **2024-09-28** a16z
  (`6f5b57d`) · **2025-07-20** SIX Group (`0e8e445`) — all dated by the diodb commit that added
  them. `[HIGH]` — https://github.com/disclose/diodb

---

## 📈 Goal evolution (verbatim, dated)

| when | stated goal/mission (verbatim) | source |
|------|-------------------------------|--------|
| **2014** | *(implicit in the framework)* "an open-source disclosure policy with legal safe harbor" | bugcrowd/disclosure-policy |
| **2018** *(pre-pivot)* | "Disclose.io is a community-maintained **resource** for vulnerability disclosure" — the Jan-2018 guidance site, *before* the terms-project pivot of Aug 2018 | Wayback 2018-01/08 |
| **2018** *(launch)* | "a collaborative and vendor-agnostic project to **standardize best practices around safe harbour** for good-faith security research" | Wayback 2018-08-02 |
| **2020** | "To drive vulnerability disclosure adoption through **safety, simplicity, and standardization**" | Wayback 2020-11-15 |
| **2022** | "a **cross-industry, vendor-agnostic standardization project** for safe harbor best practices… a maturity model" | Wayback 2022-07-14 |
| **2026** | "make vulnerability disclosure **safe, simple, and standardized** for everyone" | Wayback 2026-06-04 |

The arc: a **legal artifact** (2014 safe-harbor template) → a **community resource/directory**
(2018) → a **standardization project with a maturity model** (2020–22). The safe-harbor clause is
the invariant; the ambition around it kept widening.

---

## 🔎 Confidence legend & honest caveats

- `[HIGH]` = git commit hash, GitHub API field, RFC/directive, or verified Wayback snapshot.
- `[MED]` = single/secondary source or non-day-precise date.
- **Caveats (carried forward, not hidden):**
  1. The often-cited "DEF CON 26 Legal Bug Bounty talk" could **not** be confirmed as a titled
     DEF CON 26 main-stage talk — likely a conflation with 2017 Skytalks (unrecorded).
  2. The SSRN paper has **no DOI** — cite SSRN ID 3161758. Its page bot-blocks `curl` (403) but
     renders live in a browser.
  3. ISO 29147's first-edition *day* isn't shown on iso.org; the 2014 edition year is confirmed.
  4. ~2-year gap between "terms provably existed on disclose.io" (2018-08) and "terms text is
     archived word-for-word" (2020-11) — Wayback never grabbed the original `core_terms` file,
     only the repo's tree listing.
  5. **An earlier Bugcrowd *terms* artifact exists but isn't the root** — "Standard Disclosure Terms"
     (2014-03) carries researcher-protection intent but **no safe-harbor legal clause**; the
     falsifiable claim is about the earliest *safe-harbor* template, which still resolves to 2014-07-23.
  6. **Earliest-found ≠ earliest-that-exists** — git archaeology establishes the earliest commit
     *located*, not proof none earlier could surface; the 2014-07-23 headline is a retestable conjecture.

## Provenance
All 15 load-bearing URLs checked 2026-05-31: 14× HTTP 200, 1× 403 (SSRN bot-block, live in-browser).
Zero 404s, zero fabricated links. Full ledger: [`sources/LEDGER.md`](sources/LEDGER.md). Original 2014 terms text:
[`sources/2014-07-23_responsible_disclosure_policy_FIRST.md`](sources/2014-07-23_responsible_disclosure_policy_FIRST.md).
