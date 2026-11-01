# Personal AI Reading Knowledge System

A privacy-first prototype for turning a personal digital reading library into a structured, searchable and AI-assisted knowledge system.

This project documents the public, reusable architecture and methodology of a WeRead-based workflow. It does not publish personal annotations, highlights, book-level private records, API credentials, raw exports or account-specific identifiers.

## Objectives

- Build a structured index of books that contain personal notes.
- Organize reading material into useful knowledge domains.
- Identify a transparent, metadata-based professional-development shortlist.
- Distinguish source records from derived classifications and AI recommendations.
- Preserve personal source material locally while publishing only sanitized methods and aggregate validation results.

## Latest pilot snapshot

The latest local test reported:

- **2,666 electronic-book records** and **27 album / audiobook records** in the inspected bookshelf snapshot.
- **240 books with personal notes**, with **1,470 personal-note records** reported by the notebook overview.
- **10 books** in the first prioritized test batch.
- **1 of those 10 books** returned note content in the targeted content test. This is not a conclusion about the other books in the full library.
- The tested book yielded **11 highlights / underlined passages, 1 personal thought/comment and 1 personal review** — **13 records total**.
- All **13 source blocks** passed a verbatim comparison against the local pilot report, with 13 unique local record IDs.
- A private local Markdown knowledge-base file was generated with the 13 records, preserving original wording and separating AI-generated topic suggestions from source text.

Bookmark information was available only as a count; bookmark text was not exportable through the tested interface.

These are scoped test results. The one-of-ten result must not be extrapolated to all 240 books. The 1,470 count is the notebook overview total, not the number of note bodies retrieved in this pilot.

## Case studies and validation

- [Case Study 01 — From Personal Reading Notes to an AI-Ready Knowledge Asset](Case_Studies/01_Personal_Reading_Notes_to_AI_Knowledge.md) — sanitized proof of concept and privacy controls.
- [Pilot Validation Report](Validation_Report.md) — scope, latest counts, record-level validation and known limitations.

## Design principles

1. **Privacy by default** — publish methods and aggregate results, not personal reading content.
2. **Traceability** — retain source identifiers locally and distinguish metadata from derived labels.
3. **Evidence-aware classification** — title/metadata matches are discovery signals, not proof of full book content.
4. **Human review** — use AI to prioritize and organize; keep final reading decisions with the user.
5. **No credential leakage** — API keys and local environment files must never enter Git.
6. **Source/AI separation** — original personal notes, AI tags and AI analysis remain distinct fields.

## Project structure

- [Pilot Overview](AI_Reading_Pilot.md)
- [Pilot Validation Report](Validation_Report.md)
- [Knowledge Base Architecture](Knowledge_Base_Architecture.md)
- [Classification Methodology](Classification_Methodology.md)
- [Roadmap](Roadmap.md)
- [Case Studies](Case_Studies/)

## Data and privacy boundary

The public repository intentionally excludes raw WeRead JSON, CSV exports, local databases, personal highlights, annotations, reviews, bookmarks, notebook text, book/account identifiers, API keys, tokens, cookies, environment files, full-text book content and copyrighted reading material.

Only aggregate counts, generic workflow descriptions, conceptual schemas and reusable methodology belong here. Review future samples for personal or copyrighted content before publishing.

## Technology concept

The workflow combines a local export/index, metadata normalization, thematic classification, prioritization, note retrieval through documented interfaces, record-level validation and Markdown reporting. Personal source data remains in private local storage. This repository contains no credentials or populated personal-note records.

## Status

**Proof of concept completed for one selected book; broader coverage and repeatability remain under validation.** The next step is to validate note retrieval across a small additional batch before scaling to the complete note-bearing book list.

## Disclaimer

This is an independent personal learning project, not affiliated with or endorsed by WeRead or Tencent. Product names identify the data source and integration context only.
