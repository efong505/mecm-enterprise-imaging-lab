# Lab Network Design

## Purpose

This document defines the planned network topology, role placement, naming strategy, and isolation boundaries for the MECM Enterprise Imaging Lab.

It is a lab design artifact, not a production network design.

## Phase 01 Baseline

The Phase 01 foundation establishes the following planned role model:

| System | Planned Role | Phase 01 State |
|---|---|---|
| DC01 | Domain Controller / DNS | Required |
| CM01 | MECM Primary Site Server | Required |
| SQL01 | SQL Server | Placement decision pending Phase 02 |
| DP01 | Distribution Point / PXE | Placement decision pending Phase 02 |
| WINCLIENT01 | Test Client | Required |

The role names above are lab-only placeholders and may change before implementation.

## Design Principles

- Keep the environment isolated from production and employer systems.
- Use lab-only names, addresses, and credentials.
- Avoid publishing sensitive or private infrastructure details.
- Document assumptions before implementation.
- Record planned and implemented state separately.
- Validate network dependencies before enabling PXE or deployment workflows.

## Network Design Record

| Item | Phase 01 Decision / Value | Status |
|---|---|---|
| Virtualization platform | Not yet selected / recorded | Pending Phase 02 |
| Lab network / virtual switch | Dedicated lab-only network required | Defined principle; implementation pending |
| Lab-only domain | Lab-only namespace required | Naming pending Phase 02 |
| IP address range | Private lab range required | CIDR pending Phase 02 |
| Subnet mask / prefix | Derived from selected lab CIDR | Pending Phase 02 |
| Default gateway strategy | Controlled lab routing only | Implementation pending |
| DNS server strategy | DC01 provides lab DNS | Baseline selected |
| DHCP strategy | To be selected based on lab topology | Pending Phase 02 |
| PXE boot path | Test client must reach intended DP/PXE service | Baseline requirement |
| Internet access strategy | Only as required for installation/update workflow | Pending Phase 02 |
| Isolation controls | No employer/production network dependency | Required |

## Planned Logical Flow

```text
                 Isolated Lab Network
                        |
                +-------+-------+
                |               |
              DC01            CM01
           AD DS / DNS          |
                                +---- SQL01 (placement pending)
                                |
                                +---- DP01 / PXE (placement pending)
                                         |
                                    WINCLIENT01
```

## PXE / Deployment Considerations

Before PXE implementation, Phase 02 must resolve:

- which component provides DHCP;
- whether the test client and DP share a broadcast domain;
- how PXE traffic reaches the intended DP;
- firmware mode used by the test client;
- boot-image availability;
- boundary and boundary-group assumptions.

## Open Design Decisions Carried to Phase 02

1. Virtualization platform.
2. SQL Server colocated with CM01 or separated.
3. Distribution Point colocated with CM01 or separated.
4. Lab domain name.
5. Lab CIDR / addressing plan.
6. DHCP location and scope.
7. Internet egress approach.
8. Test-client operating-system version.
9. Exact Windows Server / SQL / ConfigMgr / ADK versions.

## Current Status

**Phase 01 baseline established. Detailed infrastructure values remain intentionally pending for Phase 02 validation.**
