---
doc_id: GOV-REFERENCES
document_type: Governance
audience: Contributors
status: Draft
revision: 0.1
reviewer: Requester
applies_to: Repository
language: en
---

# External-reference policy

[繁體中文](reference-policy.zh-TW.md)

This shared definition consolidates the accepted credibility tiers and citation principles; the consolidated document remains pending review.

## Credibility tiers

Classify the specific evidence and supported claim, not merely the website or organization.

| Tier | Examples | Use |
| --- | --- | --- |
| T1 | Applicable-version official docs, release notes, source code, formal standards | Primary evidence for behavior and limits, subject to version, configuration, and scope. |
| T2 | Maintainer issues/PRs, first-hand design proposals, engineering reports with environment and method | Analysis and context; proposals or individual reports do not establish supported capabilities. |
| T3 | Third-party articles/tutorials with citations, versions, and reproducible methods | Explanation and discovery; corroborate important claims with applicable T1 or relevant first-hand validation. |
| T4 | Unsourced claims, unsupported forum answers, AI summaries | Search/validation leads only, never the sole basis for a specification. |

## Applicability and validation

- Assess authority, applicability, and verification separately. Check version, date, configuration, workload, deployment model, and whether behavior is released.
- Do not assume `/latest/` applies to a Doris candidate; prefer matching versions. Candidate versions themselves do not establish verified release status or compatibility.
- Official benchmarks or marketing statements are not universal performance guarantees. Source-code observations do not necessarily establish supported public contracts.
- Upstream Apache Doris capabilities are not automatically this service's capabilities or guarantees; confirm service scope and availability separately.
- Preserve conflicting claims and version/condition differences. Do not average claims or silently select the convenient source.
- When evidence is unavailable or inaccessible, mark it unverified and state the needed check. Do not invent quotations, citations, access dates, or validation results.
- There is no source allowlist/denylist; prefer applicable primary material.

## Citation records

Place reference IDs near important claims and record the following in that document's references section. Both languages use the same IDs and evidence; translation does not change tiers.

| Field | Recording convention |
| --- | --- |
| ID, title, location | Stable ID, source title, URL or repository path. |
| Tier | T1–T4 for external sources. |
| Version/revision, publication date | Record known information; otherwise `unknown`. |
| Access date | Actual access date; state truthfully when not accessed. |
| Supported claim, applicability | What the source supports and under which limits. |
| Local validation | Method, result, and evidence location, or `not verified`. |

Requester statements and approved internal decisions are decision sources, not automatically T1. Record confirmed content and available provenance without claiming to have read inaccessible Pipeline documents. Use only information the requester confirms is suitable to record.

## Open questions

- Recheck version-dependent references once the Doris version is selected; do not create fictitious product citations now.
