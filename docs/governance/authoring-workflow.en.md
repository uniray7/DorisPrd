---
doc_id: GOV-WORKFLOW
document_type: Governance
audience: Contributors
status: Draft
revision: 0.1
reviewer: Requester
applies_to: Repository
language: en
---

# Authoring and maintenance workflow

[繁體中文](authoring-workflow.zh-TW.md)

This document consolidates the discussed collaboration rules for contributors and the skill. It remains Draft pending requester review of the consolidated text. There is no existing mandatory company template or review process; Requester is currently the sole final reviewer and decision maker.

## Document responsibilities

| Type | Primary responsibility |
| --- | --- |
| Overall PRD | Problems, users, goals, scope, non-goals, success criteria, and requirements. |
| Feature Spec | Detailed behavior, rules, states, exceptions, and acceptance criteria. |
| RFC | Decision, options, trade-offs, recommendation, and eventual resolution. |
| System Architecture | Components, interfaces, dependencies, and responsibility boundaries. |
| Data Flow | Sources, destinations, transformations, delivery, failure, and recovery behavior. |
| External Service Spec | Consumer-visible capabilities, supported scope, quotas, limits, and approved commitments. |
| External procedures, guides, and policies | Application, approval, usage, troubleshooting, consumer responsibilities, and usage rules. |

Each shared fact has an owning document; other documents link to it. Drafts must not silently override approved decisions. Identify conflicting claims and their states; the requester resolves product decisions, while technical facts are investigated under the [reference policy](reference-policy.en.md).

## Content states and document lifecycle

| Content state | Meaning |
| --- | --- |
| Confirmed current state | Supported by implementation, configuration, observations, tests, or requester confirmation of actual operation; identify the basis. |
| Approved specification | Decided, but implementation or rollout may be pending. |
| Proposal | A reasoned suggestion awaiting a decision. |
| Assumption | A temporary premise requiring validation. |
| Open question | Missing information or an unresolved decision; explain the impact. |

Lifecycle: `Draft → In Review → Approved → Published`; use Published only where applicable and `Superseded` for replaced documents. Approval does not establish feature availability. Do not invent human approval, implementation verification, or publication.

The requester authorizes existing Pipeline designs as the documentation baseline, not as verified production operation. Confidential documents are not imported; ask about dependencies as needed and leave unanswered details open.

## Hybrid workflow

1. Read repository instructions, related documents, and requester decisions. Identify audience, type, scope, and dependencies; preserve existing edits.
2. First clarify consequential gaps affecting service commitments, architecture, access boundaries, data semantics, or acceptance criteria. Group related questions.
3. Draft around other gaps with explicit proposals, assumptions, and open questions. Do not invent SLAs/SLOs, quotas, retention, interfaces, support windows, or delivery dates. Distinguish numerical examples from requirements.
4. Check important claims and sources; distinguish upstream Apache Doris capabilities, this service's scope, and actual availability.
5. Produce both languages and check semantic parity. Establish purpose and boundaries before detailed design; follow the agreed skeletons without independently expanding document types.
6. Present changes, pending decisions, evidence gaps, and affected documents for requester review and decisions.
7. Finalize/publish as directed and synchronize related documents and languages. Record consequential decisions with IDs, content, reviewer, known dates, and rationale/source; do not fabricate history.

## Metadata and bilingual maintenance

Use YAML frontmatter with `doc_id`, `document_type`, `audience`, `status`, `revision`, `reviewer`, `applies_to`, and `language`, plus a relative counterpart link in the body. Add owners or dates only when known. Metadata keys and shared values use consistent English identifiers; `TBD` means undecided.

- Place `.zh-TW.md` / `.en.md` pairs in the same directory with matching IDs, revisions, status, and applicability.
- Both languages have equal semantic standing. Draft in the discussion language, then produce the counterpart; resolve ambiguity with the requester.
- Match requirements, values, units, examples, limits, evidence states, references, open questions, and the force of `must` / `should` / `may`.
- Use Traditional Chinese prose with English technical terms, explain abbreviations at first use, and follow the [glossary](glossary.en.md).
- Report unsynchronized pairs as incomplete and not ready for approval. Preserve established layout; avoid unsolicited bulk renames or unrelated translations.
- The skill is a filename exception: `SKILL.md` is the entry point and `SKILL.zh-TW.md` its Chinese companion.

## External drafts and final content

External documents currently contain authoring skeletons. Their open questions are author tasks, not consumer instructions or service commitments. Resolve relevant gaps before publication.

- Final external content must reflect confirmed availability for its audience and approved commitments. Describe plans/previews early only when requested, with explicit status.
- Service Specs own capabilities and technical limits; Usage Policy owns consumer responsibilities. Guides reference specifications rather than defining separate quotas or commitments.
- Do not infer application approvers, turnaround times, or approval guarantees. Requester here is the documentation reviewer, not automatically the service-application approver.
- Internal specifications decide monitoring/log access and masking policies. External examples, screenshots, diagrams, and logs must follow those decisions. Until then, use explicitly illustrative placeholders without exposing internal data.
- Keep infrastructure details and procedures internal unless approved and needed by consumers. External sources cannot decide exposure policy.
- Distinguish monitoring, logs, metrics, and alerting ownership; future consumer-managed alerts do not imply service-managed alerting.

## Completion checks

- Preserve user work and make audience, document type, and content states clear.
- Check important sources for credibility, applicability, and truthful verification status.
- Check bilingual metadata, IDs, values, obligation strength, section meaning, and counterpart links.
- For shared-fact changes, check the PRD, Feature Specs, architecture/data flows, Service Specs, and guides. Update dependencies within scope or identify pending updates.
- Use documentation-appropriate tools to check Markdown, relative links, and bilingual pairing.
- Report changes, decisions, open questions, and actual validation/review status.

## Open questions

- The publication destination and method are undecided; this does not block maintaining drafts in the repository.
