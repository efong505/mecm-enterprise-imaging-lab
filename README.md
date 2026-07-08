# MECM Enterprise Imaging Lab

## Purpose

This repository is a guided practice lab for learning Microsoft Endpoint Configuration Manager / Configuration Manager Current Branch in an enterprise imaging and endpoint management context.

The lab is designed around a Multi-Agent System (MAS) learning model. Instead of trying to write one large tutorial all at once, the repository separates planning, prerequisites, installation, imaging infrastructure, client management, troubleshooting, and documentation into focused agent files and phase files.

This repository is a learning lab. It is not production documentation.

## What This Lab Teaches

This lab is intended to help a learner understand how MECM is used in an enterprise-style imaging and endpoint management environment.

The lab will eventually walk through concepts such as:

- MECM / Configuration Manager Current Branch fundamentals
- How MECM differs from smaller MDT-style deployment workflows
- Lab topology planning for a domain-based endpoint management environment
- Active Directory and DNS dependencies
- SQL Server planning for a primary site
- MECM server prerequisite validation
- Site installation concepts
- Distribution point and PXE imaging concepts
- Boot images, operating system images, packages, applications, and drivers
- Task sequence planning and test deployments
- Client installation, discovery, inventory, and health validation
- Log-driven troubleshooting
- Documentation discipline for a repeatable lab build

## Lab Disclaimer

This repository is for learning and practice only.

It should not be treated as a hardened production implementation guide, a compliance document, a security baseline, or a replacement for official Microsoft documentation.

Do not commit:

- Passwords
- Secrets
- License keys
- Tenant IDs
- Private domain names
- Production hostnames
- Customer data
- Real user data
- Internal organization details
- Fake screenshots
- Invented lab results

Screenshots, configuration evidence, and validation notes should only be added after the lab step has actually been performed.

## MAS Agent Model Overview

The MAS model breaks the lab into focused responsibilities. Each agent acts like a specialized guide for one part of the implementation path.

| Agent | Role in the Lab |
|---|---|
| MECM Tutorial Agent | Main guide that keeps the learner moving through the lab in order. |
| Lab Architecture Agent | Defines lab boundaries, topology, server roles, and network assumptions. |
| Prerequisite Validation Agent | Confirms readiness before installation or phase transitions. |
| AD/DNS Agent | Guides identity, domain, DNS, and service dependency planning. |
| SQL Server Agent | Guides SQL Server planning, installation assumptions, and validation checkpoints. |
| MECM Installation Agent | Guides MECM setup preparation and installation documentation. |
| Distribution Point / PXE Agent | Guides content distribution, PXE, boot image, and network boot concepts. |
| OS Deployment Agent | Guides operating system image and task sequence learning. |
| Client Management Agent | Guides client installation, discovery, inventory, and health validation. |
| Troubleshooting Agent | Helps isolate problems using logs, symptoms, and repeatable checks. |
| Documentation Agent | Keeps notes, diagrams, screenshots, runbooks, and checkpoint records organized. |

## Suggested Lab Topology

A basic learning topology may include the following roles:

| Role | Example Purpose |
|---|---|
| Domain Controller | Provides Active Directory Domain Services and DNS for the lab. |
| MECM Primary Site Server | Hosts the MECM site server role for the practice environment. |
| SQL Server | Hosts the site database. This may be colocated or separated depending on the lab design. |
| Distribution Point | Stores deployment content and supports PXE imaging concepts. |
| Test Client VM | Used for MECM client testing and imaging deployment practice. |
| Optional NAT / Router VM | Provides isolated lab network routing if needed. |

The final topology should be documented in `docs/lab-network-design.md` before implementation begins.

## Phase List

The lab is organized into seven starter phases:

1. `phase-01-foundation.md` — define scope, topology, and lab boundaries.
2. `phase-02-server-prerequisites.md` — validate server prerequisites before MECM setup.
3. `phase-03-mecm-installation.md` — document the MECM installation path.
4. `phase-04-imaging-infrastructure.md` — prepare distribution point, PXE, and imaging concepts.
5. `phase-05-task-sequence.md` — plan and build the task sequence learning path.
6. `phase-06-test-deployment.md` — validate deployment behavior with a test client.
7. `phase-07-enterprise-concepts.md` — connect the lab to enterprise-scale concepts.

## How to Use This Repository

Start by reading the documents in `/docs`, then move through the `/phases` folder in order.

Use the `/agents` folder to decide which specialized guide should help with each phase. Use `/templates` to capture notes, change records, troubleshooting entries, and screenshot checklists. Use `/runbooks` when validating logs, PXE, client health, or content distribution. Use `/checkpoints` before declaring a phase complete.

This repository begins as a scaffold. Full tutorials, screenshots, lab results, and implementation evidence should be added only as the lab is actually built.
