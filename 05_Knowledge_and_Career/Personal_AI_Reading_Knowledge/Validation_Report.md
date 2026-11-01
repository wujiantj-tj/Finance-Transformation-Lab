# Pilot Validation Report — Personal AI Reading Knowledge

**Status:** Proof of concept completed for one selected book  
**Scope:** Local bookshelf inventory, notebook overview, one targeted note-content test and one local Markdown artifact  
**Public-data policy:** Aggregate metrics and workflow only; no personal annotation text or account-specific book identifiers

## 1. Source inventory snapshot

| Measure | Result |
|---|---:|
| Electronic-book records in local bookshelf snapshot | 2,666 |
| Album / audiobook records | 27 |
| Books reported in notebook overview as having personal notes | 240 |
| Personal-note records reported by notebook overview | 1,470 |

The 240-book and 1,470-record figures describe the notebook overview. They are not equivalent to 240 books or 1,470 note bodies having been downloaded.

## 2. Targeted retrieval test

The first prioritized test batch contained 10 books. One book returned note content in the targeted test.

| Retrieved record type | Count |
|---|---:|
| Highlights / underlined passages | 11 |
| Personal thoughts / comments | 1 |
| Personal reviews | 1 |
| **Total retrieved personal annotation records** | **13** |

The source interface returned bookmark information as a count only. Bookmark text was not available for export through the tested interface.

The nine other books in the first batch did not yield matching note content in this targeted test. This is not proof that those books have no notes in the account.

## 3. Local Markdown artifact validation

A private local Markdown knowledge-base file was generated for the selected test book.

| Validation check | Result |
|---|---|
| Unique local record IDs | 13 |
| Source blocks checked | 13 |
| Verbatim source comparison | 13 / 13 passed |
| Record types and AI topic suggestions | Present for each record |
| Available chapter/time/range metadata | Retained where present |
| Personal source text uploaded to this public repository | No |
| Additional API calls during Markdown generation | No |
| WeRead source data modified | No |

Original personal annotation text remains in private local storage. AI topic labels and analysis are separate from source wording.

## 4. Confirmed capabilities and boundaries

### Confirmed in this pilot

- A local bookshelf snapshot can be indexed and validated.
- The notebook overview can report books with notes and aggregate note counts.
- Selected personal annotation types were retrievable for one tested book.
- Retrieved personal records can be preserved in a Markdown-first local knowledge-base format.
- A record-level verbatim comparison can be used to validate source-text fidelity.

### Not demonstrated

- Complete note-body retrieval for all 240 books.
- Export of bookmark text through the tested interface.
- General-purpose full-book or full-chapter text retrieval.
- Full-text access as a consequence of membership status.
- Accuracy of all AI-generated topic labels without human review.

## 5. Privacy and publication controls

This public report intentionally excludes:

- Personal highlights, thoughts, reviews and bookmark content.
- Book title and account-specific book identifiers from the tested personal record.
- Raw API responses, JSON/CSV exports and local databases.
- API keys, access tokens, cookies and environment files.
- Full-book or chapter text.

The populated knowledge-base Markdown file remains private. The repository publishes only aggregate results, workflow descriptions and validation methodology.

## 6. Recommended next validation step

Test a small additional batch of books from the notebook overview, using documented read-only operations. Record retrieval coverage separately from overview counts, preserve source text locally, and review the privacy boundary before any publication.

Do not scale to bulk export until the note-type behavior, pagination and validation process are repeatable.
