# Case Study 01 — From Personal Reading Notes to an AI-Ready Knowledge Asset

## Executive summary

This case study documents a small, privacy-first proof of concept: retrieving selected personal annotations from a digital reading platform, preserving their original wording locally, and organizing them into a Markdown knowledge asset for later search, synthesis and AI-assisted learning.

The public case study describes the method and validation outcome only. It does **not** publish the source book title, account or book identifiers, original annotation text, review text, API credentials, raw API responses or copyrighted book content.

## Scope and verified outcome

One book was used as the first end-to-end test case.

| Data type | Retrieved records | Result |
|---|---:|---|
| Highlights / underlined passages | 11 | Retrieved |
| Personal thoughts / comments | 1 | Retrieved |
| Personal review | 1 | Retrieved |
| **Total personal annotation records** | **13** | **Validated locally** |
| Bookmark content | Not exported | The tested interface exposed a count, not the bookmark text |

The 13 source records were checked against the local pilot report. The validation reported 13 unique record IDs and a verbatim comparison pass for all 13 source blocks.

These figures describe this single test case only. They do not establish the coverage or retrieval success rate for the complete reading library.

## Workflow

1. **Discover documented capabilities** — inspect the integration skill documentation and use only documented API operations.
2. **Retrieve the permitted source data** — request the selected book's available personal annotation data without attempting to bypass access controls or DRM.
3. **Preserve source evidence** — retain the original wording, source record ID and available structural metadata in a private local artifact.
4. **Add a separate knowledge layer** — attach a stable local record ID, annotation type and AI-suggested topic labels without replacing the source text.
5. **Validate** — compare each extracted record with its source block and check record counts and uniqueness.
6. **Publish a sanitized case study** — share the workflow, aggregate results and limitations; keep personal content private.

## Suggested knowledge-record schema

| Field | Purpose |
|---|---|
| record_id | Stable local identifier for the knowledge record |
| source_record_id | Original source identifier; keep private where it can identify an account record |
| source_type | Highlight, thought/comment or review |
| source_text | Verbatim personal annotation; private by default |
| topic_tags | AI-suggested themes, clearly marked as derived |
| chapter_or_section | Source location, when provided |
| created_at / updated_at | Source timestamps, when provided |
| validation_status | Whether the source text was checked against the retrieved record |

The public repository intentionally does not contain populated personal records.

## What the proof of concept establishes

- The documented integration was sufficient to retrieve selected annotation types for the tested book.
- The extracted personal records could be preserved in a local Markdown-first workflow.
- Source text and AI-generated topic labels can be kept as separate layers.
- A record-level validation step can make the transformation auditable.

## What it does not establish

- It does not prove that all books with notes can be retrieved.
- It does not provide full-book or full-chapter text.
- It does not export bookmark content where the interface returns only a count.
- It does not demonstrate that AI topic labels are correct without human review.
- It does not establish that a paid membership grants unrestricted API access; access depends on the documented interface and applicable platform rules.

## Privacy, copyright and security controls

- Keep raw API responses, personal highlights, thoughts, reviews and source identifiers in private local storage.
- Never commit API keys, tokens, cookies, environment files or raw exports.
- Do not publish copyrighted book text or reproduce private annotations in this public case study.
- Do not bypass DRM, platform restrictions or access controls.
- Publish only generalized methodology, sanitized schemas and appropriately aggregated validation results.
- Review every generated artifact before committing it to a public repository.

## Reusable lessons for Finance knowledge management

The same architecture can support a controlled Finance knowledge base:

- Preserve the original source (policy, process note, training material or personal learning note).
- Add a structured metadata layer for topic, process, system, business role and effective date.
- Separate extracted facts from AI interpretation and recommendations.
- Keep provenance and validation status visible.
- Publish reusable methods while protecting confidential or personal source material.

This pattern is relevant to Finance transformation because it creates traceable knowledge assets without confusing source evidence with AI-generated interpretation.

## Status

**Proof of concept completed for one selected book.** Broader coverage, repeatability across different note types and the quality of AI-generated topic labels require further testing.
