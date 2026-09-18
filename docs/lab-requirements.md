# Lab Requirements

## Purpose

This document defines the infrastructure, software, media, and documentation prerequisites that must be resolved before MECM implementation begins.

Requirements may remain `Pending` until verified. A requirement must not be marked satisfied without corresponding evidence.

## Infrastructure Requirements

Document and verify:

- virtualization platform;
- available CPU and memory capacity;
- available storage capacity;
- planned virtual-machine count;
- isolated lab network or virtual switch;
- IP addressing approach;
- DNS strategy;
- DHCP strategy where applicable;
- controlled Internet access requirements.

## Server and Client Roles

A representative topology may include:

| Role | Purpose | Status |
|---|---|---|
| Domain Controller | AD DS and DNS for the isolated lab domain | Planned |
| MECM Primary Site Server | Configuration Manager primary site | Planned |
| SQL Server | Site database; colocated or separate based on final design | Planned |
| Distribution Point | Content distribution and PXE / OSD support | Planned |
| Test Client | MECM client, imaging, deployment, and troubleshooting validation | Planned |

## Software and Media Requirements

Identify the source and intended version for:

- supported Windows Server media;
- supported Windows client media;
- Configuration Manager Current Branch installation media;
- SQL Server media;
- Windows ADK;
- Windows PE add-on;
- required Windows features / roles;
- any supporting tools used for logging, validation, or evidence capture.

Version-specific decisions should be verified against current Microsoft documentation before implementation.

## Security and Isolation Requirements

Before build work begins:

1. The lab must be isolated from employer or production systems.
2. Names, addresses, and credentials must be lab-only.
3. No production secrets or real user data may be introduced.
4. Screenshots must be reviewed before publication.
5. Evidence must show only the controlled lab environment.

## Readiness Gate

Phase 02 should not be considered complete until:

- topology is documented;
- compute/storage capacity is confirmed;
- server/client operating-system choices are recorded;
- required media sources are identified;
- AD/DNS/SQL/network assumptions are documented;
- unresolved blockers are explicitly listed.

## Current Status

**Status: Planned — requirements not yet fully validated.**
