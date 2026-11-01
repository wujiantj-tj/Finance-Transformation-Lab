# Personal AI Reading Knowledge System

A privacy-first prototype for turning a personal digital reading library into a structured, searchable and AI-assisted knowledge system.

This project documents the public, reusable architecture and methodology of a WeRead-based workflow. It does not publish personal annotations, highlights, book-level private records, API credentials, raw exports or account-specific identifiers.

## Objectives

- Build a structured index of books that contain personal notes.
- Organize reading material into useful knowledge domains.
- Identify a transparent, metadata-based professional-development shortlist.
- Distinguish source records from derived classifications and AI recommendations.
- Keep personal reading content under the account owner's control.

## Current pilot snapshot

The local pilot reported:
- **240 books** in the personal-notes indexing scope.
- **10 books** selected for the next prioritization batch.
- Subject groups including Finance & Accounting, AI & Technology, Controlling/FP&A, Investment & Wealth Management, Economics & Business Strategy, Data Analytics & BI, and SAP/ERP & Enterprise Systems.
- **185 records** in the displayed snapshot grouped as “Other / To be classified”.

These are snapshot figures, not a claim that every record has been reviewed or semantically verified. Refresh them when the private index is updated.

## Design principles

1. **Privacy by default** — publish methods and aggregate results, not personal reading content.
2. **Traceability** — retain source identifiers locally and distinguish metadata from derived labels.
3. **Evidence-aware classification** — title/metadata matches are discovery signals, not proof of full book content.
4. **Human review** — use AI to prioritize and organize; keep final reading decisions with the user.
5. **No credential leakage** — API keys and local environment files must never enter Git.

## Project structure

- [Pilot Overview](AI_Reading_Pilot.md)
- [Knowledge Base Architecture](Knowledge_Base_Architecture.md)
- [Classification Methodology](Classification_Methodology.md)
- [Roadmap](Roadmap.md)

## Data and privacy boundary

The public repository intentionally excludes raw WeRead JSON, CSV exports, local databases, personal highlights, annotations, reviews, bookmarks, notebook text, book/account identifiers, API keys, tokens, cookies, environment files, full-text book content and copyrighted reading material.

Only aggregate counts, generic workflow descriptions, conceptual schemas and reusable methodology belong here. Review future samples for personal or copyrighted content before publishing.

## Technology concept

The workflow combines a local export/index, metadata normalization, thematic classification, prioritization and Markdown reporting. A WeRead API integration may be used locally where the account owner has authorized access. This repository contains no credentials.

## Status

**Prototype / ongoing personal knowledge-management project.** Classification quality, coverage and usefulness should be validated iteratively.

## Disclaimer

This is an independent personal learning project, not affiliated with or endorsed by WeRead or Tencent. Product names identify the data source and integration context only.
