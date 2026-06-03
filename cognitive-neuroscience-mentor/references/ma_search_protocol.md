# MA-Search Protocol

Use this file when the user asks to search for literature, locate PDFs, download papers, organize a reading folder, or update literature indexes.

## Purpose

MA-search should do as much useful retrieval work as possible while staying legal, transparent, and verifiable.

It borrows the best operational ideas from academic research workflows and Nature-style academic search:

- define the exact search claim or literature need before collecting papers;
- search across multiple source tiers instead of relying on one database;
- verify bibliographic metadata before recommending a source;
- keep a record of where each PDF came from and why it was or was not downloaded;
- continue with fallback sources when one source fails;
- separate paper discovery, PDF retrieval, evidence relevance, and manuscript usefulness.

## Source Tiers

Use a tiered route rather than one broad search.

### Tier 1: Authoritative Metadata And Biomedical/Neuroscience Sources

Use first when available:

- PubMed;
- PubMed Central and NCBI OA utilities;
- Crossref DOI metadata;
- DOI landing pages;
- publisher article pages;
- Semantic Scholar or OpenAlex-style discovery for citation graph and related work.

Goal: verify that the paper exists, get the correct title/authors/year/DOI, and determine official access status.

### Tier 2: Legitimate Full-Text And Repository Sources

Use for PDF retrieval:

- publisher open-access PDF links;
- PubMed Central PDFs and OA packages;
- institutional repositories;
- university author pages;
- OSF, Zenodo, Figshare;
- arXiv, bioRxiv, medRxiv, psyArXiv;
- funder or government repositories;
- journal supplementary material pages.

Goal: obtain a legal PDF or preprint when the version is scientifically useful.

### Tier 3: Discovery Expansion

Use when Tier 1/2 fail or the query is broad:

- exact-title web search;
- DOI plus "pdf";
- author plus title plus "pdf";
- related-article and citation-chaining search;
- review/meta-analysis reference mining;
- backward and forward citation tracking;
- alternate title, acronym, and construct synonyms.

Goal: recover hard-to-find legitimate copies and identify adjacent literature.

Do not use pirated repositories or methods that bypass paywalls.

## Search Order

1. Inspect local project literature maps and folders when available:
   - `00_project_context/organized_workspace_manifest.md`
   - `03_literature/literature_inventory_by_theme.md`
   - `03_literature/mentor_literature_use_guide.md`
   - `03_literature/`
2. Define the exact search target:
   - concept/topic;
   - population;
   - task/paradigm;
   - method;
   - date range if relevant;
   - whether the user needs PDFs, citations, or an evidence summary.
3. Build search strings:
   - exact phrase query for known titles;
   - concept query for broad topics;
   - population + paradigm + method query;
   - synonym query for constructs and disorders;
   - DOI/title + PDF query for retrieval.
4. Search external sources using Tier 1 -> Tier 2 -> Tier 3 routing.
5. Deduplicate candidates by DOI, title, year, and first author.
6. For each candidate, classify PDF status:
   - downloaded and verified;
   - open access but download blocked in the current environment;
   - abstract/citation only;
   - behind paywall or institution login needed;
   - not found or bibliographically uncertain.
7. If a target paper is important but inaccessible, report the best legal route:
   - university library login;
   - interlibrary loan;
   - author request;
   - institutional repository alert;
   - preprint or accepted manuscript if available.

## Download Rules

- Download only legitimate PDFs from official, open, institutional, preprint, or author-hosted sources.
- Do not use pirated repositories or bypass paywalls.
- If a paper is not legally downloadable, provide citation, DOI, and access status instead.
- Prefer the version of record. If only a preprint or accepted manuscript is available, label it clearly.
- Use clear file names:

```text
FirstAuthor_Year_Short_Title.pdf
```

- Store files in the most relevant project folder, usually under `03_literature/[theme_folder]/`.
- If no suitable folder exists, create a focused folder with a readable name.
- Validate downloaded PDFs by checking that the file begins with `%PDF` and has a plausible size.
- If a download produces HTML, a redirect page, or a "preparing download" placeholder, do not keep it as a PDF.
- Remove or replace failed HTML placeholder downloads; do not leave fake `.pdf` files in the literature folder.

## Aggressive But Legitimate PDF Retrieval

When the user says "尽可能", "找到任何想要的文献", "download all PDFs", or invokes `MA-search`, use this fallback chain:

1. DOI landing page -> publisher PDF.
2. PubMed/PMC article page -> PMC PDF -> NCBI OA package API.
3. Crossref/OpenAlex/Semantic Scholar metadata -> `openAccessPdf` or equivalent field if available.
4. Exact title in web search with `filetype:pdf` and author/institution terms.
5. Institutional repository search by title and first author.
6. Preprint server search by title, DOI, and author.
7. Author homepage / lab publication page search.
8. Related review/reference list mining when the original target is vague.
9. If all fail, create a "not_downloaded" record with DOI, access status, and next legal acquisition route.

This is aggressive search, not illegal access. Do not imply that unavailable paywalled PDFs can always be obtained automatically.

## Index Update

After downloads, create or update a short index such as `README.md` or `source_index.md` in the target folder.

Include:

```text
File name
Full citation
DOI or URL
Why it is relevant
Support level: direct / partial / background / contradictory
Access status
PDF source URL or source type
Version: version of record / accepted manuscript / preprint / unknown
```

## Search Output

Default concise output:

```text
Downloaded:
Not downloaded:
Folder:
Index updated:
Next useful search:
```

Full output when requested:

```text
Search question
Search strings/sources
Candidate table
Downloaded and verified PDFs
Missing/blocked papers
Evidence relevance notes
Recommended reading order
Next legal acquisition route
```

## Quality Controls

- Verify bibliographic details before recommending a citation for manuscript use.
- Use DOI, PMID, PMCID, publisher page, or repository record where possible.
- If the title/year/authors do not match exactly, mark the candidate as uncertain.
- Prefer primary empirical papers and methods papers over broad summaries when the user needs manuscript support.
- Include contradictory or boundary-condition evidence when the question is interpretive.
- Mark unverified references clearly.
- Do not overfit search results to support the user's preferred interpretation.

## Folder Strategy

If the user gives no folder, use:

```text
03_literature/[topic_slug]/
```

Recommended topic slugs:

- `go_nogo_child_erp`
- `erp_microstate_methods`
- `attention_reading_math_risk`
- `dimensional_risk_approach`
- `frp_eye_tracking_eeg`
- `statistics_methods`

Keep project PDFs out of public skill repositories.
