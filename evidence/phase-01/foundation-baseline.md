# Phase 01 Foundation Baseline

**Date:** 2026-09-18  
**Phase:** 01 — Foundation  
**Evidence class:** Planning / architecture baseline

## Goal

Establish the controlled lab scope, planned role model, isolation requirements, documentation structure, and evidence rules before infrastructure implementation.

## Work Performed

- employer-facing repository structure reviewed and cleaned;
- lab purpose and evidence boundaries documented;
- planned server-role model established;
- network-design baseline established;
- infrastructure and software requirement categories established;
- Phase 01 topology diagram created;
- phase checkpoint prepared;
- unresolved detailed design decisions explicitly carried into Phase 02.

## Confirmed Foundation Decisions

- This is a controlled lab / production-like practice environment.
- It does not represent professional production MECM ownership.
- Employer and production environments are out of scope.
- Lab-only names, addresses, and credentials are required.
- Real employer/customer data is prohibited.
- Fabricated screenshots or validation results are prohibited.
- Required logical roles are DC/DNS, MECM primary site, SQL capability, DP/PXE capability, and a test client.

## Open Decisions

The following are intentionally unresolved and must be validated in Phase 02:

- virtualization platform;
- compute and storage capacity;
- Windows Server version;
- Windows client version;
- SQL Server version and placement;
- Configuration Manager Current Branch version;
- Windows ADK / WinPE versions;
- lab domain name;
- CIDR / subnet;
- DHCP design;
- DP placement;
- Internet egress approach.

## Result

Phase 01 foundation requirements are satisfied. Detailed infrastructure prerequisite validation is the next controlled step.

No VM, server role, SQL instance, MECM site, DP/PXE service, or client build is claimed by this record.
