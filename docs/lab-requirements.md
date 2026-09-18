# Lab Requirements

## Purpose

This document defines the infrastructure, software, media, and documentation prerequisites that must be resolved before MECM implementation begins.

Requirements may remain `Pending` until verified. A requirement must not be marked satisfied without corresponding evidence.

## Phase 01 Requirement Baseline

| Requirement | Phase 01 State |
|---|---|
| Isolated virtualization environment | Required; platform selection pending |
| Dedicated lab-only network | Required |
| Domain Controller / DNS | Required |
| MECM Primary Site Server | Required |
| SQL Server capability | Required; placement pending |
| Distribution Point / PXE capability | Required; placement pending |
| Test Windows client | Required |
| Evidence-capture structure | Established |
| Production/employer isolation | Required and controlling |
| Secrets / private data exclusion | Required and controlling |

## Infrastructure Requirements for Phase 02 Validation

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

## Software and Media Requirements

Identify the source and intended version for:

- supported Windows Server media;
- supported Windows client media;
- Configuration Manager Current Branch installation media;
- SQL Server media;
- Windows ADK;
- Windows PE add-on;
- required Windows features / roles;
- supporting tools used for logging, validation, and evidence capture.

Version-specific decisions must be verified against current Microsoft documentation before implementation.

## Security and Isolation Requirements

Before build work begins:

1. The lab must be isolated from employer or production systems.
2. Names, addresses, and credentials must be lab-only.
3. No production secrets or real user data may be introduced.
4. Screenshots must be reviewed before publication.
5. Evidence must show only the controlled lab environment.

## Phase 01 Result

The requirement categories and safety boundaries are established. Exact platform, capacity, addressing, software-version, and media decisions remain Phase 02 work.

## Current Status

**Phase 01 baseline complete — Phase 02 prerequisite validation required before implementation.**
