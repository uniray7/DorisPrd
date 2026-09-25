---
doc_id: INT-RFC-INDEX
document_type: RFC Index
audience: Internal
status: Draft
revision: 0.1
reviewer: Requester
applies_to: OLAP Service / Data Ingestion Pipeline; version TBD
language: en
---

# RFC index and creation guide

[繁體中文](README.zh-TW.md) · [Internal documentation](../README.en.md)

## Topic index

No RFCs exist yet; do not prefill decisions or invent approval records. New entries record RFC ID, topic, document status, decision state, and bilingual links.

## When to create an RFC

Use an RFC for consequential design choices, option comparisons, or decisions affecting multiple documents. Keep ordinary gaps in the relevant document's open questions.

## Naming and required sections

- Filenames: `0001-<topic>.zh-TW.md` and `0001-<topic>.en.md`, numbered sequentially.
- Follow the [authoring workflow](../../governance/authoring-workflow.en.md) for metadata; share the RFC ID across languages.
- Sections: background/decision, goals/non-goals, constraints, options, comparisons/trade-offs, recommendation, validation needs, decision/rationale, dependencies, open questions, and references.
- Support options with applicable evidence; recommendations are not approved decisions. After requester confirmation, record the reviewer, known date, and rationale.

## Open questions

Create RFCs according to actual design needs. For example, Doris version selection is pending, but a separate RFC has not been decided upon.
