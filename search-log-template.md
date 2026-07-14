# Search Log Template

Companion to `search-strategy.md`. Use `search-log-template.csv` (import into
Excel/Google Sheets) to record each database search as it is run — this is
the raw material for the PRISMA 2020 flow diagram and for the "Search
strategy" section of the review write-up.

## Column definitions

| Column | What to record |
|---|---|
| `Database` | Name of the bibliographic database (e.g., Scopus, EconLit) |
| `Platform/Interface` | Vendor/interface used to access it (e.g., EBSCOhost, ProQuest, Clarivate) — some databases are reachable via multiple platforms, and syntax varies by platform |
| `Date searched` | ISO date (YYYY-MM-DD) the search was actually run — searches should ideally all be run within a short window of each other |
| `Search string version` | Reference to the exact string used (e.g., `v1`, or a link/commit hash to the version in `search-strategy.md` if the string is revised mid-review) |
| `Limiters applied` | Language, date range, document type, subject area filters actually applied in that database's interface |
| `Records retrieved` | Total hits returned by the search, before deduplication |
| `Duplicates removed` | Number removed when merging this database's results into the master reference set (fill in during deduplication, not at search time) |
| `Notes` | Anything database-specific: syntax had to be simplified, a term didn't work, subject filter unavailable, etc. |

## Process

1. Run the adapted search string for each database listed in
   `search-strategy.md`.
2. Immediately log the date, exact string version, limiters, and raw hit
   count in `search-log-template.csv` — do this the same day the search is
   run, before screening starts.
3. Export/download all records (RIS or CSV) into your reference manager
   (e.g., Zotero, EndNote, Covidence, Rayyan).
4. After deduplication across all databases, fill in the
   `Duplicates removed` column per database (or record total duplicates
   removed as a single combined figure if your tool doesn't attribute
   duplicates back to source database).
5. Total `Records retrieved` minus total duplicates gives the "Records after
   duplicates removed" figure for the PRISMA flow diagram's identification
   stage.
6. If the search string changes during the review (e.g., after a pilot test
   reveals missed seed papers), bump the version label (`v2`, `v3`, …), note
   the change and rationale in `search-strategy.md`, and re-run all
   databases under the new version — don't mix result counts from different
   string versions in the same log row.
