# Predecessor Policy Language Lineage & Feature Evolution

> How the disclosure-policy genre evolved from 2000 → 2022, traced by **actual fetched text**.
> Companion to `TIMELINE.md`. Compiled 2026-06-21. Every quote below was retrieved verbatim from a
> working URL this session (GitHub raw, IETF archive, Packet Storm, Wayback, iso.org, dropbox.tech, CERT/CC).
> Confidence: `[HIGH]` = verbatim from primary text · `[MED]` = secondary/abstract · `[LOW]` = inferred.
>
> **Method note (read this):** this is a *textual-lineage* analysis — it compares the words policies
> use. Textual similarity is **not** authorship provenance: no commit-level "who-typed-what" diff
> exists for cross-organization legal text. Where this doc says a phrase "first appears" or "is
> attested," it means *within the seven documents fetched here*, not "was invented then." Genealogy
> claims are framed as concordance/convergence, not derivation.

---

## TL;DR — three findings

1. **The clause has three distinct authors, and the legal magic word is Dropbox's, not Elazari's.**
   The *bilateral goodwill promise* ("we commit to: Not pursue or support any legal action") is
   **2014, Bugcrowd**. The **legally-operative word "authorized"** — the exact term that negates the
   CFAA's "without authorization" element — first appears in this corpus in **Dropbox's March 2018**
   policy (*"'authorized' conduct under the Computer Fraud and Abuse Act"*), a year *before* Amit
   Elazari's 2018 `#legalbugbounty` template — whose own README credits *"leading policies like
   Dropbox."* Elazari's 2018 contribution was **standardization** (a reusable, statute-naming
   template); dioterms (2020) **parameterized** the result. The modern clause shows **textual
   concordance with three documented predecessors**, matching disclose.io's own "three tributaries"
   attribution — not a two-parent fusion.
2. **The earliest feature is the clock, not the contract.** A *disclosure window* (RFPolicy's "5
   working days," 2000) is the genre's founding feature and the only one present in every policy
   since. Safe harbor is the **last** major feature to appear, ~17 years later.
3. **The center of gravity migrated:** process (2000) → shared terminology + roles (2002) → neutral
   naming + vendor standard (2010–14) → reusable template (2014) → **legal protection (2017–18)** →
   machine-readable standardization + government mandate (2020–22). Each layer was added when a new
   **failure mode** became the dominant pain.

---

## The corpus (8 documents, all fetched this session)

| # | Document | Date | Source (verified) | Conf |
|---|----------|------|-------------------|------|
| 1 | **RFPolicy** (Rain Forest Puppy) v1 "Issue disclosure policy v1.1" / v2.0 | 2000-06 / 2001 | Packet Storm raw `rfpolicy-2.0.txt`; Wayback of `wiretrip.net/rfp/policy.html` (2000-08-19); Bugtraq 2000-06-12 | [HIGH] |
| 2 | **IETF draft** "Responsible **Vulnerability** Disclosure Process" (Christey/MITRE + Wysopal/@stake) | 2002-02 | `ietf.org/archive/id/draft-christey-wysopal-vuln-disclosure-00.txt` (full 61 KB) | [HIGH] |
| 3 | **ISO/IEC 29147** "Vulnerability disclosure" 1st ed. | 2014-02 | `iso.org/standard/45170.html` (public abstract; body paywalled; now *withdrawn*/superseded 2018) | [MED] |
| 4 | **Bugcrowd** "Open Source Vulnerability Disclosure Framework" (`responsible_disclosure_policy.md`) | 2014-07-23 | local `sources/2014-07-23_responsible_disclosure_policy_FIRST.md` (commit `10ea3e1`) | [HIGH] |
| 5 | **Dropbox** "Protecting security researchers" VDP | 2018-03 | `dropbox.tech/security/protecting-security-researchers` (canonical home of the orig. `blogs.dropbox.com` post) | [HIGH] |
| 6 | **Elazari `#legalbugbounty`** `safe_harbor.md` template + README (EdOverflow repo) | 2018-03/04 | `raw.githubusercontent.com/EdOverflow/legal-bug-bounty/master/` | [HIGH] |
| 7 | **disclose.io dioterms** `core-terms-vdp.md` / `core-terms-bbp.md` | 2018→2020 | `raw.githubusercontent.com/disclose/dioterms/master/` | [HIGH] |
| 8 | *(context)* CISA BOD 20-01 mandate; RFC 9116 `security.txt` | 2020 / 2022 | cisa.gov; rfc-editor.org | [HIGH] |

disclose.io's 2018 launch credited **three tributaries** — Bugcrowd+CipherLaw's framework (#4),
Elazari's `#legalbugbounty` (#6), and Dropbox's researcher-protection language (#5). **All three are
now fetched.** Terminology authority: CERT/CC *Guide to CVD*.

---

## Part 1 — Feature comparison matrix

Features derived first-principles (what a disclosure policy fundamentally must provide):

| Feature | RFPolicy 2000 | IETF 2002 | ISO 29147 2014 | Bugcrowd 2014 | **Dropbox 2018** | Elazari 2018 | dioterms 2020 |
|---|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| **A. Reporting channel** | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ |
| **B. Scope (in/out)** | ❌ | ⚪ | ✅ | ✅ | ✅ | ➖ | ✅ |
| **C. Disclosure window** | ✅ 5 working days | ✅ 30d resolve / 30d grace | ❔ paywalled | ✅ [90] days | ⚪ policy-set | ➖ | ✅ `{{disclosure_window}}` |
| **D. Researcher good-faith conduct** | ✅ | ✅ | ❌ | ✅ | ✅ | ➖ | ✅ |
| **E. Vendor commitments** | ⚪ encouraged | ✅ non-binding BCP | ✅ vendor process | ✅ 72h + HoF | ✅ pledges | ➖ | ✅ "Our Commitments" |
| **F. Legal safe harbor** | ❌ *disclaims* legal force | ❌ (0 occurrences) | ❌ | ⚪ goodwill "won't pursue" | ✅✅ **CFAA "authorized" + DMCA + 3rd-party** | ✅✅ + Cal 502(c), templatized | ✅ structured (anti-hacking + anti-circumvention + TOS/AUP) |
| **G. Bilateral "we commit / we expect"** | ❌ | ⚪ | ❌ | ✅ | ✅ | ✅ | ✅ |
| **H. Standardization / reusable** | ✅ free-to-reuse | ✅ BCP/RFC2119 | ✅ ISO std | ✅ OSS template | ✅ open-sourced its VDP | ✅✅ template project | ✅ `{{templated}}` + maturity model |
| **I. Machine-readability / automation** | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ diodb + diosts + `security.txt` |
| **J. Self-applied label** | "Full Disclosure" | "Responsible" | "Vulnerability disclosure" | "Responsible Disclosure" | "VDP / protect researchers" | "Safe Harbor" | "VDP / BBP + Safe Harbor" |

✅ present · ⚪ partial/weak · ➖ N/A (clause-insert, not a whole policy) · ❌ absent · ❔ unknown (not retrievable)

---

## Part 2 — Language lineage (verbatim phrase propagation)

### Thread 1 — the disclosure window (oldest feature; continuously present)
- **RFPolicy v2.0 (2000)** [HIGH]: *"The MAINTAINER is to be given **5 working days**… should no contact occur by the end of 5 working days, the ORIGINATOR should disclose the ISSUE."* (v1 was *"at least 48 hours… to respond"* + 5 days; v2 dropped the 48h clause as too ambiguous.)
- **IETF (2002)** [HIGH]: *"resolve the vulnerability **within 30 days**"* + a *"**Grace Period** up to 30 days."*
- **Bugcrowd (2014)** [HIGH]: *"Keep information… confidential… until we've had **[90] days** to resolve the issue."*
- **dioterms (2020)** [HIGH]: *"at least **`{{disclosure_window}}` days** from the initial report."*
- **Arc:** fixed 5-day ultimatum → negotiable 30 → 90 → **parameterized** variable. The window evolves from leverage-against-stonewalling into a mutually-agreed setting.

### Thread 2 — the actor vocabulary
- **RFPolicy (2000)** [HIGH]: **ORIGINATOR** / **MAINTAINER** / **ISSUE**.
- **IETF (2002)** [HIGH]: **Reporter / Vendor / Coordinator / Customer** — *"A Coordinator… works with the Reporter and the Vendor."* The modern **Reporter–Vendor–Coordinator triad is fixed here, 2002,** and survives into CERT/CC CVD and ISO 29147.

### Thread 3 — the safe-harbor clause (three stages, verbatim)
- **Stage 1 — Bugcrowd 2014 (goodwill promise, no statutes)** [HIGH]: *"If you follow these guidelines… we commit to: **Not pursue or support any legal action related to your research**."*
- **Stage 2 — Dropbox March 2018 (the legal instrument — where "authorized" enters)** [HIGH]: *"a clear statement that we consider actions consistent with the policy as constituting **'authorized' conduct under the Computer Fraud and Abuse Act (CFAA)**"* · *"a pledge that we **won't bring a Digital Millennium Copyright Act (DMCA) action**…"* · *"if a third party initiates legal action, Dropbox will make it clear when a researcher was acting in compliance with the policy (**and therefore authorized by us**)."*
- **Stage 3 — Elazari `#legalbugbounty` 2018 (standardization)** [HIGH]: *"we will not pursue civil action or initiate a complaint to law enforcement for accidental, good faith violations… We consider [this] **'authorized' conduct under the Computer Fraud and Abuse Act, the DMCA and applicable anti-hacking laws such as Cal. Penal Code 502(c)**."* The README credits its basis: *"…the DOJ guidelines… and some leading policies like **Dropbox**."* Adds reusable templates + a state statute.
- **Stage 4 — dioterms 2020 (parameterized synthesis)** [HIGH]: *"**Authorized** concerning any applicable anti-hacking laws, and we will **not initiate or support legal action**… **Authorized** concerning any relevant anti-circumvention laws… **Exempt** from restrictions in our Terms of Service (TOS) and/or Acceptable Usage Policy (AUP)… **Lawful**, helpful… and conducted in good faith."*

**What the concordance shows (similarity, not a proven derivation chain):**
- The **bilateral "we commit / we expect" structure** traces to **Bugcrowd 2014**.
- The **statutory "authorized under the CFAA" + DMCA waiver + third-party caveat** is present in **Dropbox 2018**, *before* Elazari's template — so "authorized" is **not** an Elazari invention; her project **standardized and credited** it.
- dioterms' verb-phrase *"not initiate or support legal action"* mirrors Bugcrowd's *"not pursue or support any legal action"*; its *"Authorized concerning… anti-hacking laws"* mirrors the Dropbox/Elazari *"authorized conduct under the CFAA / anti-hacking laws."*
- dioterms then **adds clauses none of the three parents isolated**: an explicit standalone **anti-circumvention** bullet and a **TOS/AUP carve-out** — the two non-CFAA traps researchers hit next.

### ⚠ Provenance limitation
The Stage-1→4 ordering is **chronological attestation across fetched texts**, not a proven author-to-author derivation. "Pursue/support legal action" is partly generic legalese that independent counsel could converge on; common-ancestor convention and parallel drafting are not excluded. The claim defended here is *concordance + chronology*, corroborated by disclose.io's own three-tributary attribution and Elazari's explicit Dropbox credit — not a commit-level diff.

---

## Part 3 — terminology evolution (accreting layers, not replacements)

| Era | Label | Why it changed | Source |
|-----|-------|----------------|--------|
| 2000 | **Full Disclosure** | RFP ethos: *"if the issue is to be disclosed, all aspects of it should be disclosed."* | RFPolicy v2.0 [HIGH] |
| 2002 | **Responsible Disclosure** | IETF: "responsible" = *"a formal, repeatable process for the reporting, evaluation, resolution and publication of vulnerability information."* | IETF draft [HIGH] |
| 2010–14 | **Coordinated (CVD)** | CERT/CC: *"what constitutes responsible behavior is a matter of opinion… framed within the values of whoever is using the term"* → neutral "coordinated." ISO 29147:2014 dropped "responsible" from its title. | CERT/CC [HIGH] |
| 2017–18 | **Safe Harbor** | A *legal-protection* framing layered on top of CVD (Dropbox → Elazari → dioterms). | Dropbox / Elazari [HIGH] |

The names accrete: *full* = **completeness**, *responsible* = **process**, *coordinated* = **neutrality**, *safe harbor* = **legality**. dioterms speaks all four dialects at once.

---

## Part 4 — how the needs evolved (the demand-side)

Each feature appeared when a new **fear or friction** became the dominant pain:

1. **2000 — fear: vendor stonewalling.** Finders had no leverage. *Need → a deadline.* RFPolicy's
   innovation is "5 days, then I publish" — and it deliberately *disclaims* legal weight (*"This
   policy has no legal merit what-so-ever"*); the leverage is social.
2. **2002 — fear: multi-party chaos & antagonism.** *Need → roles + a repeatable process.* IETF's
   goal: *"Minimize the amount of antagonism."* Gives the Reporter/Vendor/Coordinator triad + clocks.
3. **2010–2014 — fear: "responsible" is a weapon.** *Need → neutral terminology + a vendor-side
   standard* (CVD; ISO 29147 — guidance for vendors who *receive* reports, explicitly not a researcher
   document).
4. **2014 — friction: every program reinvents the policy.** Bug bounties scaling (Bugcrowd &
   HackerOne since 2012). *Need → a copy-pasteable open-source template* + a bilateral **goodwill**
   no-legal-action promise (Bugcrowd's framework).
5. **2017–2018 — fear: researchers actually getting prosecuted (CFAA/DMCA).** Goodwill wasn't legally
   operative; the DOJ issued a framework (2017); real legal threats mounted. **Dropbox (March 2018)**
   shipped the first operative safe harbor naming the CFAA + DMCA + the magic word "authorized," and
   open-sourced it; **Elazari (2018)** turned it into a standardized, reusable, statute-naming
   template — README: *"safe harbor is the exception, not the standard and thousands… are put in
   legal's harm way."* *Need → legally-operative, standardized safe harbor.*
6. **2018–2020 — friction: adoption at scale + machine discovery.** *Need → standardization,
   parameterization (`{{organization}}`), program-type variants (BBP vs VDP), a maturity model, and
   machine-readability* (diodb directory + diosts scraper + `security.txt`).
7. **2020–2022 — driver: government mandate + automation.** CISA BOD 20-01 forced U.S. federal VDPs;
   RFC 9116 standardized `security.txt`. *Need → machine-discoverable, mandated adoption* — the
   inflection that jumped the diodb directory **981 → 3,524 in one commit.**

**The throughline:** a disclosure policy started as a *threat* ("fix it or I publish"), became a
*protocol* (roles, clocks), then a *brand-neutral standard*, then a *reusable contract*, then a
*legal shield*, and finally a *machine-readable, government-mandated interface*. The safe-harbor
clause everyone now treats as the heart of the dioterms is the genre's **most recent** organ — and
it assembled across three orgs (Bugcrowd's bilateral promise, Dropbox's statutory "authorized"
language, Elazari's standardization) before dioterms parameterized it.

---

## Sources & confidence
All primary quotes [HIGH], fetched verbatim this session, except ISO 29147 body [MED] (abstract only;
paywalled). The IETF draft's exact title is *"Responsible **Vulnerability** Disclosure Process"* (it
expired Aug 2002, never an RFC). ISO 29147:2014 1st ed. is *withdrawn* (superseded 2018). The Dropbox
quotes are from `dropbox.tech/security/protecting-security-researchers`, the canonical current home of
the original 2018-03-21 `blogs.dropbox.com/tech/2018/03` announcement (Wayback-pinned to 2018-03-21; the raw HTML there yields the verbatim quotes).

## Caveats
- **Similarity ≠ provenance** (see the ⚠ box in Part 2): no commit/authorship diff exists for
  cross-org legal text; the genealogy is concordance + chronology, corroborated by disclose.io's own
  three-tributary attribution and Elazari's explicit Dropbox credit.
- The dioterms `core-terms-{vdp,bbp}.md` reflect the repo's **current** (`master`) text; the
  2020-07-15 `generic-core-terms.md` milestone in `TIMELINE.md` is the same lineage earlier (the repo
  later split into BBP/VDP/simple-safeharbor variants + a maturity model).
- The Dropbox announcement is Wayback-pinned to **2018-03-21** (an earlier draft said "March 2017"; corrected 2026-07-05). The exact word-for-word body of
  Dropbox's *policy* (vs. the announcement describing it) were not pinned to a dated snapshot this
  session — a follow-up probe if day-precision is needed.
