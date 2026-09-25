---
doc_id: GOV-GLOSSARY
document_type: Glossary
audience: Contributors
status: Draft
revision: 0.1
reviewer: Requester
applies_to: Repository
language: en
---

# Shared glossary

[繁體中文](glossary.zh-TW.md)

## Documentation terms

| Term | Meaning in this repository |
| --- | --- |
| Internal | The team designing, implementing, and operating the services. |
| External | Service consumers in other company departments, not the public internet. |
| Requester | The user requesting work and making final documentation decisions, not automatically the service-application approver. |
| PRD | Product Requirements Document; defines why, for whom, and product scope. |
| Feature Spec | Defines detailed feature behavior, rules, and acceptance criteria. |
| RFC | Request for Comments; records design options, trade-offs, and decisions. |
| Service Spec | Describes consumer capabilities, limits, and approved commitments. |
| TBD | To Be Determined; information or a decision is pending. |

## Service terms

| Term | Usage in this repository |
| --- | --- |
| OLAP | Online Analytical Processing; this service is based on Apache Doris. |
| Data Ingestion Pipeline | The product's ingestion component; detailed documentation is currently blank. |
| FE / BE | Apache Doris Frontend / Backend component names; this glossary does not define counts or topology. |
| Monitoring | Capabilities for consumers or the team to observe service/workload state; details are undecided. |
| Logs | Records used for investigation and troubleshooting; visibility and masking rules are undecided. |
| Metrics | Measurements for analysis and integration; consumer access remains a possible future direction. |
| Alerting | Alert generation/delivery; future consumer integration with metrics does not imply managed alerting by the service. |

## Open questions

- Add official product, user-role, and resource-scope names after PRD/Feature Spec decisions.
- Sources are the current requester discussion and documentation conventions, not evidence of version-specific Doris behavior.
