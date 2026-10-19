# Workflow and Persistent Records

## Scope record

Before searching, record the working question, candidate contribution, inclusion and exclusion criteria, languages, dates, document types, databases, and allowed access routes. Treat the proposed research gap as provisional.

## Search run record

Every database run should preserve:

```yaml
search_id:
database:
platform:
searched_at:
query_exact:
filters:
result_count:
export_format:
export_file:
file_sha256:
operator:
notes:
```

School credentials, cookies, MFA data, and browser profiles must never enter these records.

## Candidate and source records

Use DOI as the preferred canonical identifier, then stable database ID, then a normalized title-year key. The source manifest should track:

- canonical ID and citekey;
- title, authors, year, DOI;
- discovery source and search ID;
- screening decision and reason;
- access mode and local PDF path;
- Zotero key/collection when known;
- evidence level, reading status, and human-review status;
- checksum for locally managed source files when appropriate.

Do not create a second Literature Note when a citekey or DOI already has one.

## Institutional access

Use the user's authorized browser session for school SSO, proxy, VPN, CAPTCHA, or payment-bound access. The user completes credentials and MFA. Prefer database export functions (RIS, BibTeX, or CSV) over scraping. Stop and record the manual action when automated access is blocked.

## Small-batch processing

- Short, clean theory papers: 3-5 per batch.
- Long surveys, theses, or reports: 1-2 per batch.
- Complete the handoff and human review for one batch before starting a large next batch.

## Status vocabulary

Use the project statuses `inbox`, `screened`, `reading`, `extracted`, `human-reviewed`, `accepted`, `peripheral`, `excluded`, and `needs-verification` for paper notes. Use `waiting-review` for an AI-completed batch that has not been accepted by the user.

## Recovery record

For long work, update a concise audit/worklog with:

- time and task;
- files and sources read;
- files written;
- decisions and reasons;
- unresolved markers;
- current gate and next action.

Do not rely on chat history as the only workflow state.
