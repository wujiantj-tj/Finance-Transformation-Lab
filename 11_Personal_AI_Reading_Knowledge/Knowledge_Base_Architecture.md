# Personal AI Reading Knowledge Base — Architecture

## 1. Conceptual flow

```text
Authorized WeRead account
        |
        v
Local data retrieval / user-authorized export
        |
        v
Private raw data layer
        |
        v
Normalization and validation
        |
        +---- Books
        +---- Albums / audiobooks
        +---- Personal notes and highlights
        |
        v
Private structured index
        |
        v
Metadata-based thematic classification
        |
        v
Priority shortlist + human review
        |
        v
Personal Markdown knowledge base
        |
        v
AI-assisted retrieval, synthesis and learning
```

The public repository documents the design only. Private source data and note content remain in explicitly controlled private storage.

## 2. Logical data layers

| Layer | Purpose | Public repository |
|---|---|---|
| Source | Original bookshelf and note records | Excluded |
| Normalized index | Consistent book, album and note metadata | Excluded |
| Classification | Theme labels and confidence / rationale | Method only |
| Prioritization | Candidate reading sequence | Method and aggregate summary |
| Knowledge base | Curated notes, summaries and source references | Personal content excluded |
| Presentation | Public documentation and aggregate metrics | Included |

## 3. Suggested conceptual entities

**Book:** private source identifier, title, author, category/publisher metadata, source update timestamp and explicitly returned reading status.

**Album / audiobook:** private source identifier, title, narrator/author metadata, track count and completion metadata where available.

**Personal note:** private note identifier, associated book identifier, note type, chapter reference, timestamp and original text. Original text is private and must not be published by default.

**Classification:** entity identifier, theme, evidence basis, confidence level, review status and reviewer decision.

## 4. Separate source facts from AI interpretation

Every derived record should identify whether a value is:
- **Source fact:** returned by the source system or present in the user's export.
- **Transformation:** normalized or calculated from source fields.
- **Heuristic:** inferred from title or metadata signals.
- **Human-reviewed:** explicitly confirmed or corrected by the user.

Do not present a heuristic label as verified book content.

## 5. Privacy and security controls

- Store API credentials in environment variables or a local secret manager.
- Add local secret files and raw exports to .gitignore.
- Never commit API keys, access tokens, cookies or account identifiers.
- Keep personal note text, private reviews and highlights out of public Git history.
- Use synthetic examples when demonstrating schemas.
- Review staged changes before every commit.
- If a secret is accidentally committed, revoke/rotate it; deleting the latest file alone does not remove it from Git history.

## 6. Known integration boundaries

The documented WeRead skill describes APIs for bookshelf synchronization, book information, chapter metadata, reading progress, notebook overview, highlights and personal reflections. The notebook overview provides counts and metadata; retrieving individual note content requires separate note-related calls.

The documented skill does not establish a general-purpose full-book-text export endpoint. Membership status should not be assumed to grant API access beyond documented endpoints.

## 7. Markdown-first knowledge representation

Markdown is portable, versionable and readable by humans and AI tools. Each curated knowledge item should include a title and source reference, topic tags, a short user-authored synthesis, key concepts and questions, links to related items, and review date/status.

Avoid copying large copyrighted passages. Prefer concise personal synthesis and short quotations only where legally appropriate.
