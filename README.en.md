---
doc_id: DOC-ROOT
document_type: Index
audience: Contributors
status: Draft
revision: 0.1
reviewer: Requester
applies_to: Repository
language: en
---

# OLAP Service and Data Ingestion Pipeline documentation

[繁體中文](README.zh-TW.md)

This repository documents the company-internal Apache Doris-based OLAP Service and Data Ingestion Pipeline.

## Entry points

- [External documentation](docs/external/README.en.md): service specifications, application, approval, usage, and troubleshooting for consumers in other departments.
- [Internal documentation](docs/internal/README.en.md): the overall PRD, Feature Specs, RFCs, Architecture, and Data Flows for the team.
- [Authoring workflow](docs/governance/authoring-workflow.en.md), [reference policy](docs/governance/reference-policy.en.md), and [glossary](docs/governance/glossary.en.md).
- [OpenCode skill](.opencode/skills/service-documentation/SKILL.md): entry point for AI-assisted documentation.

## Directory map

```text
docs/
├── governance/                 Workflow, reference policy, and terminology
├── external/
│   ├── service-specs/          Consumer capabilities and service limits
│   ├── getting-started/        Application, approval, and first use
│   ├── user-guides/            OLAP, monitoring, and log usage
│   ├── policies/              Usage policies
│   └── support/               Troubleshooting
└── internal/
    ├── prd/                   One overall PRD
    ├── feature-specs/         Feature behavior and acceptance
    ├── rfcs/                  Design decisions and trade-offs
    ├── architecture/          System and deployment design
    └── data-flows/            Data paths and behavior
```

## Status and maintenance

- The requester has confirmed the directory structure; individual documents are currently `Draft`. Skeletons do not establish approved specifications, verified implementation, or released capabilities.
- Maintain `.zh-TW.md` / `.en.md` pairs with matching document IDs, revisions, and status. Traditional Chinese prose retains English technical terms.
- Use one overall PRD. Operational Runbooks are outside this repository's scope.
- `external` means other departments in the company, not the public internet. Drafts in that directory are not published.
- The four reserved Pipeline directories contain only `.gitkeep`, without confidential originals or inferred content. Ask the requester for necessary, recordable details when another feature depends on them.
- Keep open questions with the relevant document; use RFCs for consequential cross-document design decisions.

## Confirmed documentation decisions

Source: requester confirmation during this documentation-structure discussion; reviewer: Requester. These are document-organization decisions, not product-specification approval.

| ID | Decision | Rationale / context |
| --- | --- | --- |
| DOC-DEC-001 | Organize by audience, then document purpose | Separate consumer documentation from team design documents. |
| DOC-DEC-002 | Use one overall PRD | The requester selected this PRD granularity. |
| DOC-DEC-003 | Exclude operational documentation | The requester confirmed the repository scope. |
| DOC-DEC-004 | Create bilingual lightweight skeletons; leave Pipeline blank | Make documentation gaps visible while respecting the confidential-document boundary. |

## Open questions and next steps

- The official product name is undecided; `service-platform` is only the overall PRD filename.
- Start with the [overall PRD](docs/internal/prd/service-platform.en.md) to clarify users, core scenarios, scope, and priorities, then develop the related specifications.
