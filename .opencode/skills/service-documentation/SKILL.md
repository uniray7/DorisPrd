---
name: service-documentation
description: Use when drafting, reviewing, translating, or updating PRDs, Feature Specs, RFCs, architecture, data flows, Service Specs, application and approval procedures, usage policies, or user guides for this repository's Apache Doris OLAP Service and Data Ingestion Pipeline. Applies bilingual authoring, evidence tiers, and the agreed review workflow.
---

# Service documentation

This is the executable skill entry point. `SKILL.zh-TW.md` is its Traditional Chinese companion; keep both aligned when changing these rules. Product documents must be delivered in Traditional Chinese and English.

## 1. Purpose and audience

This repository holds documentation for a company-internal OLAP Service based on Apache Doris and a Data Ingestion Pipeline.

- **External** means service consumers in other departments of the company, not the public internet.
- **Internal** means the team designing, implementing, and operating the services.
- There is no existing mandatory company template or review process. Use the lightweight workflow below.
- The requester is currently the sole final reviewer and decision maker. Do not invent additional approval roles.

| Document | Responsibility |
| --- | --- |
| PRD | Problem, users, goals, scope, non-goals, success criteria, and requirements. |
| Feature Spec | Detailed behavior, rules, states, exceptions, and acceptance criteria. |
| RFC | Decision to be made, options, trade-offs, recommendation, and eventual decision. |
| System Architecture | Components, interfaces, dependencies, and responsibility boundaries. |
| Data Flow | Sources, destinations, transformations, and relevant delivery, failure, and recovery behavior. |
| External Service Spec | Consumer-visible capabilities, supported scope, quotas, limits, and approved service commitments. |
| External procedures and guides | Service application, approval, onboarding, usage, troubleshooting, and usage policies. |

Use these responsibilities to decide where a fact belongs. Link to its owning document rather than copying extensive definitions. A draft must not silently override an approved document; surface conflicts to the requester.

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

Distinguish these states wherever their difference affects interpretation. Prefer section-level labels or compact tables to tagging every sentence.

| State | Meaning |
| --- | --- |
| Confirmed current state | Supported by implementation, configuration, observations, tests, or explicit requester confirmation of actual operation. Identify the basis. |
| Approved specification | Decided, but implementation or rollout may still be pending. |
| Proposal | A suggested option awaiting a decision. |
| Assumption | A temporary premise requiring validation. |
| Open question | Missing information or an unresolved decision. |

Document lifecycle and implementation state are separate: an approved design is not automatically an available service. Preserve the Pipeline baseline exception as described above without upgrading it to verified production operation.

- Never fill gaps with invented SLAs/SLOs, quotas, retention periods, limits, API behavior, support windows, architecture choices, or delivery dates.
- Offer useful proposals with reasons; label them as proposals. Keep numerical examples and placeholders distinct from requirements.
- Record consequential decisions with an identifier, decision, reviewer, date when known, and rationale or source. Do not fabricate historical dates or approval records.
- When inputs conflict, identify the conflicting claims and their states. Ask the requester to resolve service or design decisions; use applicable technical evidence to investigate factual behavior.

## 4. External-reference credibility

Assign tiers to the evidence supporting each important claim, not merely to a website or organization.

| Tier | Examples | Allowed use |
| --- | --- | --- |
| T1 — Authoritative primary evidence | Applicable-version official docs, release notes, source code, and formal standards. | Primary support for technical behavior and limits, subject to version, configuration, and evidence scope. |
| T2 — Traceable first-hand explanation | Maintainer issue/PR discussions, design proposals, engineering reports with environment and method. | Design analysis and contextual evidence. An open proposal or individual report does not establish a supported feature. |
| T3 — Corroborated secondary material | Third-party articles or tutorials with citations, versions, and reproducible methods. | Explanation and discovery; corroborate consequential claims with applicable T1 evidence or relevant first-hand validation. |
| T4 — Unverified information | Unsourced claims, unsupported forum answers, and AI-generated summaries. | Search or validation leads only; never the sole basis for a specification. |

- Authority, applicability, and verification are separate. Evaluate version, date, configuration, workload, deployment model, and whether the source describes a proposal or released behavior.
- Official authorship alone does not make marketing claims or benchmarks universal guarantees. A source-code observation is not necessarily a supported public contract.
- Do not assume `/latest/` documentation describes either Doris candidate. Check versioned references before making version-specific claims. If unavailable, mark the claim unverified and identify the needed check.
- For important technical claims, keep a nearby reference ID and a source record: title, URL or repository path, tier for external sources, version/revision and publication date if known, access date, supported claim, applicable conditions, and local-validation status. Use `unknown` or `not verified` when appropriate.
- Internal approved decisions and requester statements are decision authority, not external credibility tiers. Reference their origin separately; do not label them T1 by default.
- No source allowlist or denylist has been specified. Prefer applicable primary evidence and use lower tiers according to the table.
- If sources disagree, retain the conflict and explain differences in version or scope when supported. Do not resolve it by averaging claims or silently selecting the convenient one.
- If a source cannot be accessed, say so. Do not fabricate a citation, quotation, verification result, or access date.
- Apache Doris capabilities do not automatically become capabilities or guarantees of this managed service. Confirm service scope and implementation status separately.

## 5. Hybrid authoring workflow

1. **Inspect inputs.** Read repository instructions, relevant existing documents, and supplied decisions. Identify audience, document type, scope, and dependencies. Preserve existing user work.
2. **Ask consequential questions first.** Clarify missing information that materially changes service commitments, architecture, access boundaries, data semantics, or acceptance criteria. Group related questions. Do not require answers to every minor detail before drafting.
3. **Draft around non-blocking gaps.** Structure the document from known inputs; mark proposals, assumptions, and open questions explicitly. Each important open question should state what decision is needed and what it affects.
4. **Check evidence.** Verify consequential external claims using the tier rules. Trace product requirements to requester decisions or approved specifications. Distinguish upstream capability from this service's offering.
5. **Produce the bilingual pair.** Use Traditional Chinese with English technical terms and a complete English counterpart. Review both for semantic parity.
6. **Review and decide.** Present material changes, unresolved decisions, evidence gaps, and affected documents to the requester. Only the requester can approve. Generating a polished draft or translation does not constitute approval.
7. **Finalize or publish as directed.** Apply accepted decisions and synchronize affected documents and languages. Do not label a draft approved/published or perform a release without the corresponding requester decision.

For a new topic, establish purpose and service boundaries before detailed design. Create only the document types useful for the current task; do not automatically generate every type in the table.

## 6. Bilingual and structural conventions

- Default product-document naming: `<topic>.zh-TW.md` and `<topic>.en.md` in the same directory. Preserve an established repository layout if one is introduced; avoid unsolicited bulk renames or translations of unrelated legacy files.
- Both languages have equal semantic standing. Draft in the working language of the discussion, then produce the other version. Resolve ambiguity with the requester rather than assuming one language overrides the other.
- Give paired documents the same stable document ID and revision, equivalent status, and links to each other. Localized headings may differ; requirement, decision, and reference IDs must match when used.
- Keep requirements, obligations, numerical values, units, examples, limitations, evidence states, references, and open questions equivalent. Translate normative force accurately (`must`, `should`, `may`). Never strengthen a commitment during translation.
- Use Traditional Chinese prose with English technical terms. Define unfamiliar abbreviations at first use; keep service/component names and identifiers consistent. Maintain a shared glossary when terminology ambiguity or reuse warrants it.
- Minimum document metadata: document ID, type, audience, lifecycle status, revision or last-updated date, reviewer, applicable service/version (including unresolved selection), and counterpart link. Add an owner only if known; do not invent people or dates.
- Suggested lifecycle: `Draft → In Review → Approved → Published` where publication is applicable; use `Superseded` for replaced documents. Treat this as a lightweight default, not a requirement for extra company approval roles.
- Use the relevant sections from the document responsibility table, followed as needed by decisions, open questions, references, and related documents. Avoid empty boilerplate sections; state `not applicable` only when useful.
- A bilingual change is ready for approval only when both versions agree. If one cannot be completed, report the pair as incomplete rather than claiming synchronized completion.
- The skill itself is a filename exception: OpenCode requires `SKILL.md`. Its Chinese companion is `SKILL.zh-TW.md`.

## 7. External-facing content and observability

- External documentation describes capabilities and commitments confirmed as available for the intended audience. Approved but unreleased design may be documented as explicitly planned or preview material when requested, with its status clearly visible.
- Derive consumer documentation from approved internal specifications while checking rollout status. Explain application and approval procedures only to the extent decided; do not invent approvers, turnaround times, or approval guarantees.
- For external monitoring/logging documentation, clarify relevant identity/access scope, visible information, masked/withheld information, investigation workflow, and any decided retention/query limits. Keep unresolved policies as internal open questions until decided.
- External examples, screenshots, diagrams, and sample logs must follow the agreed visibility rules. Do not infer that the internal view is safe to expose; use clearly labeled illustrative placeholders while those rules are unresolved.
- Distinguish monitoring views, log investigation, metrics access, and alerting ownership. Future user-managed alerts do not imply service-managed alert delivery.
- Keep internal infrastructure details and operational procedures in their owning internal documents unless explicitly approved and needed for consumers. External sources cannot decide internal exposure policy.

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
