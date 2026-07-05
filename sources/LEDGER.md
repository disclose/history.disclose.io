# Sources Ledger — history.disclose.io

> Every dated claim in TIMELINE.md must trace to a row here. Ground-truth hierarchy:
> git commit author-dates + Wayback snapshot timestamps > publish dates > recollection.

| date | artifact | type | how dated | url | confidence | note |
|------|----------|------|-----------|-----|------------|------|
| 2020-11-15 | disclose.io 2020 mission (verbatim), via the dioterms text | wayback | snapshot ts | https://web.archive.org/web/20201115224220/https://github.com/disclose/dioterms/blob/master/generic-core-terms.md | HIGH | "To drive vulnerability disclosure adoption through safety, simplicity, and standardization." |
| 2022-07-14 | disclose.io 2022 mission (verbatim) | wayback | snapshot ts | https://web.archive.org/web/20220714165017/https://disclose.io/ | HIGH | "a cross-industry, vendor-agnostic standardization project for safe harbor best practices... a maturity model." |
| 2013-03-05 | Bugcrowd "The List" — bug-bounty directory | wayback | snapshot ts | http://web.archive.org/web/20130305011641/http://bugcrowd.com/list-of-bug-bounty-programs | MED | Directory antecedent of diodb; conceptual only. |
| 2010-07-22 | Microsoft MSRC responsible→coordinated rename | wayback | post byline + snapshot | https://web.archive.org/web/20100724135757/http://blogs.technet.com/b/msrc/archive/2010/07/22/announcing-coordinated-vulnerability-disclosure.aspx | HIGH | Terminology neutrality pivot. |
| 2013-11 | ISO/IEC 30111 1st ed. (vuln handling) | standard | iso.org catalog via wayback | https://web.archive.org/web/20171220083905/https://www.iso.org/standard/53231.html | HIGH | Predates ISO 29147:2014 by ~3mo. |
| 2018-10 | ISO/IEC 29147 2nd ed. | standard | iso.org catalog via wayback | https://web.archive.org/web/20181215190313/https://www.iso.org/standard/72311.html | HIGH | Supersedes 2014 1st ed. |
| 2014-03-31 | Bugcrowd "Standard Disclosure Terms" | wayback | snapshot ts + in-page changelog | http://web.archive.org/web/20140411213116/http://blog.bugcrowd.com:80/standard-disclosure-terms/ | HIGH capture / MED release-day | Earlier Bugcrowd terms artifact; NO safe-harbor clause; not the root. |
| 2014-07-15 | Google Project Zero announced (+90-day 2015-02-13) | press | post byline | https://projectzero.google/2014/07/announcing-project-zero.html | HIGH | Disclosure-clock antecedent; 8d before the root commit. |
| 2014-07-24 | Launch press: PRNewswire + Threatpost | press | dateline / article ts | https://www.prnewswire.com/news-releases/bugcrowd-releases-open-source-responsible-disclosure-framework-268435072.html | HIGH | Third-party press ~15h after 10ea3e1. Threatpost: https://threatpost.com/bugcrowd-releases-open-source-vulnerability-disclosure-framework/107399/ |
| 2017-07 | DOJ Framework for a VDP for Online Systems v1.0 | gov | in-doc version/date | https://www.justice.gov/criminal-ccips/page/file/983996/download | HIGH | Credited in Elazari's template README. |
| 2017-08 | CERT Guide to CVD (CMU/SEI-2017-SR-022) | doc | SEI library date | https://www.sei.cmu.edu/library/the-cert-guide-to-coordinated-vulnerability-disclosure-2/ | HIGH | Canonical CVD handbook. |
| 2018-03-21 | Dropbox "Protecting Security Researchers" | wayback | earliest capture + live byline | https://web.archive.org/web/20180321173139/https://blogs.dropbox.com/tech/2018/03/protecting-security-researchers/ | HIGH | First CFAA-authorized safe harbor in corpus. Corrects earlier '2017' — zero 2017 captures. |
| 2018-08-02 | disclose.io launch-day terms-project capture | wayback | snapshot ts | https://web.archive.org/web/20180802132142/https://disclose.io | HIGH | Corrects earliest-terms-capture 08-29→08-02; carries launch-day goal quote. |
| 2021-06-03 | Van Buren v. United States (SCOTUS 19-783) | court | slip-opinion date | https://www.supremecourt.gov/opinions/20pdf/19-783_k53l.pdf | HIGH | CFAA 'exceeds authorized access' narrowed. |
| 2022-05-19 | DOJ revised CFAA charging policy | gov | press-release date + wayback | https://www.justice.gov/archives/opa/pr/department-justice-announces-new-policy-charging-cases-under-computer-fraud-and-abuse-act | HIGH | 'Good-faith security research should not be charged.' |
| 2022-11-16 | HackerOne Gold Standard Safe Harbor | press | press-release date | https://www.hackerone.com/press-release/hackerone-announces-gold-standard-safe-harbor-improve-protections-good-faith-security | HIGH | Platform-level standardization; does not cite disclose.io. |
| 2022-12-27 | EU NIS2 Directive (EU) 2022/2555, Art. 12 | eu-law | OJ publication date | https://eur-lex.europa.eu/eli/dir/2022/2555/oj | HIGH | National CVD policy required per Member State. |
| 2023-02-15 | Belgium national CVD safe-harbor framework | gov | CCB page + earliest wayback | https://web.archive.org/web/20230215171904/https://ccb.belgium.be/en/vulnerability-reporting-ccb | HIGH | First EU nationwide statutory safe harbor. |
| 2024-12-10 | EU Cyber Resilience Act (Reg. (EU) 2024/2847) | eu-law | OJ + EC in-force date | https://eur-lex.europa.eu/eli/reg/2024/2847/oj | HIGH | CVD policy required of manufacturers. EC: https://digital-strategy.ec.europa.eu/en/policies/cyber-resilience-act |
| 2026-06-04 | disclose.io 2026 mission restatement | wayback | snapshot + live | https://web.archive.org/web/20260604052740/https://disclose.io/ | HIGH | "safe, simple, and standardized for everyone." |
| 2026-06-03 | directory.disclose.io first capture | wayback | earliest capture (upper bound) | https://directory.disclose.io/ | MED | Hosted diodb front-end; capture is an upper bound, not a launch date. |
| 2014-07-23 | bugcrowd/disclosure-policy **first commit** `10ea3e1` "first commit" by Chris Raethke | git | commit author-date | https://github.com/bugcrowd/disclosure-policy/commit/10ea3e10c26f237cd8eca3453d816bedf251d640 | HIGH | THE EARLIEST KNOWN ANCESTOR. Added `responsible_disclosure_policy.md` + `setting_up_a_responsible_disclosure_program.md`. Already contains safe-harbor core: "Not pursue or support any legal action related to your research." |
| 2014-07-24 | bugcrowd/disclosure-policy repo created | github api | created_at field | https://github.com/bugcrowd/disclosure-policy | HIGH | Desc: "Open Source Vulnerability Disclosure Framework. Maintained by Bugcrowd and Cipherlaw. **Merged with github.com/disclose/dioterms.**" — the explicit chain to disclose.io |
| 2018-04-04 | Terminology rename: responsible→vulnerability disclosure (Jason Haddix commits) | git | commit author-date | https://github.com/bugcrowd/disclosure-policy/commit/cc83616 | HIGH | `responsible_disclosure_policy.md`→`vulnerability_disclosure_policy.md`. The responsible→coordinated/VDP terminology shift, datable in-repo. |
| 2016-10-02 | disclose.io earliest Wayback snapshot (301 redirect) | wayback cdx | snapshot timestamp | http://web.archive.org/web/20161002234519/http://disclose.io/ | HIGH | Brand existed/registered by 2016; redirect only. |
| 2018-01-18 | disclose.io first HTTP 200 Wayback snapshot | wayback cdx | snapshot timestamp | https://web.archive.org/web/20180118045058/https://disclose.io/ | HIGH | First live disclose.io content. |
| 2018-05-17 | disclose/diodb repo created (oldest in disclose org) | github api | created_at | https://github.com/disclose/diodb | HIGH | The disclose.io database/directory — adoption tracking begins. |
| 2020-06-30 | disclose/dioterms repo created | github api | created_at | https://github.com/disclose/dioterms | HIGH | Terms get their own canonical repo (language predates it by ~6 yrs). |
| 2020-06-30 | disclose/dioseal + disclose/resources created | github api | created_at | https://github.com/disclose/dioseal | HIGH | dioseal (trust seal), resources. |
| 2021-01-19 | disclose/website created | github api | created_at | https://github.com/disclose/website | HIGH | Current site repo. |

## Headline finding (falsifiable conjecture)

**EARLIEST PROVENANCE ROOT of the dioterms lineage = 2014-07-23**, `bugcrowd/disclosure-policy`
first commit `10ea3e1`. NOT itself a "dioterm" (disclose.io didn't exist until 2018) — it is the
earliest repo-documented *ancestor* ("Merged with disclose/dioterms"). The safe-harbor clause —
dioterms' defining feature — is present in the very first 2014 file. **Date hardened to [HIGH]:**
author==committer date, root commit (no parent, not an import), clean 3-file initial commit, and
independently corroborated by Wayback capturing the live repo 2014-10-16. **Refutation search:**
no earlier Bugcrowd template/gist/snapshot found pre-2014-07-23.

## Platform pre-history — "crowdsourced security as a service" (the market soil)

| date | artifact | how dated | url | conf | note |
|------|----------|-----------|-----|------|------|
| 2012 | **Bugcrowd & HackerOne both founded; Bugcrowd launched first** — per @senorarroz (Alex Rice, HackerOne co-founder/CTO): "Both founded 2012, @Bugcrowd launched first! @Hacker0x01 kickoff 2/2012, 1st commit 4/2012, 1st private 1/2013, 1st public 10/2013" | tweet (primary, a founder on record) | https://x.com/senorarroz/status/779402727885410304 | HIGH | The crowdsourced-security-as-a-service category begins (demand soil for dioterms). **Archived verbatim (w/ reply context):** [`sources/2016-09-23_alex-rice-crowdsourced-security-2012-origin.md`](2016-09-23_alex-rice-crowdsourced-security-2012-origin.md). Tweet dated 2016-09-23; facts asserted are 2012-2013. |

## Confirmed by archaeology agents (2026-05-31)

### Predecessor / origins lineage
| date | artifact | how dated | url | conf |
|------|----------|-----------|-----|------|
| 2000-08-19 | **RFPolicy v1.1** (Rain Forest Puppy) live on wiretrip.net — first formalized disclosure-policy template | wayback snapshot (primary) | http://web.archive.org/web/20000819053824/http://www.wiretrip.net/rfp/policy.html | HIGH | **Cleanest PRE-2014 anchor**, upgraded MED→HIGH 2026-07-01: earliest Wayback capture (200) of the policy page shows "Issue disclosure policy v1.1" verbatim. Wikipedia row retired as source. |
| 2000-10-17 | **RFPolicy v2.0** first captured ("Full Disclosure Policy (RFPolicy) v2.0"; "5 working days" window) | wayback snapshot + packetstorm raw text (primary) | http://web.archive.org/web/20001017192112/http://www.wiretrip.net/rfp/policy.html | HIGH | v2.0 went live between 2000-08-19 and 2000-10-17 (bracketed by snapshots). Full raw text: https://dl.packetstormsecurity.net/papers/general/rfpolicy-2.0.txt (fetched 2026-07-01). Packet Storm *posting* date unverified — do not cite it. |
| 2002-02-15 | IETF draft "Responsible **Vulnerability** Disclosure Process" (Christey/MITRE + Wysopal/@stake), rev 00 | datatracker submission date (primary) | https://datatracker.ietf.org/doc/draft-christey-wysopal-vuln-disclosure/ | HIGH | Upgraded MED→HIGH 2026-07-01: datatracker fetched, rev-00 submission 2002-02-15; expired individual draft, only rev 00 exists. Terminology root: "responsible disclosure". |
| 2014-02 | ISO/IEC 29147 first edition (vuln disclosure standard) | vendor catalog (iso.org confirms 2014 ed., not day-precise) | https://www.iso.org/standard/45170.html | MED | standards backdrop |
| 1988 | CERT/CC founded (oldest diodb dataset entry, self-reported) | dataset field | (diodb program_list) | MED | historical root only |

### #LegalBugBounty / Amit Elazari thread (the legal-safe-harbor idea)
| date | artifact | how dated | url | conf |
|------|----------|-----------|-----|------|
| 2017 | Elazari academic foundation — DEF CON Skytalks / BSidesLV (unrecorded) | secondary | — | MED | NOTE: brief's "DEF CON 26 talk" unconfirmed — likely 2017 Skytalks conflation |
| 2018-01-16/18 | Enigma 2018 talk "Hacking the Law: Are Bug Bounties a True Safe Harbor?" | conf program | https://www.usenix.org/conference/enigma2018/presentation/elazari | HIGH |
| 2018-03-29 | `EdOverflow/legal-bug-bounty` templates repo created | github api | https://github.com/EdOverflow/legal-bug-bounty | HIGH |
| 2018-04-12 | SSRN paper "Private Ordering Shaping Cybersecurity Policy: The Case of Bug Bounties" (SSRN ID 3161758 — NO DOI, cite the ID) | ssrn posted date | https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3161758 | HIGH |

### disclose.io org — GitHub ground truth (commit author-dates)
| date | artifact | commit | url | conf |
|------|----------|--------|-----|------|
| 2018-08-02 | **disclose.io launched** (Bugcrowd + Amit Elazari) — merged 3 predecessors: Bugcrowd+CipherLaw 2014 framework, Elazari #legalbugbounty, Dropbox researcher-protection language | press | https://www.bugcrowd.com/blog/introducing-disclose-io/ | HIGH |
| 2018-05-16 | disclose/diodb first commit | `0158e3b` | https://github.com/disclose/diodb | HIGH | oldest in disclose org |
| 2018-12-07 | diodb first actual program list (426 entries) | `698675f` | https://github.com/disclose/diodb | HIGH |
| 2020-06-30 | disclose/dioterms repo first commit (README) | `851a906` | https://github.com/disclose/dioterms | HIGH |
| 2020-07-15 | dioterms first actual terms text in disclose org | `be213be` | https://github.com/disclose/dioterms | HIGH | "Safe Harbor" section matures here |
| 2021-04-11 | **dioterms licensed CC0-1.0** — LICENSE file added, "Change to CC0 1.0 Per recommendation in issues/2" | `365c5f86` (commit author-date 2021-04-11T05:56:49Z; only commit ever touching LICENSE) | https://github.com/disclose/dioterms/commit/365c5f863a633b3e118e566c2b926b84c9c9852a | HIGH | Added 2026-07-01. Nuance: repo created 2020-06-30, but CC0 adoption is 2021-04-11 — "2020 CC0 dioterms" shorthand conflates the two. GitHub API license field confirms `CC0-1.0` as of 2026-07-01. |
| 2020-08-12 | disclose/diosts (Go security.txt scraper) created | repo | https://github.com/disclose/diosts | HIGH | drove the adoption spike |
| — | **No git tags/releases** on dioterms/diodb/disclosure-policy — versioning was via in-repo `archive/` + dated filenames | git tag | — | HIGH | no tagged versions exist |

### Adoption axis
| date | org/event | commit/source | url | conf |
|------|-----------|--------------|-----|------|
| 2016-11-21 | U.S. DoD VDP (Hack the Pentagon) | — | https://hackerone.com/deptofdefense | HIGH |
| 2020-09-02 | CISA BOD 20-01 finalized (forced US federal VDPs) | directive | https://www.cisa.gov/news-events/directives/bod-20-01-develop-and-publish-vulnerability-disclosure-policy | HIGH | macro driver |
| 2020-11-16 | **Inflection: diosts bot auto-imports security.txt programs** → diodb 981→3,524 in one commit | `aee74f1` | https://github.com/disclose/diodb | HIGH | automation, not a conference |
| 2022-04-27 | RFC 9116 (security.txt) published — EdOverflow co-author (early diodb contributor) | rfc | https://www.rfc-editor.org/rfc/rfc9116 | HIGH |
| 2023-11-03 | Target added to diodb | `f71528c` | https://github.com/disclose/diodb | HIGH |
| 2024-03-10 | Dell added | `ddf2f8e` | https://github.com/disclose/diodb | HIGH |
| 2024-09-28 | a16z added | `6f5b57d` | https://github.com/disclose/diodb | HIGH |
| 2025-07-20 | SIX Group added | `0e8e445` | https://github.com/disclose/diodb | HIGH |
| 2026-07-01 | diodb currently holds **2,408 entries** (program-list.json length) — the 3,524 bot-import peak of 2020-11-16 was later **curated down** | raw file fetch + count | https://raw.githubusercontent.com/disclose/diodb/master/program-list.json | HIGH | Added 2026-07-01. Latest diodb commit `1a43861` 2026-06-22 (CI validation fix); 1,072 stars. |

## Lineage afterlife — safe harbor extends to AI research (2026)

| date | artifact | how dated | url | conf | note |
|------|----------|-----------|-----|------|------|
| 2026-01-20 | **HackerOne "Good Faith AI Research Safe Harbor"** — industry framework extending safe-harbor authorization to good-faith AI-system testing | press release publish date | https://www.hackerone.com/press-release/hackerone-sets-standard-ai-era-testing-good-faith-ai-research-safe-harbor | HIGH | Does NOT mention disclose.io/dioterms — descendant of the safe-harbor standardization *idea*, not a documented textual derivation. Conceptual-antecedent framing applies in reverse. |

## Research-refresh log

- **2026-07-01 pass:** all 24 load-bearing URLs re-probed — 22× resolve 200 (Wayback 429s cleared on retry), SSRN 403 (known bot-block, live in-browser), **iso.org now also 403s curl** (new since May — bot-block, page live in-browser; annotate, not dead). RFPolicy + IETF rows upgraded MED→HIGH on primary fetches (reconciling the ledger with `research/predecessor-language-lineage.md`, which had already fetched both primary texts on 2026-06-21). CC0 licensing row added. Refutation hunt re-run on the 2014-07-23 headline (see below).
- **Resolved:** earliest terms-text snapshot 2020-11-15, goal snapshots 2018/2020/2022 (see TIMELINE.md). Section retired 2026-07-01.
