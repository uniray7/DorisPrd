---
doc_id: ARCH-DEPLOYMENT
document_type: System Architecture
audience: Internal
status: Draft
revision: 0.1
reviewer: Requester
applies_to: Apache Doris / Nomad / Consul / Vault; versions TBD
language: en
---

# Deployment topology

[繁體中文](deployment-topology.zh-TW.md) · [Internal documentation](../README.en.md)

> Lightweight skeleton describing deployment design, not procedures or verified environment configuration.

## Confirmed deployment direction

Source: requester confirmation. Self-managed bare-metal machines host a HashiCorp Nomad cluster with Consul and Vault. Doris FE/BE run as Docker containers on Nomad agents' Docker daemons.

Doris candidates are 4.1.0 or 4.1.4; selection is pending and release/compatibility are unverified. Other component versions have not been provided.

## Node allocation and scheduling

TBD: roles, node counts, resources, failure domains, placement, and colocation rules. Do not infer an HA topology.

## Networking, storage, and integrations

TBD: connectivity/discovery, container networking, persistent data/storage boundaries, and actual Consul/Vault responsibilities and interfaces.

## Dependencies and design constraints

TBD: version compatibility, environment constraints, and decided failure impacts. Deployment, upgrade, and recovery Runbooks are excluded.

## Open questions

- How will Doris selection and compatibility be validated? This determines references and configuration.
- What are FE/BE node counts, resources, and scheduling boundaries? This determines topology and failure domains.
- How are persistent data and networking configured? This determines data/connection boundaries.
- Which workflows involve Consul and Vault? This determines actual component dependencies.

## Related documents and references

- [System overview](system-overview.en.md)
- [Reference policy](../../governance/reference-policy.en.md)

External version evidence and local validation records have not been added.
