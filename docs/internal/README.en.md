---
doc_id: INT-INDEX
document_type: Index
audience: Internal
status: Draft
revision: 0.1
reviewer: Requester
applies_to: OLAP Service / Data Ingestion Pipeline; version TBD
language: en
---

# Team documentation

[繁體中文](README.zh-TW.md) · [Repository home](../../README.en.md)

This directory records requirements, feature rules, architecture, and design decisions as lightweight skeletons. It uses one overall PRD and excludes operational Runbooks.

## Requirements and specifications

- [Overall PRD](prd/service-platform.en.md): product goals, users, and service boundaries.
- [Application and approval](feature-specs/service-application-and-approval.en.md).
- [Access Control](feature-specs/access-control.en.md).
- [OLAP Service](feature-specs/olap-service.en.md).
- [Monitoring](feature-specs/monitoring.en.md).
- [Logging and information exposure](feature-specs/logging-and-information-exposure.en.md).

## Decisions, architecture, and data flows

- [RFC index](rfcs/README.en.md).
- [System overview](architecture/system-overview.en.md), [deployment topology](architecture/deployment-topology.en.md), and [Observability Architecture](architecture/observability.en.md).
- [OLAP Query Flow](data-flows/olap-query.en.md) and [Telemetry Flow](data-flows/telemetry.en.md).

## Pipeline boundary

Leave `feature-specs/data-ingestion/` and `data-flows/data-ingestion/` blank. Do not import existing confidential designs; ask the requester only for necessary, recordable dependency details.

## Open questions and reading order

Resolve product questions in the PRD first, then develop Feature Specs, RFCs, architecture, and flows according to dependencies. Each document's open questions guide subsequent discussions; fill external documentation after confirming specifications and availability.
