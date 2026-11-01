# AI Reading Pilot — Public Project Summary

## Purpose

The pilot explores how a large personal digital reading library can become a structured knowledge resource for continuous learning and professional development.

The workflow moves beyond a flat bookshelf: it identifies books with personal notes, organizes available metadata into broad themes, and produces a reviewable shortlist.

## Pilot stages

### Stage 1 — Local bookshelf inventory

A local raw bookshelf export was inspected without API requests during the structural-analysis step. The reported snapshot contained:
- 2,666 electronic-book records.
- 27 album / audiobook records.
- No missing book titles in the inspected book records.
- Seven book records with missing author metadata.
- No reading-progress field in the raw bookshelf records.

The raw export was left unchanged. These figures describe that local snapshot.

### Stage 2 — Index and portfolio analysis

A combined local index kept book and album/audiobook record types distinct. A summary report recorded row counts, metadata gaps and validation checks.

A reading portfolio report summarized available metadata and identified professional-development candidates. It distinguished bookshelf update timestamps from publication years.

### Stage 3 — Semantic classification and prioritization

A second-stage classification assigned candidate themes using book titles and available metadata. A priority list was produced for human review.

**Limitation:** classification is metadata-based, not based on reading every book or verifying full contents. A title match is a discovery signal, not a content-quality assessment.

The strict title-signal intersection for AI + Finance + Management returned no confirmed three-way match in the pilot. Adjacent two-domain matches were kept distinct.

### Stage 4 — Personal-note knowledge-base pilot

The personal-note overview reported **240 books with personal notes**. The first prioritized batch contained **10 books**. A targeted content test of that batch found personal notes for **one book**; the other nine did not yield personal-note content in this test.

For the one book with notes, the workflow successfully retrieved:
- **11 highlights / underlined passages**
- **1 personal thought / comment**
- **1 personal review**

The source returned bookmark information only as a count field; bookmark content was not available for export through the tested interface.

This is a targeted test result, not evidence that the other books in the full 240-book set lack notes. The test deliberately used a small prioritized batch rather than downloading every note at once.

## Snapshot indicators

| Indicator | Reported value | Interpretation |
|---|---:|---|
| Electronic-book records in inspected export | 2,666 | Local snapshot |
| Album / audiobook records | 27 | Separate record type |
| Books in personal-note overview | 240 | Overview count |
| Books in first prioritized test batch | 10 | Selected for targeted testing |
| Books with notes found in that batch | 1 | Result of this test only |
| Highlights / underlined passages retrieved | 11 | Successful retrieval |
| Personal thoughts / comments retrieved | 1 | Successful retrieval |
| Personal reviews retrieved | 1 | Successful retrieval |
| Bookmark content | Not available | Count field only in tested interface |

Do not interpret the nine books without notes in this test batch as proof that they have no notes in the source account. Do not extrapolate the one-of-ten result to all 240 books.

## Validation and controls

- Keep raw source exports unchanged.
- Preserve source identifiers in private local files.
- Separate electronic books from albums/audiobooks.
- Keep progress status separate from inferred reading progress.
- Validate row counts and duplicate identifiers after generating local indexes.
- Label title/metadata classifications as heuristic.
- Distinguish overview counts from successfully retrieved note content.
- Distinguish unavailable fields from empty fields and from API errors.
- Keep personal note content, book identifiers and account credentials outside the public repository.

## What this pilot demonstrates

The pilot demonstrates a practical architecture for converting personal reading metadata into a structured, reviewable learning portfolio and confirms retrieval of selected note types for one tested book. It does not demonstrate automated understanding of all book contents, complete export of every WeRead data type, or verified semantic classification of every indexed title.
