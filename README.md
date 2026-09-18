# MECM Enterprise Imaging Lab

Enterprise-style Microsoft Configuration Manager Current Branch lab focused on Windows endpoint deployment, Active Directory and DNS dependencies, SQL Server planning, distribution infrastructure, PXE, task sequences, client management, and log-driven troubleshooting.

This is a controlled hands-on lab / production-like practice environment. It is intended to build current MECM implementation evidence without representing lab work as professional production MECM ownership.

## Current Status

**Phase 01 — Foundation:** complete. **Next:** Phase 02 — Server Prerequisites.

The repository contains the architecture baseline, implementation work packages, runbooks, evidence templates, checkpoints, and supporting documentation required to build and validate the environment. Implementation evidence is added only after the corresponding work is actually performed.

## Architecture Overview

| Component | Purpose |
|---|---|
| Domain Controller | Active Directory Domain Services and DNS |
| MECM Primary Site Server | Configuration Manager primary site |
| SQL Server | MECM site database; final placement remains a design decision |
| Distribution Point / PXE | Deployment content and network-boot support |
| Test Client VM | Client, imaging, deployment, and troubleshooting validation |

```text
Active Directory / DNS
        |
        +----------------------+
        |                      |
 MECM Primary Site -------- SQL Server
        |
 Distribution Point / PXE
        |
   Test Client VM
```

The authoritative topology and open design decisions are tracked in `docs/lab-network-design.md`.

## Technical Scope

- Active Directory and DNS dependencies
- Windows Server and SQL Server prerequisites
- Configuration Manager site architecture
- distribution points and content distribution
- PXE and boot images
- operating-system deployment and task sequences
- client discovery, inventory, policy, and health
- log-driven troubleshooting
- evidence capture, validation, and repeatable runbooks

## Implementation Phases

1. **Foundation** — scope, topology, boundaries, requirements, and evidence model
2. **Server Prerequisites** — OS, AD/DNS, SQL, network, media, and service readiness
3. **MECM Installation** — primary-site installation and post-install validation
4. **Imaging Infrastructure** — Distribution Point, PXE, boot images, and content
5. **Task Sequence** — controlled OSD task-sequence design
6. **Test Deployment** — real client deployment and troubleshooting evidence
7. **Enterprise Concepts** — compare validated lab evidence with enterprise-scale considerations

## Evidence Boundary

This repository distinguishes:

- **planned design**
- **executed lab work**
- **validated evidence**
- **enterprise-scale concepts**

It does not claim professional production MECM ownership. Do not commit secrets, production hostnames, employer/customer data, real user data, fabricated screenshots, or invented validation results.

## Technical Review Path

Start with:

1. `docs/lab-overview.md`
2. `docs/lab-network-design.md`
3. `docs/lab-requirements.md`
4. `phases/phase-01-foundation.md`
5. `runbooks/pxe-troubleshooting.md`
6. `runbooks/client-health-checks.md`

As phases are executed, review the corresponding evidence and checkpoint artifacts.
