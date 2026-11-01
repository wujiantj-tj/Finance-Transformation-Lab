# Roadmap

## Current status

**Prototype completed; iterative development planned.**

The pilot demonstrated local bookshelf indexing, metadata-based thematic classification, shortlist generation and a limited personal-note retrieval test. A later snapshot reported 240 books in the personal-note indexing scope and a 10-book next-batch shortlist.

## Phase 1 — Stabilize the private data pipeline

- [ ] Define a repeatable local import / synchronization procedure.
- [ ] Validate schema changes and API response fields.
- [ ] Add repeatable duplicate and missing-metadata checks.
- [ ] Keep source exports immutable and timestamp each snapshot.
- [ ] Add local-only secret and data-file exclusions to Git.

## Phase 2 — Improve classification quality

- [ ] Refine the theme taxonomy.
- [ ] Add explicit evidence and confidence fields.
- [ ] Separate metadata-based suggestions from human-reviewed labels.
- [ ] Review ambiguous and unclassified records in batches.
- [ ] Measure classification coverage and human correction rate.

## Phase 3 — Curate the personal knowledge base

- [ ] Define a consistent Markdown template for curated knowledge items.
- [ ] Link notes to source books and chapter references where available.
- [ ] Separate original personal notes from AI-generated synthesis.
- [ ] Add topic indexes and cross-links.
- [ ] Keep all personal note content in private storage.

## Phase 4 — Build AI-assisted learning workflows

- [ ] Search across curated personal knowledge items.
- [ ] Generate review questions from user-authored summaries.
- [ ] Compare concepts across books with source references.
- [ ] Create learning paths for Finance Transformation, SAP, Controlling/FP&A and AI in Finance.
- [ ] Add human review before promoting generated material into the knowledge base.

## Phase 5 — Evaluate usefulness

Potential measures include the percentage of indexed books with reviewed themes, metadata completeness, number of curated knowledge items, retrieval success for user-defined questions, time to locate a previously captured insight, and user-rated usefulness of generated learning paths.

These are proposed measures; no performance results are claimed yet.

## Non-goals

- Publishing private WeRead notes or highlights.
- Republishing copyrighted books or full chapters.
- Exposing API keys or account-specific identifiers.
- Treating title-based classification as full-content understanding.
- Claiming complete access to WeRead content based solely on membership status.
