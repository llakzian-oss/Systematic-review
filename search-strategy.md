# Search Strategy

**Project:** The Impact of Political Corruption on Infrastructure Maintenance Spending in Developing Countries
**Type:** Systematic Review

## 1. Concept framework

The search string is built from three concept blocks, combined with `AND`. Terms
within each block are combined with `OR`. This follows a PICO-style breakdown
adapted for a non-clinical (economics / public administration / political
science) topic:

| Block | Concept | Role |
|---|---|---|
| 1 | Political corruption | Exposure / independent variable |
| 2 | Infrastructure maintenance spending | Outcome / dependent variable |
| 3 | Developing countries | Population / context |

## 2. Term list per concept

**Block 1 — Political corruption**
`"political corruption"`, `corrupt*`, `bribery`, `bribe*`, `embezzl*`, `graft`,
`"rent-seeking"`, `"rent seeking"`, `clientelis*`, `patronage`, `"state capture"`,
`"political capture"`, `kleptocracy`, `cronyism`, `"illicit enrichment"`,
`misappropriat*`, `"public integrity"` (as a near-antonym control term if needed)

**Block 2 — Infrastructure maintenance spending**
`"infrastructure maintenance"`, `"infrastructure spending"`,
`"infrastructure expenditure"`, `"infrastructure investment"`,
`"public infrastructure"`, `"capital expenditure"`, `"capital spending"`,
`"maintenance expenditure"`, `"maintenance spending"`, `"asset maintenance"`,
`"public works"`, `"infrastructure budget*"`, `"infrastructure financing"`,
`"infrastructure fund*"`, `"road maintenance"`, `"public capital stock"`

**Block 3 — Developing countries**
`"developing countr*"`, `"developing nation*"`,
`"low- and middle-income countr*"`, `"low and middle income countr*"`,
`LMIC`, `LMICs`, `"emerging econom*"`, `"emerging market*"`,
`"less developed countr*"`, `"low-income countr*"`, `"middle-income countr*"`,
`"third world"`, `"global south"`, `"transition econom*"`

> Consider adding specific region/country names (e.g., named LMICs, or a
> World Bank income-group list) as a supplementary filter if a database's
> subject/thesaurus terms don't capture "developing countries" well.

## 3. Master Boolean string (generic)

```
("political corruption" OR corrupt* OR bribery OR bribe* OR embezzl* OR graft
  OR "rent-seeking" OR "rent seeking" OR clientelis* OR patronage
  OR "state capture" OR "political capture" OR kleptocracy OR cronyism
  OR "illicit enrichment" OR misappropriat*)
AND
("infrastructure maintenance" OR "infrastructure spending"
  OR "infrastructure expenditure" OR "infrastructure investment"
  OR "public infrastructure" OR "capital expenditure" OR "capital spending"
  OR "maintenance expenditure" OR "maintenance spending"
  OR "asset maintenance" OR "public works" OR "infrastructure budget*"
  OR "infrastructure financing" OR "infrastructure fund*"
  OR "road maintenance" OR "public capital stock")
AND
("developing countr*" OR "developing nation*"
  OR "low- and middle-income countr*" OR "low and middle income countr*"
  OR LMIC OR LMICs OR "emerging econom*" OR "emerging market*"
  OR "less developed countr*" OR "low-income countr*"
  OR "middle-income countr*" OR "third world" OR "global south"
  OR "transition econom*")
```

This is the string to adapt per database below — most databases need only
syntax substitutions (truncation symbol, field tags, phrase quoting), not a
change in logic.

## 4. Database-specific adaptations

### Scopus
Use `TITLE-ABS-KEY()` field tag; Scopus truncation is `*`, phrases in `" "`.

```
TITLE-ABS-KEY(("political corruption" OR corrupt* OR bribery OR bribe*
  OR embezzl* OR graft OR "rent-seeking" OR "rent seeking" OR clientelis*
  OR patronage OR "state capture" OR "political capture" OR kleptocracy
  OR cronyism OR "illicit enrichment" OR misappropriat*)
AND
("infrastructure maintenance" OR "infrastructure spending"
  OR "infrastructure expenditure" OR "infrastructure investment"
  OR "public infrastructure" OR "capital expenditure" OR "capital spending"
  OR "maintenance expenditure" OR "maintenance spending"
  OR "asset maintenance" OR "public works" OR "infrastructure budget*"
  OR "infrastructure financing" OR "infrastructure fund*"
  OR "road maintenance" OR "public capital stock")
AND
("developing countr*" OR "developing nation*"
  OR "low- and middle-income countr*" OR "low and middle income countr*"
  OR LMIC OR LMICs OR "emerging econom*" OR "emerging market*"
  OR "less developed countr*" OR "low-income countr*"
  OR "middle-income countr*" OR "third world" OR "global south"
  OR "transition econom*"))
```

### Web of Science (Core Collection)
Use `TS=()` (Topic: title/abstract/keywords/Keywords Plus); truncation `*`.

```
TS=(("political corruption" OR corrupt* OR bribery OR bribe* OR embezzl*
  OR graft OR "rent-seeking" OR "rent seeking" OR clientelis* OR patronage
  OR "state capture" OR "political capture" OR kleptocracy OR cronyism
  OR "illicit enrichment" OR misappropriat*)
AND
("infrastructure maintenance" OR "infrastructure spending"
  OR "infrastructure expenditure" OR "infrastructure investment"
  OR "public infrastructure" OR "capital expenditure" OR "capital spending"
  OR "maintenance expenditure" OR "maintenance spending"
  OR "asset maintenance" OR "public works" OR "infrastructure budget*"
  OR "infrastructure financing" OR "infrastructure fund*"
  OR "road maintenance" OR "public capital stock")
AND
("developing countr*" OR "developing nation*"
  OR "low- and middle-income countr*" OR "low and middle income countr*"
  OR LMIC OR LMICs OR "emerging econom*" OR "emerging market*"
  OR "less developed countr*" OR "low-income countr*"
  OR "middle-income countr*" OR "third world" OR "global south"
  OR "transition econom*"))
```

### EconLit (EBSCOhost)
EBSCO uses `AB`/`TI`/`SU` field codes and `*` truncation; wrap each block in
`TX` (all text) or `AB OR TI` if you want to restrict to abstract/title only.

```
TX (("political corruption" OR corrupt* OR bribery OR bribe* OR embezzl*
  OR graft OR "rent-seeking" OR clientelis* OR patronage OR "state capture"
  OR "political capture" OR kleptocracy OR cronyism OR "illicit enrichment"
  OR misappropriat*)
AND
("infrastructure maintenance" OR "infrastructure spending"
  OR "infrastructure expenditure" OR "infrastructure investment"
  OR "public infrastructure" OR "capital expenditure" OR "capital spending"
  OR "maintenance expenditure" OR "maintenance spending"
  OR "asset maintenance" OR "public works" OR "infrastructure budget*"
  OR "infrastructure financing" OR "infrastructure fund*"
  OR "road maintenance" OR "public capital stock")
AND
("developing countr*" OR "developing nation*"
  OR "low- and middle-income countr*" OR LMIC OR LMICs
  OR "emerging econom*" OR "emerging market*" OR "less developed countr*"
  OR "low-income countr*" OR "middle-income countr*" OR "third world"
  OR "global south" OR "transition econom*"))
```

### ProQuest (e.g., International Bibliography of the Social Sciences, PAIS)
ProQuest uses `noft()`/`ab()`/`ti()` and `*` truncation; same logic string
works inside `noft()` (anywhere except full text) or `ab,ti()`.

```
ab,ti(("political corruption" OR corrupt* OR bribery OR bribe* OR embezzl*
  OR graft OR "rent-seeking" OR clientelis* OR patronage OR "state capture"
  OR "political capture" OR kleptocracy OR cronyism OR misappropriat*)
AND
("infrastructure maintenance" OR "infrastructure spending"
  OR "infrastructure expenditure" OR "infrastructure investment"
  OR "public infrastructure" OR "capital expenditure" OR "capital spending"
  OR "maintenance expenditure" OR "maintenance spending"
  OR "asset maintenance" OR "public works" OR "infrastructure budget*"
  OR "infrastructure financing" OR "road maintenance")
AND
("developing countr*" OR "developing nation*" OR LMIC OR LMICs
  OR "emerging econom*" OR "emerging market*" OR "less developed countr*"
  OR "low-income countr*" OR "middle-income countr*" OR "third world"
  OR "global south" OR "transition econom*"))
```

### JSTOR
JSTOR's advanced search doesn't support wildcard truncation as broadly and
has a shorter query limit — shorten each block to the highest-yield 4-6 terms
and run in `((ab:(...)) AND (ab:(...)) AND (ab:(...)))` form, e.g.:

```
((ab:(corruption OR bribery OR "rent-seeking" OR clientelism))
AND (ab:("infrastructure maintenance" OR "infrastructure spending"
  OR "public infrastructure" OR "capital expenditure"))
AND (ab:("developing countries" OR "low- and middle-income countries"
  OR "emerging economies" OR "global south")))
```

### Google Scholar
No field tags/truncation support at scale; use a shortened, quoted phrase
version and rely on Scholar's implicit stemming, e.g.:

```
("political corruption" OR corruption OR bribery) AND ("infrastructure maintenance" OR "infrastructure spending" OR "public infrastructure") AND ("developing countries" OR "low- and middle-income countries" OR "emerging economies")
```

### World Bank / OECD / IMF repositories (grey literature)
These often only support simple keyword search — run the three-block terms
as separate saved searches per repository (e.g., `corruption infrastructure
maintenance spending developing countries`) rather than full Boolean syntax,
and screen the larger result set manually.

## 5. Suggested limiters (apply consistently across databases where supported)

- **Language:** English (note as a limitation if excluding non-English studies)
- **Document type:** peer-reviewed journal articles, working papers, reports
  (decide based on protocol — grey literature inclusion affects this)
- **Date range:** state explicitly in the protocol (e.g., no lower bound, or
  from year X representing the start of a relevant policy period)
- **Subject area:** restrict to Economics, Political Science, Public
  Administration, Development Studies where the database allows subject
  filtering (helps exclude unrelated "corruption" hits from medicine/criminal
  law, and unrelated "infrastructure" hits from computer/IT infrastructure)

## 6. Notes / next steps

- Run the string in each target database, record the number of hits per
  database and per concept block (for the PRISMA flow diagram).
- Pilot-test the string against a small set of known/seed papers to confirm
  sensitivity before running the full search.
- Log the exact string, date run, and number of results for each database in
  a search log (for reproducibility per PRISMA 2020 reporting guidelines).
