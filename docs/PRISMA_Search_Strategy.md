# PRISMA-Compliant Search Strategy

**Research question:** How does corruption influence infrastructure maintenance spending and infrastructure quality in developing countries?

**Status:** Draft search strategy (v2 — tightened for precision), cross-checked against a 12-study benchmark set. Ready for information-specialist peer review (PRESS checklist) before execution.

**v2 change note:** v1 of this strategy returned unmanageable volume (~22,000 records in initial testing). The root causes, and the fixes applied in this version, are documented in Section 0.

---

## 0. Why v1 was too broad, and what changed

Diagnosis of the volume problem:

1. **Word-sense collision on `corrupt*`.** The truncation `corrupt*` also matches "data corruption", "file corruption", "memory corruption", "signal corruption" — extremely common phrases in computer science, IT and electronic-engineering literature that have nothing to do with political/financial corruption. Combined with `infrastructur*` (equally common in IT literature as "network infrastructure", "cloud infrastructure", "IT infrastructure"), this pairing alone likely produced a large share of the false-positive volume. **Fix:** add an explicit exclusion clause for the data/file/IT sense of "corrupt", and add subject-area filter guidance (Section 5).
2. **Terms not tied to any benchmark paper.** `fraud*`, `cronyism`, `nepotism`, `patronage`, `clientelis*`, `"pork barrel"`, `"public works"`, `"public asset*"`, `"capital bias"` were included in v1 as generic recall-boosters but are not required to retrieve any of the 12 benchmark studies, and several are individually very high-volume, high-noise terms (e.g. `fraud*` alone spans accounting fraud, tax fraud, insurance fraud, academic fraud). **Fix:** removed from the core string (Section 3).
3. **Redundant broad terms.** `distort*` and `misallocat*` were added for Sedgo & Omgba (2022) and Sombie (2023), but both papers' titles/abstracts also contain `"public expenditure*"`, which already retrieves them — so `distort*`/`misallocat*` (both very broad standalone economics words: market distortion, price distortion, trade distortion, resource misallocation) added volume without adding unique recall. **Fix:** removed.
4. **Term-sense collision on "asset management".** Bare `"asset management"` overwhelmingly means *financial* asset/fund/wealth management in the literature, not infrastructure asset management. **Fix:** narrowed to `"infrastructure asset management"` / `"public asset management"`.
5. **Plain Boolean `AND` across two very large `OR` sets** does not require the two concepts to be topically connected within the abstract — a paper that mentions corruption in one sentence and government spending on an unrelated topic in another sentence still matches. **Fix:** proximity operators (`W/15` / `NEAR/15` / `N15`, i.e. within 15 words) are now the **primary** logic wherever the database supports it, with plain `AND` offered only as a documented fallback if a proximity run under-retrieves.
6. **The governance-quality widening terms** (`"institutional quality"`, `"governance quality"`, `"political institution*"`) were merged directly into the main string in v1. These are mainstream terms in the (very large) institutions-and-growth economics literature, and pairing them with broad terms like `"government spending"` would itself have contributed materially to the 22,000-record volume. **Fix:** moved out of the core string into a small, separately run **supplementary search** (Section 4), targeted only at infrastructure-specific terms, and used only to chase the two benchmark papers that need it.

All changes were re-checked against the 12 benchmark studies (Section 6) to confirm no recall was lost.

---

## 1. Method used to build this strategy

1. Titles, abstracts, and (where retrievable) keywords of all 12 benchmark studies were read and coded into concepts.
2. Concepts were grouped into two **mandatory** blocks (Corruption; Infrastructure/Public-Expenditure Domain), combined with proximity (primary) or `AND` (fallback). Each block is internally an `OR` set restricted to terms that are either directly tied to a benchmark paper or a close, low-noise synonym.
3. A third concept — **geography (developing countries)** — is deliberately **excluded from the mandatory search logic**. Two benchmark papers (Hessami 2014 = OECD countries; Chen, Liu & Lee 2020 = US states) are not about developing countries at all, so requiring geographic terms in the search string would exclude them. Geography is instead applied as a **title/abstract screening criterion**.
4. No theory-of-mechanism terms (e.g., "principal-agent", "rent-seeking theory") were required, per instruction.
5. Each benchmark study's title/abstract was checked term-by-term against the core blocks (Section 6). Two studies (Arimah 2005; Chen & Martinez-Vazquez 2024) do not contain an explicit corruption term in their visible title/abstract; these are handled by a small **Supplementary Search 2** (Section 4) plus citation chasing (Section 7), rather than by inflating the main string.
6. No publication-date limit is applied (Mauro 1998 is the oldest benchmark study).

---

## 2. Concept groups (v2)

| Concept | Role | Benchmark studies that require the term |
|---|---|---|
| **A. Corruption / illicit practices** (core) | Mandatory, Search 1 | Hessami 2014; Mauro 1998; de la Croix & Delavallade 2008; Delavallade 2006; Kenny 2009 (both); Sedgo & Omgba 2022; Sombie 2023; Chen, Liu & Lee 2020; d'Agostino et al. 2016 |
| **B. Infrastructure / public expenditure domain** (core) | Mandatory, Search 1 | All 12 (see Section 6) |
| **A2. Governance-quality proxies** | Small supplementary block, Search 2 only — not merged into Search 1 | Arimah 2005; Chen & Martinez-Vazquez 2024 |
| **C. Geography (developing countries)** | Screening-stage only, not searched | Applied to all records after retrieval |

---

## 3. Search 1 (primary, sensitive search) — full term list and rationale

### Block 1 — Corruption (core only)

| Term | Rationale |
|---|---|
| `corrupt*` | Core concept. Present in 9/12 benchmark titles. **Must be paired with the data-corruption exclusion clause below** — see Section 5. |
| `brib*` | bribe, bribery, briber, bribing. |
| `graft` | Common synonym in this literature. |
| `embezzl*` | Diversion of public funds — specific corrupt-practice term. |
| `misappropriat*` | Diversion of public funds, used interchangeably with "corruption" in expenditure-composition papers. |
| `kickback*` | Procurement-corruption mechanism (Hessami 2014; Kenny, infrastructure construction). |
| `"illicit payment*"` | Standard World Bank/IMF phrasing for bribery in the public-investment literature. |
| `malfeasance` | Public-administration synonym for official corruption. |
| `collus*` | Collusion/collusive bidding — central mechanism in procurement-corruption studies. |
| `"grand corruption"` / `"petty corruption"` | Standard typology terms; low-noise phrases (unlike bare `fraud*`, they are specific to the corruption literature). |

**Removed from v1 (not needed for any benchmark; high noise):** `fraud*`, `cronyism`, `nepotism`, `patronage`, `clientelis*`, `"pork barrel"`/`"pork-barrel"`.

**Deliberately excluded throughout:** "principal-agent theory", "rent-seeking theory", "agency theory" — per instruction.

### Block 2 — Infrastructure / public expenditure domain (core only)

| Term | Rationale |
|---|---|
| `infrastructur*` | Core sector term. **Must be paired with the data/IT-infrastructure exclusion clause** — see Section 5. |
| `"public investment*"` | Core term for de la Croix & Delavallade 2008. |
| `"public expenditure*"`, `"government expenditure*"` | Core terms for Mauro 1998, Sedgo & Omgba 2022, Sombie 2023 — these two phrases alone are sufficient to retrieve both papers, making standalone `distort*`/`misallocat*` unnecessary. |
| `"government spending"`, `"public spending"` | Used by Delavallade 2006 and d'Agostino et al. 2016. |
| `"public procurement"` | Core term for Hessami 2014. |
| `"budget composition"`, `"expenditure composition"`, `"spending composition"` | Core outcome variable in Mauro 1998 and Hessami 2014. |
| `"expenditure allocation"`, `"spending allocation"` | Matches Delavallade 2006 ("distribution of public spending"). |
| `"capital expenditure*"`, `"capital spending"` | Capital vs. recurrent/maintenance spending — central to the maintenance-bias theme of the review. |
| `transport*` | Core term for Kenny 2009 (Transport Reviews) and Chen, Liu & Lee 2020. |
| `road*`, `highway*` | Sub-sector terms tied directly to the two transport-infrastructure benchmark papers. |
| `"urban infrastructure"` | Matches Arimah 2005. |
| `"infrastructure spending"`, `"infrastructure investment"` | Direct phrase matches. |
| `"infrastructure quality"` | Direct outcome term from the RQ and Chen, Liu & Lee 2020. |
| `"infrastructure maintenance"`, `"maintenance expenditure*"`, `"maintenance spending"`, `"operations and maintenance"` | Direct outcome term from the RQ and core to Chen & Martinez-Vazquez 2024. |
| `"infrastructure asset management"`, `"public asset management"` | Narrowed from bare "asset management" (v1) to avoid collision with financial/fund asset-management literature. |

**Removed from v1 (not needed for any benchmark, and/or high noise):** `"public works"`, `"public asset*"`, `"capital bias"`, `distort*`, `misallocat*` (redundant with `"public expenditure*"` for the two papers they were added for), bare `"asset management"`.

---

## 4. Search 2 (small supplementary search — governance-quality framing)

Run **separately** from Search 1, with its own, narrower term set, specifically to chase Arimah (2005) and Chen & Martinez-Vazquez (2024)-type papers that discuss corruption via governance/institutional-quality language rather than the word "corruption" itself. Keeping this search separate and narrow (infrastructure-specific Block 2, not the generic public-expenditure terms) is what keeps its volume small — pairing these governance terms with `"government spending"` instead would itself be a very high-volume combination (institutions-and-growth is a huge economics literature).

```
( "governance quality" OR "institutional quality" OR "quality of governance"
  OR "governance indicator*" OR "corruption perception*" OR "corruption index*"
  OR "political institution*" )
AND
( infrastructur* OR "urban infrastructure" OR "infrastructure maintenance"
  OR "infrastructure spending" OR "infrastructure quality" OR "infrastructure investment" )
```

Apply the same data/IT-infrastructure exclusion clause (Section 5) to the `infrastructur*` term here as well. Screen Search 2 results as a distinct, smaller batch — expect a materially smaller yield than Search 1.

---

## 5. Handling the `corrupt*` / `infrastructur*` word-sense collision

Both core terms have a common non-relevant sense in computer science/IT literature ("data corruption", "file corruption", "memory corruption"; "network/cloud/IT infrastructure"). Two complementary mitigations, to be applied together:

**(a) Exclusion clause** (add to every database string in Section 6, adjusted to that platform's `NOT`/`AND NOT` syntax):
```
AND NOT ( "data corrupt*" OR "file corrupt*" OR "memory corrupt*" OR "disk corrupt*"
          OR "signal corrupt*" OR "image corrupt*" OR "software corrupt*"
          OR "database corrupt*" OR "network infrastructure" OR "cloud infrastructure"
          OR "IT infrastructure" OR "computing infrastructure" )
```
This is a targeted, low-risk exclusion — it removes only records dominated by the IT sense of these words, not records that happen to also mention IT topics in passing.

**(b) Subject-area / database filter** (apply as a facet after running the query, not baked into the Boolean string, so it can be checked against the benchmark set before being finalised):
- **Scopus:** Limit to Subject Areas Economics/Econometrics/Finance; Business/Management/Accounting; Social Sciences; Environmental Science (captures Urban Studies-type journals). Exclude Computer Science. **Verify Kenny (2009, Transport Reviews) is not lost** before excluding Engineering broadly — Transport Reviews is sometimes cross-listed under Engineering as well as Social Sciences, so do not exclude Engineering outright; exclude Computer Science only.
- **Web of Science:** Limit to Web of Science Categories in Economics, Business, Public Administration, Urban Studies, Political Science, Transportation (do not exclude Transportation); exclude Computer Science categories.
- **ProQuest / ABI/INFORM:** Apply a Subject facet excluding "Computers and Information Technology" post-search rather than pre-search, and verify no benchmark-adjacent records are lost.
- **EconLit:** Low risk — EconLit's corpus is economics-only, so the IT word-sense collision barely applies here; the exclusion clause is optional for this database.
- **Bond Library Search:** Given the very broad, multi-disciplinary corpus of a discovery layer, this filter matters most here — apply a Subject/Discipline facet limiting to Business/Economics, Social Sciences, Political Science, Public Administration after running the search.

---

## 6. Database-specific search strategies

### 6.1 Scopus

Field: `TITLE-ABS-KEY`. Truncation `*`. Proximity `W/n` (primary logic).

```
TITLE-ABS-KEY(
  ( corrupt*  W/15  ( infrastructur* OR "public investment*" OR "public expenditure*"
      OR "government expenditure*" OR "government spending" OR "public spending"
      OR "public procurement" OR "budget composition" OR "expenditure composition"
      OR "spending composition" OR "expenditure allocation" OR "spending allocation"
      OR "capital expenditure*" OR "capital spending" OR transport* OR road* OR highway*
      OR "urban infrastructure" OR "infrastructure spending" OR "infrastructure investment"
      OR "infrastructure quality" OR "infrastructure maintenance" OR "maintenance expenditure*"
      OR "maintenance spending" OR "operations and maintenance"
      OR "infrastructure asset management" OR "public asset management" ) )
  OR
  ( brib* OR graft OR embezzl* OR misappropriat* OR kickback* OR "illicit payment*"
    OR malfeasance OR collus* OR "grand corruption" OR "petty corruption" )
    AND
  ( infrastructur* OR "public investment*" OR "public expenditure*" OR "government expenditure*"
    OR "government spending" OR "public spending" OR "public procurement" OR "budget composition"
    OR "expenditure composition" OR "spending composition" OR "expenditure allocation"
    OR "spending allocation" OR "capital expenditure*" OR "capital spending" OR transport*
    OR road* OR highway* OR "urban infrastructure" OR "infrastructure spending"
    OR "infrastructure investment" OR "infrastructure quality" OR "infrastructure maintenance"
    OR "maintenance expenditure*" OR "maintenance spending" OR "operations and maintenance"
    OR "infrastructure asset management" OR "public asset management" )
)
AND NOT ( "data corrupt*" OR "file corrupt*" OR "memory corrupt*" OR "disk corrupt*"
          OR "signal corrupt*" OR "image corrupt*" OR "software corrupt*"
          OR "database corrupt*" OR "network infrastructure" OR "cloud infrastructure"
          OR "IT infrastructure" OR "computing infrastructure" )
```

*Why two sub-clauses:* Scopus's `W/n` proximity operator only connects two single terms/phrases, not two full parenthesised `OR` lists, in a single expression the way plain `AND` does — so `corrupt* W/15 (...)` must be checked/expanded term-by-term in Scopus's actual query builder (Scopus does support `term W/n (A OR B OR C)`, but always pilot-test this exact syntax against the benchmark set in Scopus directly before running at scale, since operator support can shift). The second sub-clause (non-`corrupt*` corruption terms combined with plain `AND`, since these terms carry far less noise on their own) is retained as plain `AND` because kickback*, embezzl*, collus*, etc. do not have the IT-homonym problem, so proximity is not required for precision on that half.

Optional filters: `LIMIT-TO(SUBJAREA,"ECON") OR LIMIT-TO(SUBJAREA,"BUSI") OR LIMIT-TO(SUBJAREA,"SOCI") OR LIMIT-TO(SUBJAREA,"ENVI")`; `EXCLUDE(SUBJAREA,"COMP")`. Pilot-test filters against the benchmark set before finalising (see Section 5b caution on Transport Reviews).

*Fallback (if proximity syntax under-retrieves in testing):* revert Block 1/Block 2 to plain `AND` (full term lists as in Section 3) plus the `AND NOT` exclusion clause — still materially smaller than v1 because of the term removals in Section 3.

### 6.2 Web of Science (Core Collection)

Field: `TS=`. Truncation `*`. Proximity `NEAR/n`.

```
TS=(
  (corrupt* NEAR/15 (infrastructur* OR "public investment*" OR "public expenditure*"
     OR "government expenditure*" OR "government spending" OR "public spending"
     OR "public procurement" OR "budget composition" OR "expenditure composition"
     OR "spending composition" OR "expenditure allocation" OR "spending allocation"
     OR "capital expenditure*" OR "capital spending" OR transport* OR road* OR highway*
     OR "urban infrastructure" OR "infrastructure spending" OR "infrastructure investment"
     OR "infrastructure quality" OR "infrastructure maintenance" OR "maintenance expenditure*"
     OR "maintenance spending" OR "operations and maintenance"
     OR "infrastructure asset management" OR "public asset management"))
  OR
  ((brib* OR graft OR embezzl* OR misappropriat* OR kickback* OR "illicit payment*"
    OR malfeasance OR collus* OR "grand corruption" OR "petty corruption")
   AND
   (infrastructur* OR "public investment*" OR "public expenditure*" OR "government expenditure*"
    OR "government spending" OR "public spending" OR "public procurement" OR "budget composition"
    OR "expenditure composition" OR "spending composition" OR "expenditure allocation"
    OR "spending allocation" OR "capital expenditure*" OR "capital spending" OR transport*
    OR road* OR highway* OR "urban infrastructure" OR "infrastructure spending"
    OR "infrastructure investment" OR "infrastructure quality" OR "infrastructure maintenance"
    OR "maintenance expenditure*" OR "maintenance spending" OR "operations and maintenance"
    OR "infrastructure asset management" OR "public asset management"))
)
NOT TS=("data corrupt*" OR "file corrupt*" OR "memory corrupt*" OR "disk corrupt*"
        OR "signal corrupt*" OR "image corrupt*" OR "software corrupt*"
        OR "database corrupt*" OR "network infrastructure" OR "cloud infrastructure"
        OR "IT infrastructure" OR "computing infrastructure")
```

Timespan: All years. Databases: SCI-EXPANDED, SSCI, ESCI. Optional Web of Science Category filters as noted in Section 5b — pilot-test before excluding any category.

### 6.3 ProQuest (e.g., PAIS Index / IBSS / Social Science Premium Collection)

Field: `ti,ab,su`. Truncation `*`. Proximity `NEAR/n` (unordered).

```
( ti,ab,su(corrupt*) NEAR/15 ti,ab,su(infrastructur* OR "public investment*" OR "public expenditure*"
    OR "government expenditure*" OR "government spending" OR "public spending"
    OR "public procurement" OR "budget composition" OR "expenditure composition"
    OR "spending composition" OR "expenditure allocation" OR "spending allocation"
    OR "capital expenditure*" OR "capital spending" OR transport* OR road* OR highway*
    OR "urban infrastructure" OR "infrastructure spending" OR "infrastructure investment"
    OR "infrastructure quality" OR "infrastructure maintenance" OR "maintenance expenditure*"
    OR "maintenance spending" OR "operations and maintenance"
    OR "infrastructure asset management" OR "public asset management") )
OR
( ti,ab,su(brib* OR graft OR embezzl* OR misappropriat* OR kickback* OR "illicit payment*"
    OR malfeasance OR collus* OR "grand corruption" OR "petty corruption")
  AND
  ti,ab,su(infrastructur* OR "public investment*" OR "public expenditure*" OR "government expenditure*"
    OR "government spending" OR "public spending" OR "public procurement" OR "budget composition"
    OR "expenditure composition" OR "spending composition" OR "expenditure allocation"
    OR "spending allocation" OR "capital expenditure*" OR "capital spending" OR transport*
    OR road* OR highway* OR "urban infrastructure" OR "infrastructure spending"
    OR "infrastructure investment" OR "infrastructure quality" OR "infrastructure maintenance"
    OR "maintenance expenditure*" OR "maintenance spending" OR "operations and maintenance"
    OR "infrastructure asset management" OR "public asset management") )
NOT ti,ab,su("data corrupt*" OR "file corrupt*" OR "memory corrupt*" OR "disk corrupt*"
    OR "signal corrupt*" OR "image corrupt*" OR "software corrupt*" OR "database corrupt*"
    OR "network infrastructure" OR "cloud infrastructure" OR "IT infrastructure"
    OR "computing infrastructure")
```

Apply a Document Type filter (Scholarly Journals + Working Papers/Reports) rather than a subject filter, to avoid false exclusions. Confirm `NEAR/n` can span across the two separate `ti,ab,su()` field clauses in your ProQuest instance during pilot testing; if not, restructure as a single `ti,ab,su(termA NEAR/15 termB)` per term-pair, or fall back to plain `AND`.

### 6.4 EconLit (via EBSCOhost)

Field tags: `TI`, `AB`, `SU`/`DE`. Truncation `*`. Proximity `Nn` (unordered).

```
S1: TI ( corrupt* ) N15 TI ( infrastructur* OR "public investment*" OR "public expenditure*"
      OR "government expenditure*" OR "government spending" OR "public spending"
      OR "public procurement" OR "budget composition" OR "expenditure composition"
      OR "spending composition" OR "expenditure allocation" OR "spending allocation"
      OR "capital expenditure*" OR "capital spending" OR transport* OR road* OR highway*
      OR "urban infrastructure" OR "infrastructure spending" OR "infrastructure investment"
      OR "infrastructure quality" OR "infrastructure maintenance" OR "maintenance expenditure*"
      OR "maintenance spending" OR "operations and maintenance"
      OR "infrastructure asset management" OR "public asset management" )
    OR
    AB ( corrupt* ) N15 AB ( same Block-2 list as above )

S2: TI ( brib* OR graft OR embezzl* OR misappropriat* OR kickback* OR "illicit payment*"
      OR malfeasance OR collus* OR "grand corruption" OR "petty corruption" )
    OR AB ( same term list )

S3: TI ( same Block-2 list as in S1 ) OR AB ( same Block-2 list )

S4: S1 OR (S2 AND S3)
```

EconLit's corpus is economics-only, so the data-corruption exclusion clause is optional here (low risk) — apply only if pilot testing shows otherwise. JEL codes `H41`, `H54`, `H57`, `H83`, `O18`, `D73` can be used to spot-check recall, not as mandatory filters.

### 6.5 ABI/INFORM (ProQuest platform)

Same field logic and syntax as Section 6.3, since ABI/INFORM runs on the ProQuest platform. Apply the same `NEAR/15` structure and the `NOT` exclusion clause. Because ABI/INFORM indexes more trade/practitioner and IT-business content than EconLit, the exclusion clause and a "Computers and Information Technology" subject-facet exclusion (applied post-search, then verified against the benchmark set) are both recommended here, not optional.

### 6.6 Bond Library Search (Primo/discovery-layer "OneSearch")

Discovery layers typically support Boolean `AND`/`OR`/`NOT` and wildcard `*`, but weak or no phrase-proximity support, and search a much larger, less-curated corpus (books, news, dissertations, IT trade content) — this is the database most exposed to the word-sense collision in Section 5, so filters matter most here.

**(a) Advanced Search, field-limited to Title + Abstract/Subject (not "Anywhere"):**
```
(corrupt* OR brib* OR graft OR embezzl* OR misappropriat* OR kickback* OR malfeasance
 OR collus*)
AND
(infrastructur* OR "public investment" OR "public expenditure" OR "government expenditure"
 OR "government spending" OR "public spending" OR "public procurement" OR "budget composition"
 OR "capital expenditure" OR transport* OR road* OR highway* OR "urban infrastructure"
 OR "infrastructure spending" OR "infrastructure quality" OR "infrastructure maintenance"
 OR "maintenance expenditure" OR "maintenance spending" OR "infrastructure asset management")
NOT
("data corruption" OR "file corruption" OR "memory corruption" OR "network infrastructure"
 OR "cloud infrastructure" OR "IT infrastructure")
```

**(b) Apply post-search facets** (not part of the query string): Resource Type = Articles/Journal Articles (+ Reports/Working Papers if grey literature is in scope); Discipline/Subject facet limited to Business/Economics, Social Sciences, Political Science, Public Administration (exclude Computer Science/IT). Verify the facet does not drop any benchmark-adjacent journals before finalising.

### 6.7 Supplementary Search 2 (all databases)

Run the Section 4 query (governance-quality terms AND infrastructure-specific terms, with the same data/IT exclusion clause) separately in each of the six sources above, using the same field codes as that database's main string. Tag results from this search distinctly at the screening stage so its yield and precision can be reported separately in the PRISMA flow diagram.

---

## 7. Cross-check: would each benchmark paper be retrieved by Search 1 + Search 2?

| # | Benchmark study | Corruption-block hit | Infrastructure-block hit | Retrieved? | Notes |
|---|---|---|---|---|---|
| 1 | Hessami (2014) | `corrupt*` | `"public procurement"`, `"budget composition"` | ✅ Yes | Both terms co-occur closely in the title — well within 15 words. |
| 2 | Mauro (1998) | `corrupt*` | `"government expenditure*"` | ✅ Yes | Same title, adjacent phrase. |
| 3 | de la Croix & Delavallade (2008) | `corrupt*` | `"public investment*"` | ✅ Yes | Same title. |
| 4 | Delavallade (2006) | `corrupt*` | `"public spending"` | ✅ Yes | Same title. |
| 5 | Kenny (2009), *J. Development Studies* | `corrupt*` | `infrastructur*` | ✅ Yes | Same title ("corruption in infrastructure"). |
| 6 | Sedgo & Omgba (2022) | `corrupt*` | `"public expenditure*"` | ✅ Yes | Same title; `distort*` no longer needed for recall. |
| 7 | Sombie (2023) | `corrupt*` | `"public expenditure*"` | ✅ Yes | Confirmed via abstract ("...corruption on public expenditures..."/"...allocation of public expenditure"). |
| 8 | Arimah (2005) | ⚠️ No bare "corruption" term in the visible abstract | `infrastructur*`, `"urban infrastructure"`, `"infrastructure spending"` | ⚠️ Handled by **Search 2** + citation chasing (Section 8) | Abstract discusses city-level determinants of infrastructure spending using governance/urban indicators; corruption is plausibly one determinant tested, but not confirmable from title/abstract alone. |
| 9 | Chen & Martinez-Vazquez (2024) | ⚠️ No bare "corruption" term in the visible abstract | `"infrastructure maintenance"`, `infrastructur*` | ⚠️ Handled by **Search 2** + citation chasing (Section 8) | Abstract centres on fiscal/political decentralization; "political institutions" found significant for maintenance spending — matches Search 2's governance-quality block. |
| 10 | Chen, Liu & Lee (2020) | `corrupt*` | `transport*`, `infrastructur*` | ✅ Yes | Same title. |
| 11 | Kenny (2009), *Transport Reviews* | `corrupt*` | `transport*` | ✅ Yes | Same title. |
| 12 | d'Agostino, Dunne & Pieroni (2016) | `corrupt*` | `"government spending"` | ✅ Yes | Same title. |

**Result: 10 of 12 benchmark papers are captured by Search 1 alone, with the corruption and infrastructure terms co-occurring within the title itself (well inside a 15-word proximity window), so the switch to proximity logic does not cost any recall on this set.** The 2 remaining papers (Arimah 2005; Chen & Martinez-Vazquez 2024) are targeted by the small Search 2 plus the supplementary methods in Section 8 — this was not resolved by further widening Search 1, because doing so (e.g. adding bare "governance" or "institutional quality" to the main string) was the specific change that drove volume up in v1.

---

## 8. Supplementary methods (mandatory alongside the electronic search, per PRISMA-S)

1. **Backward citation chasing:** screen the reference lists of Arimah (2005) and Chen & Martinez-Vazquez (2024) — and of every other included study — for additional eligible papers.
2. **Forward citation chasing:** run "cited by" searches for Arimah (2005) and Chen & Martinez-Vazquez (2024) in Scopus/Web of Science/Google Scholar.
3. **Hand-searching:** manually check recent tables of contents of *Urban Studies*, *Public Finance and Management*, *Journal of Development Studies*, and *World Development*.
4. **Grey literature / institutional search:** World Bank, IMF (Fiscal Affairs Dept.), OECD, and Transparency International publication repositories, using the Section 3/4 term logic.
5. Document the yield of each supplementary method separately in the PRISMA flow diagram (PRISMA 2020 item 5).

---

## 9. Final PRISMA-ready search strategy table

| Source | Interface/Platform | Fields searched | Primary logic | Search string | Filters | Search date | Records (Search 1) | Records (Search 2) |
|---|---|---|---|---|---|---|---|---|
| Scopus | Scopus.com | `TITLE-ABS-KEY` | Proximity `W/15` (fallback: `AND`) | Section 6.1 | Optional subject-area facet, pilot-tested | *to be completed* | *to be completed* | *to be completed* |
| Web of Science | WoS Core Collection | `TS=` | Proximity `NEAR/15` (fallback: `AND`) | Section 6.2 | SCI-E, SSCI, ESCI; optional category facet | *to be completed* | *to be completed* | *to be completed* |
| ProQuest | PAIS/IBSS/Social Science Premium | `ti,ab,su` | Proximity `NEAR/15` (fallback: `AND`) | Section 6.3 | Document type: Scholarly Journals (+ Reports) | *to be completed* | *to be completed* | *to be completed* |
| EconLit | EBSCOhost | `TI`, `AB` | Proximity `N15` (fallback: `AND`) | Section 6.4 | None required | *to be completed* | *to be completed* | *to be completed* |
| ABI/INFORM | ProQuest platform | `ti,ab,su` | Proximity `NEAR/15` (fallback: `AND`) | Section 6.5 | Subject facet excluding Computers/IT | *to be completed* | *to be completed* | *to be completed* |
| Bond Library Search | Primo ("OneSearch") | Title + Abstract/Subject | Plain `AND`/`NOT` | Section 6.6 | Resource type + discipline facet (exclude CS/IT) | *to be completed* | *to be completed* | *to be completed* |

**Deduplication:** merge exports across all six sources and both searches (e.g., in EndNote/Zotero/Rayyan) before title/abstract screening.

**Screening-stage eligibility criteria (applied after retrieval, not baked into the search string):** geographic scope (developing/transition economies), empirical or theoretical focus on the corruption→infrastructure-spending/quality relationship, English language (if elected), peer-reviewed or grey-literature-eligible per protocol.

**Recommended pilot step before full execution:** run Section 6.1–6.6 in each database and confirm all 10 "clean" benchmark papers (Section 7) are returned, then check total record count is in a screenable range; if any database still returns an unexpectedly large volume, tighten further by (a) narrowing `transport*`/`road*`/`highway*` to `"transport infrastructure"`/`"road infrastructure"` if those single words are the driver, or (b) applying the subject/discipline facets in Section 5b as mandatory rather than optional.
