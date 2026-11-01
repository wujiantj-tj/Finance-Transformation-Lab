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

The documented workflow was tested on one selected book to verify retrieval of selected personal highlights and reflections. A later local indexing snapshot reported **240 books with personal notes** and produced a next-batch shortlist of 10 books.

The public project excludes extracted note text, book identifiers, personal reflections and private book-level records.

## Snapshot indicators

| Indicator | Reported value | Interpretation |
|---|---:|---|
| Electronic-book records in inspected export | 2,666 | Local snapshot |
| Album / audiobook records | 27 | Separate record type |
| Books in personal-note indexing scope | 240 | Later local snapshot |
| Next-batch shortlist | 10 | Candidates for human review |
| “Other / To be classified” in displayed subject summary | 185 | Backlog in that snapshot |

Do not add figures from different stages as if they were measured at the same time or from the same dataset.

## Validation and controls

- Keep raw source exports unchanged.
- Preserve source identifiers in private local files.
- Separate electronic books from albums/audiobooks.
- Keep progress status separate from inferred reading progress.
- Validate row counts and duplicate identifiers after generating local indexes.
- Label title/metadata classifications as heuristic.
- Keep personal note content and account credentials outside the public repository.

## What this pilot demonstrates

The pilot demonstrates a practical architecture for converting personal reading metadata into a structured, reviewable learning portfolio. It does not demonstrate automated understanding of all book contents, complete export of every WeRead data type, or verified semantic classification of every indexed title.
