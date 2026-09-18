# MECM Enterprise Imaging Lab

Enterprise-style Microsoft Endpoint Configuration Manager (MECM / Configuration Manager Current Branch) lab focused on Windows endpoint deployment, Active Directory and DNS dependencies, SQL Server planning, distribution infrastructure, PXE, operating system deployment, task sequences, client management, and log-driven troubleshooting.

The project is organized as a controlled lab with repeatable implementation phases, validation checkpoints, troubleshooting runbooks, and evidence capture. It is intended to build current hands-on familiarity with MECM architecture and operations without representing lab work as employer production ownership.

## Current Lab Status

**Evidence classification:** Hands-on learning lab / production-like practice environment.

The repository currently contains the lab architecture, implementation phases, runbooks, templates, checkpoints, and supporting documentation needed to build and validate the environment.

Full tutorials, screenshots, command output, configuration evidence, and validation results should be added only after the corresponding work has actually been performed.

This repository does **not** represent professional production MECM administration experience.

## Lab Objectives

The lab is structured to develop and document practical understanding of:

- MECM / Configuration Manager Current Branch fundamentals
- enterprise endpoint-management architecture
- Active Directory Domain Services and DNS dependencies
- SQL Server planning for a primary site
- MECM prerequisite validation
- site installation concepts
- distribution point and PXE infrastructure
- boot images and operating system images
- packages, applications, and drivers
- task-sequence design and deployment testing
- MECM client installation, discovery, inventory, and health
- log-driven troubleshooting
- repeatable implementation and operational documentation

## Architecture Overview

A representative lab topology includes:

| Component | Purpose |
|---|---|
| Domain Controller | Provides Active Directory Domain Services and DNS for the lab |
| MECM Primary Site Server | Hosts the Configuration Manager primary site role |
| SQL Server | Hosts the MECM site database; may be colocated or separated depending on lab design |
| Distribution Point | Stores deployment content and supports PXE / operating-system deployment workflows |
| Test Client VM | Used for client installation, inventory, deployment, imaging, and troubleshooting tests |
| Optional NAT / Router VM | Provides isolated routing or controlled external connectivity when required |

The authoritative network and dependency design belongs in:

`docs/lab-network-design.md`

A simplified logical flow is:

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

## Technical Areas Covered

### Enterprise Infrastructure

- Active Directory and DNS dependencies
- Windows Server roles and service relationships
- SQL Server planning
- network and service prerequisites
- role separation and dependency mapping

### Endpoint Deployment

- MECM site architecture
- distribution points
- PXE
- boot images
- operating-system images
- task sequences
- application/package deployment concepts
- client discovery and management

### Troubleshooting and Operations

- symptom capture
- log selection and interpretation
- dependency validation
- content-distribution checks
- PXE troubleshooting
- client-health checks
- repeatable troubleshooting records
- change and checkpoint documentation

## What This Repository Demonstrates Today

The current repository demonstrates:

- structured enterprise infrastructure planning;
- dependency analysis across MECM, AD, DNS, SQL, networking, and clients;
- phased implementation design;
- troubleshooting workflow design;
- operational runbook structure;
- validation/checkpoint discipline;
- evidence-integrity controls that distinguish performed work from planned work.

As the lab is executed, additional hands-on evidence can be added, including screenshots, configuration notes, command output, troubleshooting records, and validated phase results.

## Implementation Phases

The lab is organized into seven implementation phases:

1. **Foundation** — define scope, topology, boundaries, and required systems.
2. **Server Prerequisites** — validate operating-system, AD/DNS, SQL, network, and service prerequisites.
3. **MECM Installation** — prepare and document primary-site installation.
4. **Imaging Infrastructure** — configure and validate distribution-point, PXE, boot-image, and content concepts.
5. **Task Sequence** — build the operating-system deployment workflow and supporting content.
6. **Test Deployment** — validate behavior against a controlled test client and capture troubleshooting evidence.
7. **Enterprise Concepts** — connect the lab implementation to broader enterprise scale, reliability, and operational considerations.

Phase documents are stored under:

`/phases`

## Operational Documentation

The repository includes:

- `/docs` — architecture, glossary, requirements, and lab design
- `/phases` — implementation work packages
- `/runbooks` — client, content-distribution, log, and PXE troubleshooting references
- `/templates` — lab notes, change logs, screenshots, and troubleshooting records
- `/checkpoints` — phase-completion validation

These artifacts are intended to make the lab repeatable and auditable rather than a one-time installation exercise.

## Evidence and Safety Boundaries

This repository is for learning and controlled practice.

It should not be treated as:

- professional production MECM ownership;
- a hardened production implementation guide;
- a compliance baseline;
- a security baseline;
- or a replacement for current Microsoft documentation.

Do not commit:

- passwords or secrets;
- license keys;
- tenant IDs;
- private domain names;
- production hostnames;
- customer or employer data;
- real user data;
- internal organization details;
- fabricated screenshots;
- invented validation results.

Screenshots, command output, configuration evidence, and validation notes should only be committed after the corresponding lab step has actually been performed.

## What This Demonstrates to an Employer

This project is intended to show how I approach enterprise infrastructure work:

- break a complex platform into dependencies and implementation phases;
- document architecture before making changes;
- validate prerequisites before installation;
- use repeatable runbooks and checkpoints;
- troubleshoot from evidence rather than assumption;
- distinguish planning from verified implementation;
- preserve operational and security boundaries.

As hands-on execution progresses, the repository will increasingly serve as current lab evidence for MECM, Windows infrastructure, deployment systems, and troubleshooting.

## How to Review This Repository

For a technical review, start with:

1. `README.md`
2. `docs/lab-overview.md`
3. `docs/lab-network-design.md`
4. `phases/phase-01-foundation.md`
5. `runbooks/pxe-troubleshooting.md`
6. `runbooks/client-health-checks.md`

Then review later phase artifacts and evidence as they are completed.
