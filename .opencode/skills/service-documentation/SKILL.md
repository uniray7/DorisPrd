---
name: service-documentation
description: Use when drafting, reviewing, translating, or updating PRDs, Feature Specs, RFCs, architecture, data flows, Service Specs, application and approval procedures, usage policies, or user guides for this repository's Apache Doris OLAP Service and Data Ingestion Pipeline. Applies bilingual authoring, evidence tiers, and the agreed review workflow.
---

# Service documentation

This is the executable skill entry point. `SKILL.zh-TW.md` is its Traditional Chinese companion; keep both aligned when changing these rules. Product documents must be delivered in Traditional Chinese and English.

## Required repository references

Before authoring, read the shared rules in [authoring workflow](../../../docs/governance/authoring-workflow.en.md), [reference policy](../../../docs/governance/reference-policy.en.md), and [glossary](../../../docs/governance/glossary.en.md). These own the detailed conventions; this skill orchestrates their application. Change shared rules in their bilingual owning documents rather than maintaining duplicate definitions here.

Use the [repository index](../../../README.en.md) and the relevant [internal](../../../docs/internal/README.en.md) or [external](../../../docs/external/README.en.md) index to locate documents. The requester confirmed one overall PRD, the existing audience/purpose folder structure, bilingual lightweight skeletons, and no operational documentation. Preserve these choices; leave all four Pipeline directories blank except for `.gitkeep`.

## 1. Purpose and audience

This repository holds documentation for a company-internal OLAP Service based on Apache Doris and a Data Ingestion Pipeline.

- **External** means service consumers in other departments of the company, not the public internet.
- **Internal** means the team designing, implementing, and operating the services.
- There is no existing mandatory company template or review process. Use the lightweight workflow below.
- The requester is currently the sole final reviewer and decision maker. Do not invent additional approval roles.

Use the responsibility table in the authoring workflow to locate each fact's owning document. Link rather than copying extensive definitions. Surface conflicts instead of silently overriding an approved decision.

## 2. Agreed project baseline

Treat the following as requester-provided context, not independently verified deployment evidence. Update it when the requester makes new decisions.

- Existing Data Ingestion Pipeline documents are approved designs, with implementation close to completion. The requester authorizes treating them as the current documentation baseline. Do not repeatedly reopen settled design decisions without a conflict or new requirement. This authorization does not prove that every capability is deployed, tested, or generally available.
- Existing Pipeline documents are confidential company-intranet material and cannot currently be added to this repository. Leave Pipeline documentation unfilled for now; importing those documents is not a prerequisite for other work. Do not request the confidential originals, invent their contents, or claim to have reviewed them.
- When another document or feature depends on Pipeline behavior, ask the requester targeted questions about only the necessary details (for example, an interface, delivery semantics, or error handling), explaining what decision they affect. Use information the requester confirms is suitable for this repository and attribute it to requester confirmation, not to inspection of the unavailable documents. Until answered, mark the dependent details as open questions and continue independent work.
- Apache Doris version candidates are **4.1.0 or 4.1.4**; selection is pending. These are requester-supplied candidates, not verified release or compatibility claims.
- The deployment design uses a self-managed **HashiCorp Nomad cluster with Consul and Vault on bare-metal machines**. Doris FE and BE run as Docker containers on the Docker daemons of Nomad agents. Do not infer specific Consul/Vault integration details, topology, storage, sizing, or HA behavior from this description.
- The product scope includes **monitoring and logs** for both the internal team and external consumers. External access primarily supports investigation and troubleshooting, with some information masked or withheld. Detailed exposure and masking rules are unresolved.
- Exposing **metrics** for consumers to integrate with their own alerting is a possible future direction, not a committed deliverable or an available capability. Do not infer a protocol, endpoint, schedule, or service-operated alerting feature.

Preserve unresolved decisions, including Doris version selection and the monitoring/logging access and masking model. Ask for details when the document under development depends on them, rather than blocking unrelated work.

## 3. Evidence and decision state

Apply the content-state definitions and lifecycle rules in the authoring workflow. Distinguish confirmed current state, approved specification, proposal, assumption, and open question with section-level labels or compact tables when interpretation depends on them. Do not turn requester-confirmed direction into verified operation, fabricate missing rules, or treat skeleton creation as specification approval.

## 4. External-reference credibility

Follow the reference policy's T1–T4 definitions, permitted uses, applicability checks, conflict handling, and citation records. Classify evidence per important claim; distinguish internal decision authority from external evidence and upstream capabilities from this service's offering. Do not claim to have accessed or verified unavailable sources.

## 5. Hybrid authoring workflow

Execute the hybrid workflow in the shared authoring document: inspect inputs, ask consequential questions, draft around non-blocking gaps, check evidence, produce both languages, request review/decisions, and finalize or publish only as directed. Use the current skeleton's open questions as a starting point rather than asking again about settled context. Preserve existing edits and keep Pipeline dependencies as targeted questions.

## 6. Bilingual and structural conventions

Use the authoring workflow's YAML metadata and bilingual conventions with the established `.zh-TW.md` / `.en.md` pairs. Follow the glossary, keep stable IDs and normative force aligned, and update the relevant indexes when adding or moving documents. Both languages have equal semantic standing. The skill retains its required `SKILL.md` entry point and `SKILL.zh-TW.md` companion.

## 7. External-facing content and observability

Apply the authoring workflow's external-content rules. Current external skeletons are unpublished authoring artifacts, with author-facing questions clearly labeled; resolve relevant gaps before publication. Decide access and masking in internal Feature Specs, then derive external capabilities, limitations, and examples from approved scope and availability. Keep prospective consumer metrics access in the PRD's future direction until decided.

## 8. Completion check

Before reporting completion, verify:

- The requested audience and document type are clear; existing decisions and edits are preserved.
- Current state, approved design, proposals, assumptions, and unknowns are distinguishable.
- Important external claims have appropriate evidence, applicability checks, and truthful verification status.
- External commitments reflect approved service scope and availability, with exposure rules respected.
- Both language versions, counterpart links, IDs, numerical values, and obligation strength agree.
- Changes to shared facts (e.g. quotas, retention, access rules, feature scope) have been checked against related PRDs, Feature Specs, architecture/data flows, Service Specs, and guides. Update affected documents within the task scope or explicitly identify pending dependent updates; do not claim consistency while they remain.
- Links and Markdown structure have been checked using available tooling appropriate to documentation changes.
- The final summary names changed files, key decisions, remaining questions, and actual review/validation status. Do not claim human approval, implementation verification, or publication that did not occur.
