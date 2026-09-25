---
doc_id: FEAT-OLAP
document_type: Feature Spec
audience: Internal
status: Draft
revision: 0.1
reviewer: Requester
applies_to: OLAP Service; version TBD
language: en
---

# OLAP Service Feature Spec

[繁體中文](olap-service.zh-TW.md) · [Internal documentation](../README.en.md)

> Lightweight skeleton; the product is based on Apache Doris, while detailed service behavior remains undecided.

## Purpose, supported scope, and interfaces

TBD: scenarios, queries and other permitted operations, interfaces/clients, inputs/outputs, and explicit exclusions.

## Resource rules and execution behavior

TBD: resource scope, quotas, whether concurrency/timeout or other limits are needed, and enforcement. Values require decisions and applicable-version validation.

## Exceptions and visible outcomes

TBD: permission denial, exceeded limits, cancellation, failure, and retry semantics according to selected capabilities; do not infer support.

## Acceptance criteria

TBD: normal, boundary, and failure cases, plus validation methods for capabilities and limits.

## Open questions

- Which query and data operations are included initially? This determines feature boundaries and interfaces.
- At which scope do resource allocations and limits apply? This determines isolation, acceptance, and the Service Spec.
- How will the Doris version be selected? This determines feature and compatibility validation.
- What data visibility/freshness is required for queries? Ask the requester for necessary Pipeline details without inferring end-to-end guarantees.

## Dependencies and sources

- [Overall PRD](../prd/service-platform.en.md)
- [Access Control](access-control.en.md)
- [OLAP Query Flow](../data-flows/olap-query.en.md)
- Derived document: [OLAP Service Spec](../../external/service-specs/olap-service.en.md).

Known product direction comes from requester confirmation; technical capabilities and version evidence remain unverified.
