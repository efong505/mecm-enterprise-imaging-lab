# Phase 01 — Foundation

## Status

**Complete — Foundation Baseline Established**

## Objective

Establish the controlled MECM lab scope, topology baseline, documentation model, and evidence requirements before any server build or configuration work begins.

## Completed Work

- reviewed and established the employer-facing repository structure;
- defined the lab scope and evidence classification;
- established the planned server-role model;
- established production/employer isolation as a hard boundary;
- documented the initial network topology and open design decisions;
- documented infrastructure and software requirement categories;
- established evidence templates, runbooks, and checkpoint controls;
- created a Phase 01 evidence baseline and planned topology artifact.

## Phase 01 Baseline

Required roles:

- DC01 — Active Directory Domain Services / DNS
- CM01 — MECM Primary Site Server
- SQL capability — required; placement pending
- Distribution Point / PXE capability — required; placement pending
- WINCLIENT01 — controlled test client

Detailed values such as virtualization platform, CIDR, DHCP, OS versions, SQL placement, DP placement, and software-media versions are intentionally carried into Phase 02.

## Validation Criteria

| Criterion | Result |
|---|---|
| Lab scope documented | Met |
| Planned server roles identified | Met |
| Network and isolation assumptions recorded | Met |
| Infrastructure requirement categories listed | Met |
| Open questions explicit | Met |
| Evidence / checkpoint model established | Met |
| Server installation performed | Not applicable to Phase 01 |

## Evidence

- `docs/lab-overview.md`
- `docs/lab-network-design.md`
- `docs/lab-requirements.md`
- `diagrams/phase-01-planned-topology.md`
- `evidence/phase-01/foundation-baseline.md`
- `checkpoints/phase-01-foundation-checkpoint.md`

## Exit Decision

**Phase 01 COMPLETE.**

Phase 02 may begin prerequisite validation and detailed design resolution. No server installation or MECM implementation is authorized by Phase 01 completion alone.

## Boundaries

This phase does not claim that any VM, Windows Server role, SQL instance, MECM site, DP, PXE service, or client has been built. Those remain future implementation evidence.
