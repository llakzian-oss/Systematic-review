# PRISMA-Compliant Search Strategy

**Research question:** How does corruption influence infrastructure maintenance spending and infrastructure quality in developing countries?

**Status:** Draft search strategy, cross-checked against a 12-study benchmark set. Ready for information-specialist peer review (PRESS checklist) before execution.

---

## 1. Method used to build this strategy

1. Titles, abstracts, and (where retrievable) keywords of all 12 benchmark studies were read and coded into concepts.
2. Concepts were grouped into two **mandatory** blocks (Corruption; Infrastructure/Public-Expenditure Domain) combined with `AND`. Each block is internally a large synonym `OR` set, truncated wherever the database supports it.
3. A third concept — **geography (developing countries)** — was deliberately **excluded from the mandatory search logic**. Two benchmark papers (Hessami 2014 = OECD countries; Chen, Liu & Lee 2020 = US states) are not about developing countries at all, so requiring geographic terms in the search string would exclude them. Geography is instead applied as a **title/abstract screening criterion**, which is standard PRISMA practice for keeping search sensitivity high while still applying eligibility criteria downstream.
4. No theory-of-mechanism terms (e.g., "principal-agent", "rent-seeking theory") were required, per instruction — many benchmark studies are purely empirical and never name a theory.
5. Each benchmark study's title/abstract was checked term-by-term against the two mandatory blocks (Section 4). Two studies (Arimah 2005; Chen & Martinez-Vazquez 2024) do not contain an explicit corruption term in their visible title/abstract — the Corruption block was widened with governance-quality proxy terms specifically to close this gap (Section 3), and supplementary non-database methods are recommended as a backstop (Section 6).
6. No publication-date limit is applied (Mauro 1998 is the oldest benchmark study and there is no reason to assume the literature is bounded more recently).

---

## 2. Concept groups identified from the benchmark set

| Concept | Role | Example terms | Benchmark studies that supply the term |
|---|---|---|---|
| **A. Corruption / illicit practices** | Mandatory block 1 | corrupt*, bribery, graft, embezzlement, misappropriation, kickbacks, collusion, cronyism/patronage | Hessami 2014; Mauro 1998; de la Croix & Delavallade 2008; Delavallade 2006; Kenny 2009 (both); Sedgo & Omgba 2022; Sombie 2023; Chen, Liu & Lee 2020; d'Agostino et al. 2016 |
| **A2. Governance-quality proxies** | Mandatory block 1 (recall-widening subset) | governance quality, institutional quality, corruption perception/index, political institutions | Added specifically for Arimah 2005 and Chen & Martinez-Vazquez 2024 — see Section 5 |
| **B. Public expenditure / investment / procurement** | Mandatory block 2 | public expenditure, government spending, public investment, budget/expenditure composition, public procurement, capital expenditure | Hessami 2014; Mauro 1998; de la Croix & Delavallade 2008; Delavallade 2006; Sedgo & Omgba 2022; Sombie 2023; d'Agostino et al. 2016 |
| **B2. Infrastructure sector & sub-sectors** | Mandatory block 2 | infrastructure, transport*, road*, highway*, public works, urban infrastructure | Kenny 2009 (both); Arimah 2005; Chen & Martinez-Vazquez 2024; Chen, Liu & Lee 2020 |
| **B3. Maintenance & quality outcomes** | Mandatory block 2 | infrastructure maintenance, maintenance expenditure/spending, infrastructure quality, asset management, O&M | Chen & Martinez-Vazquez 2024; Chen, Liu & Lee 2020; Kenny 2009 (Transport Reviews) |
| **B4. Distortion/allocation outcomes** | Mandatory block 2 | expenditure distortion, misallocation, expenditure/spending allocation or composition | Sedgo & Omgba 2022; Sombie 2023; Mauro 1998; Hessami 2014 |
| **C. Geography (developing countries)** | Optional / screening-stage only, NOT ANDed into the search | developing countr*, low-income, middle-income, emerging econom*, transition econom*, Sub-Saharan Africa, Global South | Used for eligibility screening; deliberately not required in the search string (would exclude Hessami 2014 and Chen, Liu & Lee 2020) |

B, B2, B3 and B4 are merged into a single OR-connected "Block 2" in the search strings below (not run as separate AND-mandatory sub-blocks), because several benchmark studies satisfy only *one* of these sub-facets (e.g. Arimah 2005 talks about infrastructure *spending* but not "quality"; Chen, Liu & Lee 2020 talks about infrastructure *quality* but not "maintenance expenditure"). Requiring more than one sub-facet at once would have caused false exclusions.

---

## 3. Full term list and rationale

### Block 1 — Corruption (Concepts A + A2)

| Term | Rationale |
|---|---|
| `corrupt*` | Core concept; truncation captures corruption, corrupt, corruptly, corruptive, corrupts. Present in 9/12 benchmark titles. |
| `brib*` | Common synonym/operationalisation of corruption (bribe, bribery, briber, bribing). |
| `graft` | US/African-English synonym for corruption, common in this literature (e.g., Sedgo & Omgba's African-focus journal). |
| `embezzl*` | Captures embezzlement of public funds, a specific corrupt-practice term used in public-finance corruption studies. |
| `misappropriat*` | Synonym for diversion of public funds, frequently used interchangeably with "corruption" in expenditure-composition papers. |
| `kickback*` | Specific procurement-corruption mechanism, directly relevant to Hessami 2014 (public procurement) and Kenny 2009 (infrastructure construction). |
| `"illicit payment*"` | Common World Bank/IMF phrasing for bribery in the public-investment literature. |
| `malfeasance` | Public-administration synonym for official corruption. |
| `fraud*` | Broad but standard co-occurring term in public-expenditure corruption literature; constrained by mandatory co-occurrence with Block 2. |
| `collus*` | Captures collusion/collusive bidding — central mechanism in procurement-corruption studies (Hessami 2014; Kenny, transport construction). |
| `"grand corruption"` / `"petty corruption"` | Standard typology terms used throughout the corruption-economics literature; increases recall for papers that use the typology instead of the bare word "corruption" only once. |
| `cronyism`, `nepotism`, `patronage`, `clientelis*`, `"pork barrel"` / `"pork-barrel"` | Political-economy synonyms for corrupt allocation of public resources; broaden recall to patronage-politics framed papers on expenditure allocation. |
| `"governance quality"`, `"institutional quality"`, `"quality of governance"`, `"governance indicator*"` | **Recall-widening terms.** Added because Arimah (2005) and Chen & Martinez-Vazquez (2024) frame corruption as one determinant within a broader "governance/institutional determinants of infrastructure spending" literature; their abstracts foreground governance/institutional-quality language rather than the bare word "corruption." |
| `"corruption perception*"`, `"corruption index*"` | Captures papers that operationalise corruption via the Corruption Perceptions Index / ICRG corruption index without necessarily repeating the word "corruption" elsewhere in the abstract. |
| `"political institution*"` | Added specifically because Chen & Martinez-Vazquez (2024) test "political institutions" as a determinant of infrastructure maintenance spending — a governance-adjacent channel through which corruption/accountability operates. |

**Deliberately excluded:** "principal-agent theory", "rent-seeking theory", "agency theory" — per instruction, since several benchmark papers (e.g., Delavallade 2006, Kenny 2009, Arimah 2005) are empirical and do not invoke a named theory. (Bare "rent-seeking" as a mechanism word was also left out of the mandatory string, since it is theory-flavoured; it is optional and can be added by the reviewer as an extra OR term if later needed — see Section 6.)

### Block 2 — Infrastructure / Public expenditure domain (Concepts B, B2, B3, B4)

| Term | Rationale |
|---|---|
| `infrastructur*` | Core sector term (infrastructure, infrastructural). Present in 6/12 benchmark titles/abstracts. |
| `"public investment*"` | Core term for de la Croix & Delavallade 2008. |
| `"public expenditure*"`, `"government expenditure*"` | Core terms for Mauro 1998, Sedgo & Omgba 2022, Sombie 2023. |
| `"government spending"`, `"public spending"` | Synonyms for expenditure, used by Delavallade 2006 and d'Agostino et al. 2016. |
| `"public procurement"` | Core term for Hessami 2014 and the procurement-corruption mechanism generally. |
| `"budget composition"`, `"expenditure composition"`, `"spending composition"` | Core outcome variable in Mauro 1998 and Hessami 2014 — corruption's effect on *how* budgets are composed, not just their size. |
| `"expenditure allocation"`, `"spending allocation"` | Synonyms for composition/distribution, matching Delavallade 2006 ("distribution of public spending"). |
| `"capital expenditure*"`, `"capital spending"` | Common budget-classification terms (capital vs. recurrent/maintenance spending), central to the maintenance-bias literature this review addresses. |
| `"public works"` | Traditional term for infrastructure construction/investment, common in older literature (relevant given Mauro 1998, no date limit). |
| `transport*` | Core term for Kenny 2009 (Transport Reviews) and Chen, Liu & Lee 2020. |
| `road*`, `highway*` | Sub-sector terms for transport infrastructure, the most commonly studied infrastructure type in this literature. |
| `"urban infrastructure"` | Matches Arimah 2005 (city-level infrastructure spending). |
| `"infrastructure spending"`, `"infrastructure investment"` | Direct phrase matches for several benchmark abstracts. |
| `"infrastructure quality"` | Direct outcome term from the research question and Chen, Liu & Lee 2020. |
| `"infrastructure maintenance"`, `"maintenance expenditure*"`, `"maintenance spending"`, `"operations and maintenance"` | Direct outcome term from the research question and core to Chen & Martinez-Vazquez 2024. |
| `"asset management"` | Practitioner/technical synonym for infrastructure maintenance planning. |
| `"capital bias"` | Named concept in the public-investment-vs-maintenance literature (governments' bias toward new construction over upkeep) — increases recall beyond the 12 benchmark papers for closely related literature. |
| `distort*`, `misallocat*` | Outcome terms matching Sedgo & Omgba 2022 ("distortion of public expenditures") and Sombie 2023 (distributional/allocation effects). |
| `"public asset*"` | Broadens recall to public-asset-management framed papers. |

---

## 4. Master Boolean logic (database-agnostic)

```
( Block 1: Corruption/governance-quality terms, OR-connected )
AND
( Block 2: Infrastructure/public-expenditure terms, OR-connected )
```

No date limit. No language limit is imposed at the search stage (recommend restricting to English at screening, and noting any non-English exclusions in the PRISMA flow diagram per PRISMA 2020 item 5).

---

## 5. Database-specific search strategies

### 5.1 Scopus

Field: `TITLE-ABS-KEY` (title, abstract, author keywords, indexed keywords). Truncation `*`. Optional proximity `W/n`.

```
TITLE-ABS-KEY(
  ( corrupt* OR brib* OR graft OR embezzl* OR misappropriat* OR kickback* OR "illicit payment*"
    OR malfeasance OR fraud* OR collus* OR "grand corruption" OR "petty corruption"
    OR cronyism OR nepotism OR patronage OR clientelis* OR "pork barrel" OR "pork-barrel"
    OR "governance quality" OR "institutional quality" OR "quality of governance"
    OR "governance indicator*" OR "corruption perception*" OR "corruption index*"
    OR "political institution*" )
  AND
  ( infrastructur* OR "public investment*" OR "public expenditure*" OR "government expenditure*"
    OR "government spending" OR "public spending" OR "public procurement" OR "budget composition"
    OR "expenditure composition" OR "spending composition" OR "expenditure allocation"
    OR "spending allocation" OR "capital expenditure*" OR "capital spending" OR "public works"
    OR transport* OR road* OR highway* OR "urban infrastructure" OR "infrastructure spending"
    OR "infrastructure investment" OR "infrastructure quality" OR "infrastructure maintenance"
    OR "maintenance expenditure*" OR "maintenance spending" OR "operations and maintenance"
    OR "asset management" OR "capital bias" OR distort* OR misallocat* OR "public asset*" )
)
```

*Optional precision-refinement variant (if the sensitive string above returns an unmanageable volume):* replace the `AND` with proximity, e.g. `(corrupt* W/15 infrastructur*) OR (corrupt* W/15 "public expenditure*") OR (corrupt* W/15 "public investment*") ...` — use only as a secondary, documented run, not a replacement, since proximity reduces sensitivity.

Filters: `LIMIT-TO(LANGUAGE,"English")` optional; `LIMIT-TO(DOCTYPE,"ar") OR LIMIT-TO(DOCTYPE,"re") OR LIMIT-TO(DOCTYPE,"cp")` if restricting to articles/reviews/conference papers.

### 5.2 Web of Science (Core Collection)

Field: `TS=` (Topic: title, abstract, author keywords, Keywords Plus). Truncation `*`. Proximity `NEAR/n`.

```
TS=(
  (corrupt* OR brib* OR graft OR embezzl* OR misappropriat* OR kickback* OR "illicit payment*"
   OR malfeasance OR fraud* OR collus* OR "grand corruption" OR "petty corruption"
   OR cronyism OR nepotism OR patronage OR clientelis* OR "pork barrel" OR "pork-barrel"
   OR "governance quality" OR "institutional quality" OR "quality of governance"
   OR "governance indicator*" OR "corruption perception*" OR "corruption index*"
   OR "political institution*")
  AND
  (infrastructur* OR "public investment*" OR "public expenditure*" OR "government expenditure*"
   OR "government spending" OR "public spending" OR "public procurement" OR "budget composition"
   OR "expenditure composition" OR "spending composition" OR "expenditure allocation"
   OR "spending allocation" OR "capital expenditure*" OR "capital spending" OR "public works"
   OR transport* OR road* OR highway* OR "urban infrastructure" OR "infrastructure spending"
   OR "infrastructure investment" OR "infrastructure quality" OR "infrastructure maintenance"
   OR "maintenance expenditure*" OR "maintenance spending" OR "operations and maintenance"
   OR "asset management" OR "capital bias" OR distort* OR misallocat* OR "public asset*")
)
```

Timespan: All years. Databases within WoS Core Collection: select SCI-EXPANDED, SSCI, ESCI at minimum (SSCI is essential — most benchmark studies are social-science/economics).

### 5.3 ProQuest (e.g., PAIS Index / International Bibliography of the Social Sciences / Social Science Premium Collection on the ProQuest platform)

Field: `ti,ab,su` (title, abstract, subject terms). Truncation `*`. Proximity `NEAR/n` (unordered), `PRE/n` (ordered).

```
ti,ab,su(corrupt* OR brib* OR graft OR embezzl* OR misappropriat* OR kickback* OR "illicit payment*"
  OR malfeasance OR fraud* OR collus* OR "grand corruption" OR "petty corruption"
  OR cronyism OR nepotism OR patronage OR clientelis* OR "pork barrel" OR "pork-barrel"
  OR "governance quality" OR "institutional quality" OR "quality of governance"
  OR "governance indicator*" OR "corruption perception*" OR "corruption index*"
  OR "political institution*")
AND
ti,ab,su(infrastructur* OR "public investment*" OR "public expenditure*" OR "government expenditure*"
  OR "government spending" OR "public spending" OR "public procurement" OR "budget composition"
  OR "expenditure composition" OR "spending composition" OR "expenditure allocation"
  OR "spending allocation" OR "capital expenditure*" OR "capital spending" OR "public works"
  OR transport* OR road* OR highway* OR "urban infrastructure" OR "infrastructure spending"
  OR "infrastructure investment" OR "infrastructure quality" OR "infrastructure maintenance"
  OR "maintenance expenditure*" OR "maintenance spending" OR "operations and maintenance"
  OR "asset management" OR "capital bias" OR distort* OR misallocat* OR "public asset*")
```

If initial results seem low, widen the field from `ti,ab,su` to `noft()` ("anywhere except full text") for maximum sensitivity, then re-tighten if volume is unmanageable. Apply a Document Type filter to Scholarly Journals (+ Working Papers/Reports if grey literature is in scope) rather than a subject filter, to avoid false exclusions.

### 5.4 EconLit (via EBSCOhost)

Field tags: `TI` (title), `AB` (abstract), `SU`/`DE` (subject/descriptor). Truncation `*`. Proximity `Nn` (unordered), `Wn` (ordered).

```
S1: TI ( corrupt* OR brib* OR graft OR embezzl* OR misappropriat* OR kickback* OR "illicit payment*"
     OR malfeasance OR fraud* OR collus* OR "grand corruption" OR "petty corruption"
     OR cronyism OR nepotism OR patronage OR clientelis* OR "pork barrel" OR "pork-barrel"
     OR "governance quality" OR "institutional quality" OR "quality of governance"
     OR "governance indicator*" OR "corruption perception*" OR "corruption index*"
     OR "political institution*" )
  OR AB ( same term list as above )

S2: TI ( infrastructur* OR "public investment*" OR "public expenditure*" OR "government expenditure*"
     OR "government spending" OR "public spending" OR "public procurement" OR "budget composition"
     OR "expenditure composition" OR "spending composition" OR "expenditure allocation"
     OR "spending allocation" OR "capital expenditure*" OR "capital spending" OR "public works"
     OR transport* OR road* OR highway* OR "urban infrastructure" OR "infrastructure spending"
     OR "infrastructure investment" OR "infrastructure quality" OR "infrastructure maintenance"
     OR "maintenance expenditure*" OR "maintenance spending" OR "operations and maintenance"
     OR "asset management" OR "capital bias" OR distort* OR misallocat* OR "public asset*" )
  OR AB ( same term list as above )

S3: S1 AND S2
```

EconLit's JEL classification codes can be used as a supplementary (not replacement) filter to sanity-check coverage: `H41` (Public Goods), `H54` (Infrastructure), `H57` (Procurement), `H83` (Public Administration/Corruption), `O18` (Regional/Urban/Infrastructure in developing economies), `D73` (Corruption/Bureaucracy). Do not apply these as mandatory AND filters — some benchmark papers may be mis-classified — use only to spot-check recall.

### 5.5 ABI/INFORM (ProQuest platform)

Same field logic and syntax as Section 5.3 (ProQuest), since ABI/INFORM runs on the ProQuest platform:

```
ti,ab,su(corrupt* OR brib* OR graft OR embezzl* OR misappropriat* OR kickback* OR "illicit payment*"
  OR malfeasance OR fraud* OR collus* OR "grand corruption" OR "petty corruption"
  OR cronyism OR nepotism OR patronage OR clientelis* OR "pork barrel" OR "pork-barrel"
  OR "governance quality" OR "institutional quality" OR "quality of governance"
  OR "governance indicator*" OR "corruption perception*" OR "corruption index*"
  OR "political institution*")
AND
ti,ab,su(infrastructur* OR "public investment*" OR "public expenditure*" OR "government expenditure*"
  OR "government spending" OR "public spending" OR "public procurement" OR "budget composition"
  OR "expenditure composition" OR "spending composition" OR "expenditure allocation"
  OR "spending allocation" OR "capital expenditure*" OR "capital spending" OR "public works"
  OR transport* OR road* OR highway* OR "urban infrastructure" OR "infrastructure spending"
  OR "infrastructure investment" OR "infrastructure quality" OR "infrastructure maintenance"
  OR "maintenance expenditure*" OR "maintenance spending" OR "operations and maintenance"
  OR "asset management" OR "capital bias" OR distort* OR misallocat* OR "public asset*")
```

ABI/INFORM indexes more practitioner/trade content than EconLit — expect higher recall of grey-literature-adjacent items (e.g., infrastructure asset-management trade press); screen accordingly rather than narrowing the string.

### 5.6 Bond Library Search (Primo/discovery-layer "OneSearch")

Discovery layers such as Bond's typically support Boolean `AND`/`OR`/`NOT` and wildcard `*`, but have weak or no support for phrase-proximity operators and search across a much larger, less-curated corpus (books, news, dissertations). Two complementary approaches:

**(a) Advanced Search, field-limited to Title + Abstract/Subject (not "Anywhere"):**
```
(corrupt* OR brib* OR graft OR embezzl* OR misappropriat* OR kickback* OR malfeasance OR fraud*
 OR collus* OR cronyism OR nepotism OR patronage OR clientelis*
 OR "governance quality" OR "institutional quality" OR "corruption perception" OR "corruption index"
 OR "political institution*")
AND
(infrastructur* OR "public investment" OR "public expenditure" OR "government expenditure"
 OR "government spending" OR "public spending" OR "public procurement" OR "budget composition"
 OR "capital expenditure" OR "public works" OR transport* OR road* OR highway*
 OR "urban infrastructure" OR "infrastructure spending" OR "infrastructure quality"
 OR "infrastructure maintenance" OR "maintenance expenditure" OR "maintenance spending"
 OR "asset management" OR distort* OR misallocat*)
```

**(b) Apply post-search facets** (not part of the query string, to avoid false exclusions at search time): Resource Type = Articles/Journal Articles (+ Reports/Working Papers if grey literature in scope); Peer Reviewed = Yes (optional, apply only at screening if used, since some working papers in the benchmark set, e.g. earlier versions of de la Croix & Delavallade, may not be peer-reviewed journal articles). Given Bond's index breadth, expect substantially higher irrelevant-result volume than the specialist databases above — this is expected and acceptable at the sensitive-search stage.

---

## 6. Cross-check: would each benchmark paper be retrieved?

| # | Benchmark study | Block 1 hit (term) | Block 2 hit (term) | Retrieved? | Notes |
|---|---|---|---|---|---|
| 1 | Hessami (2014) | `corrupt*` | `"public procurement"`, `"budget composition"` | ✅ Yes | Clean match on both blocks. |
| 2 | Mauro (1998) | `corrupt*` | `"government expenditure*"` | ✅ Yes | Clean match. |
| 3 | de la Croix & Delavallade (2008) | `corrupt*` | `"public investment*"` | ✅ Yes | Clean match. |
| 4 | Delavallade (2006) | `corrupt*` | `"public spending"` | ✅ Yes | Clean match. |
| 5 | Kenny (2009), *J. Development Studies* | `corrupt*` | `infrastructur*` | ✅ Yes | Clean match. |
| 6 | Sedgo & Omgba (2022) | `corrupt*` | `"public expenditure*"`, `distort*` | ✅ Yes | Double match on Block 2. |
| 7 | Sombie (2023) | `corrupt*` | `"public expenditure*"`, `misallocat*` | ✅ Yes | Confirmed via abstract (bias in allocation of public expenditure). |
| 8 | Arimah (2005) | ⚠️ No bare "corruption" term found in the retrievable abstract | `infrastructur*`, `"infrastructure spending"`, `"urban infrastructure"` | ⚠️ **At risk** | Abstract (verified via SAGE listing) discusses city-level determinants of infrastructure spending using UN-Habitat governance/urban indicators, but does not use the word "corruption" in the visible abstract. **Mitigation applied:** Block 1 widened with `"governance quality"`, `"institutional quality"`, `"governance indicator*"`, `"corruption perception*"`, `"corruption index*"` — plausible matches if these terms appear in the full abstract/keywords (UN-Habitat's urban indicators database includes governance/corruption-perception measures), but this cannot be guaranteed from title/abstract alone. **See supplementary methods below.** |
| 9 | Chen & Martinez-Vazquez (2024) | ⚠️ No bare "corruption" term found in the retrievable abstract | `"infrastructure maintenance"`, `infrastructur*` | ⚠️ **At risk** | Abstract centres on fiscal/political decentralization and finds "political institutions" are a significant determinant of maintenance spending. **Mitigation applied:** Block 1 widened with `"political institution*"` and `"institutional quality"`, which plausibly match if this phrase is used in the abstract/keywords, but confirmation was not possible without full-text/database access. **See supplementary methods below.** |
| 10 | Chen, Liu & Lee (2020) | `corrupt*` | `transport*`, `infrastructur*` | ✅ Yes | Clean match — corruption AND transportation infrastructure quality both in title. |
| 11 | Kenny (2009), *Transport Reviews* | `corrupt*` | `transport*` | ✅ Yes | Clean match. |
| 12 | d'Agostino, Dunne & Pieroni (2016) | `corrupt*` | `"government spending"` | ✅ Yes | Clean match. |

**Result: 10 of 12 benchmark papers are captured with high confidence by the Boolean string alone; 2 (Arimah 2005; Chen & Martinez-Vazquez 2024) are addressed by the widened governance-quality terms in Block 1 but cannot be verified as captured with certainty using title/abstract text alone**, because no full-text or indexed-keyword access was available during strategy design. This is a known limitation of any keyword-based string for papers that frame corruption as one determinant among several rather than as the primary focus — no further keyword widening was applied beyond Section 3, because broader single-word governance terms (e.g., bare "governance", "accountability", "transparency") would have caused a very large increase in false positives across all six databases without a proportionate gain in true recall for just two papers.

---

## 7. Supplementary methods (mandatory alongside the electronic search, per PRISMA-S)

To close the residual gap identified in Section 6, and consistent with PRISMA 2020 / PRISMA-S guidance that database searching alone rarely achieves 100% sensitivity:

1. **Backward citation chasing:** screen the reference lists of Arimah (2005) and Chen & Martinez-Vazquez (2024) — and of every other included study — for additional eligible papers.
2. **Forward citation chasing:** run "cited by" searches for Arimah (2005) and Chen & Martinez-Vazquez (2024) in Scopus/Web of Science/Google Scholar, since papers citing them for their governance/decentralization-infrastructure findings are likely to include corruption as a related determinant.
3. **Hand-searching:** manually check recent tables of contents of *Urban Studies*, *Public Finance and Management*, *Journal of Development Studies*, and *World Development* for the review period, since these are the core outlets for this literature.
4. **Grey literature / institutional search:** World Bank, IMF (Fiscal Affairs Dept.), OECD, and Transparency International publication repositories, using the same two-block logic, since corruption–infrastructure work is heavily produced by these institutions and may not be indexed identically to academic databases.
5. Document the yield of each supplementary method separately in the PRISMA flow diagram (PRISMA 2020 item 5).

---

## 8. Final PRISMA-ready search strategy table

| Source | Interface/Platform | Fields searched | Search string | Limits/filters | Search date | Records retrieved |
|---|---|---|---|---|---|---|
| Scopus | Scopus.com | Title, Abstract, Keywords (`TITLE-ABS-KEY`) | See Section 5.1 | None (all years, all languages) | *to be completed when run* | *to be completed* |
| Web of Science | Clarivate WoS Core Collection | Topic (`TS=`) across SCI-E, SSCI, ESCI | See Section 5.2 | None (all years) | *to be completed when run* | *to be completed* |
| ProQuest | ProQuest platform (PAIS/IBSS/Social Science Premium) | Title, Abstract, Subject (`ti,ab,su`) | See Section 5.3 | Document type: Scholarly Journals (+ Reports/Working Papers) | *to be completed when run* | *to be completed* |
| EconLit | EBSCOhost | Title, Abstract (`TI`, `AB`) | See Section 5.4 | None | *to be completed when run* | *to be completed* |
| ABI/INFORM | ProQuest platform | Title, Abstract, Subject (`ti,ab,su`) | See Section 5.5 | None | *to be completed when run* | *to be completed* |
| Bond Library Search | Primo ("OneSearch") | Title + Abstract/Subject (Advanced Search) | See Section 5.6 | Resource type facet applied post-search (Articles/Reports) | *to be completed when run* | *to be completed* |

**Supplementary methods:** backward/forward citation chasing on all included studies; hand-search of *Urban Studies*, *Public Finance and Management*, *Journal of Development Studies*, *World Development*; grey-literature search of World Bank, IMF, OECD, Transparency International repositories (Section 7).

**Deduplication:** merge exports across all six sources (e.g., in EndNote/Zotero/Rayyan) before title/abstract screening.

**Screening-stage eligibility criteria (applied after retrieval, not baked into the search string):** geographic scope (developing/transition economies — Concept C, Section 1), empirical or theoretical focus on the corruption→infrastructure-spending/quality relationship, English language (if elected), peer-reviewed or grey-literature-eligible per protocol.
