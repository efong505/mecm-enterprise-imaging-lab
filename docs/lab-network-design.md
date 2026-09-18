# Lab Network Design

## Purpose

This document defines the planned network topology, role placement, naming strategy, and isolation boundaries for the MECM Enterprise Imaging Lab.

It is a lab design artifact, not a production network design.

## Design Principles

- Keep the environment isolated from production and employer systems.
- Use lab-only names, addresses, and credentials.
- Avoid publishing sensitive or private infrastructure details.
- Document assumptions before implementation.
- Record planned and implemented state separately.
- Validate network dependencies before enabling PXE or deployment workflows.

## Planned Logical Topology

| System | Planned Role | Status |
|---|---|---|
| DC01 | Domain Controller / DNS | Planned |
| CM01 | MECM Primary Site Server | Planned |
| SQL01 | SQL Server, if separated from CM01 | Planned / design decision pending |
| DP01 | Distribution Point / PXE | Planned / placement decision pending |
| WINCLIENT01 | Test Client | Planned |

## Network Design Record

Complete during Phase 01 / Phase 02:

| Item | Decision / Value | Status |
|---|---|---|
| Lab network / virtual switch |  | Pending |
| Lab-only domain |  | Pending |
| IP address range |  | Pending |
| Subnet mask / prefix |  | Pending |
| Default gateway strategy |  | Pending |
| DNS server strategy |  | Pending |
| DHCP strategy |  | Pending |
| PXE boot path |  | Pending |
| Internet access strategy |  | Pending |
| Isolation controls |  | Pending |

## PXE / Deployment Considerations

Before PXE implementation, document:

- which component provides DHCP;
- whether client and distribution point share a broadcast domain;
- how PXE traffic reaches the intended distribution point;
- firmware mode used by the test client;
- boot-image availability;
- boundary and boundary-group assumptions.

## Diagram

Architecture and network diagrams belong in `/diagrams`.

A diagram should be labeled `Planned`, `Draft`, or `Implemented` and should not imply deployment evidence that does not exist.

## Open Design Decisions

- SQL Server colocated with CM01 or separated?
- Distribution Point colocated with CM01 or separated?
- DHCP location and scope?
- PXE traffic path?
- Test-client operating-system version(s)?
- Required Internet access and egress restrictions?

## Current Status

**Status: Planned — topology values and role-placement decisions remain to be validated.**
