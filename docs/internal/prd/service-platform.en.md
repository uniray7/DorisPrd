---
doc_id: PRD-PLATFORM
document_type: PRD
audience: Internal
status: Draft
revision: 0.1
reviewer: Requester
applies_to: OLAP Service / Data Ingestion Pipeline; version TBD
language: en
---

# Overall service PRD

[繁體中文](service-platform.zh-TW.md) · [Internal documentation](../README.en.md)

> Lightweight skeleton. `service-platform` is not the official product name; the background below is not a complete specification or release commitment.

## Background and problem

Confirmed direction: provide an Apache Doris-based OLAP Service and Data Ingestion Pipeline internally for other company departments. Specific problems and current pain points remain to be documented.

## Users and core scenarios

Known audience/user groups are service consumers in other departments and the internal team. Roles, core workflows, and priority scenarios are unresolved.

## Goals, scope, and non-goals

- Product scope includes OLAP, Data Ingestion, and internal/external monitoring and logs.
- External monitoring/logs primarily support investigation and troubleshooting, with some information masked or withheld; detailed policy is undecided.
- Existing Pipeline designs are approved and implementation is close to completion; they serve as the documentation baseline. Confidential originals are absent from this repository and detailed requirements remain blank.
- Product non-goals, initial scope, and success criteria are undecided. Excluding operational documents from this repository does not mean the product requires no operations.

## Requirements and priorities

TBD: record requirements with stable IDs, rationale, priority, state, and related Feature Specs. No detailed feature commitments have been established.

## Known design constraints

- Doris candidates are 4.1.0 or 4.1.4; selection is pending and release status/compatibility are unverified.
- The deployment design uses a self-managed bare-metal Nomad cluster with Consul and Vault; FE/BE run as Docker containers on Nomad agents' Docker daemons.
- Detailed topology, resource allocation, and integrations belong in [deployment topology](../architecture/deployment-topology.en.md).

## Success and acceptance criteria

TBD: product success measures, measurement methods, and initial acceptance scope. Do not invent SLAs/SLOs or performance values.

## Future direction

Consumer metrics access may enable integration with consumer-managed alerts. Capabilities, interfaces, and timing are uncommitted; this does not imply managed alerting by the service.

## Open questions

- Which departments/roles and problems take priority? This determines initial scenarios and priorities.
- Are OLAP, Ingestion, and monitoring/log access requested together or separately? This determines product and application boundaries.
- What is included in the initial release and explicitly excluded? This determines Feature Specs and external commitments.
- What establishes initial success and readiness for consumer access? This determines acceptance and Service Specs.

## Sources and related documents

Source: requester confirmation in the current product-background and documentation-structure discussion, not external technical validation. Pipeline documents have not been reviewed.

- [Internal documentation index](../README.en.md)
- [Documentation-organization decisions](../../../README.en.md)
