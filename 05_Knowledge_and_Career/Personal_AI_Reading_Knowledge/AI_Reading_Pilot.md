# AI Reading Pilot — Public Project Summary

## Purpose

The pilot explores how a large personal digital reading library can become a structured knowledge resource for continuous learning and professional development.

The workflow moves beyond a flat bookshelf: it inventories available metadata, identifies books with personal notes, organizes metadata into broad themes, and tests whether selected personal annotations can be retrieved and transformed into a portable Markdown knowledge asset.

## Pilot stages

### Stage 1 — Local bookshelf inventory

A local bookshelf snapshot was inspected. The reported inventory contained:

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

A classification pass assigned candidate themes using book titles and available metadata. A priority list was produced for human review.

**Limitation:** classification is metadata-based, not based on reading every book or verifying full contents. A title match is a discovery signal, not a content-quality assessment.

The strict title-signal intersection for AI + Finance + Management returned no confirmed three-way match in the pilot. Adjacent two-domain matches were kept distinct.

### Stage 4 — Personal-note overview and retrieval test

The personal-note overview reported **240 books with personal notes** and **1,470 personal-note records**.

The first prioritized test batch contained **10 books**. A targeted content test found retrievable personal-note content for **one book** in that batch. The other nine did not yield matching note content in this targeted test; this does not prove that those books have no notes in the source account.

The successful test retrieved:

- **11 highlights / underlined passages**
- **1 personal thought / comment**
- **1 personal review**
- **13 personal annotation records in total**

Bookmark information was returned only as a count; bookmark text was not available for export through the tested interface.

### Stage 5 — Local Markdown knowledge-base artifact

A local Markdown knowledge-base file was generated for the selected test book. It contains all 13 retrieved personal records, each with a unique local record ID, record type and AI-suggested topic label. Original wording was preserved and kept separate from AI-generated analysis.

Validation reported:

- 13 unique local record IDs.
- 13 of 13 source blocks passed verbatim comparison against the pilot source report.
- Available chapter, time and range metadata were retained where present.
- No additional API requests were made during Markdown file generation.
- No WeRead source data or previously generated source files were modified.

The populated Markdown artifact remains private and is intentionally not included in this public repository.

## Snapshot indicators

| Indicator | Reported value | Interpretation |
|---|---:|---|
| Electronic-book records in inspected export | 2,666 | Local bookshelf snapshot |
| Album / audiobook records | 27 | Separate record type |
| Books in personal-note overview | 240 | Notebook overview |
| Personal-note records in overview | 1,470 | Aggregate overview count |
| Books in first prioritized test batch | 10 | Selected for targeted testing |
| Books with note content retrieved in that batch | 1 | Result of this test only |
| Highlights / underlined passages retrieved | 11 | Successful retrieval |
| Personal thoughts / comments retrieved | 1 | Successful retrieval |
| Personal reviews retrieved | 1 | Successful retrieval |
| Total personal annotation records retrieved | 13 | One-book test |
| Records with unique local IDs | 13 | Local validation |
| Source blocks passing verbatim comparison | 13 / 13 | Local validation |
| Bookmark text | Not available | Count field only in tested interface |

Do not interpret the nine books without matching note content in this test batch as proof that they have no notes. Do not extrapolate the one-of-ten result to all 240 books. The 1,470 overview count is not the number of note bodies retrieved.

## Validation and controls

- Use only operations documented by the installed integration skill.
- Keep raw source exports unchanged.
- Preserve source identifiers and populated note text in private local files.
- Separate electronic books from albums/audiobooks.
- Keep progress status separate from inferred reading progress.
- Validate row counts, unique IDs and source-text fidelity after generating local indexes.
- Label title/metadata classifications as heuristic.
- Distinguish overview counts from successfully retrieved note content.
- Distinguish unavailable fields from empty fields and from API errors.
- Keep personal note content, book titles where account-specific, book identifiers and account credentials outside the public repository.
- Do not attempt to bypass DRM, platform restrictions or access controls.

## What this pilot demonstrates

The pilot demonstrates a practical architecture for turning personal reading metadata into a structured learning portfolio. It confirms that selected annotation types can be retrieved for one tested book, preserved verbatim in a local Markdown knowledge-base artifact, and augmented with separate AI topic suggestions.

It does **not** demonstrate automated understanding of all book contents, complete export of every WeRead data type, full-book or full-chapter text access, or verified semantic classification of every indexed title.
