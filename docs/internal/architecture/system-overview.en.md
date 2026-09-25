---
doc_id: ARCH-SYSTEM
document_type: System Architecture
audience: Internal
status: Draft
revision: 0.1
reviewer: Requester
applies_to: OLAP Service / Data Ingestion Pipeline; version TBD
language: en
---

# System architecture overview

[繁體中文](system-overview.zh-TW.md) · [Internal documentation](../README.en.md)

> Lightweight skeleton; a complete architecture diagram is deferred to avoid inferring undecided components or paths.

## Purpose and boundaries

See the [overall PRD](../prd/service-platform.en.md) for known direction. TBD: consumer entry points, service responsibilities, and external-system boundaries.

## Components and interfaces

Known foundations are Apache Doris FE/BE and the deployment design using Nomad, Consul, and Vault. TBD: component responsibilities, interfaces, and actual integration; do not infer functions from tool names.

## Diagrams and responsibilities

Add diagrams with content-state labels after interactions and deployment boundaries are confirmed. Leave Pipeline internals blank; ask only for necessary interfaces when cross-service connections are needed.

## Failure boundaries and design decisions

TBD: decided dependency-failure impacts, isolation, and availability design. Describe design here, not operational Runbooks.

## Open questions

- Where do consumers enter each service, and which components enforce access? This determines interface/responsibility diagrams.
- What does each component and external dependency own? This determines failure boundaries.
- Which availability/isolation requirements are decided? This determines architecture options and RFCs.

## Dependencies and sources

Source: requester-confirmed product/deployment background, not actual deployment validation.

- [Deployment topology](deployment-topology.en.md)
- [Observability Architecture](observability.en.md)
- [OLAP Query Flow](../data-flows/olap-query.en.md)
