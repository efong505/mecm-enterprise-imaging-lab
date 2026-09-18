# Lab Overview

## Purpose

This document defines the scope, boundaries, and intended technical outcomes of the MECM Enterprise Imaging Lab.

The lab is designed to establish and validate hands-on familiarity with Microsoft Endpoint Configuration Manager / Configuration Manager Current Branch in an enterprise-style imaging and endpoint-management environment.

This document describes the planned environment before implementation. It must not imply that servers, services, task sequences, deployments, or validation results exist until they have actually been created and recorded.

## Technical Objectives

The completed lab should establish evidence of practical understanding in:

- MECM / Configuration Manager architecture and site roles
- Active Directory Domain Services and DNS dependencies
- SQL Server requirements for a primary site
- content distribution and distribution-point behavior
- PXE and Windows PE boot flow
- operating-system deployment and task sequences
- client installation, discovery, inventory, and health
- log-driven troubleshooting
- phase validation, evidence capture, and repeatable documentation

## Project Context

This is a controlled lab / production-like practice environment intended to complement existing systems-administration experience with current MECM hands-on evidence.

It is not presented as professional production MECM ownership.

## Boundaries

The lab must not include:

- production secrets or credentials;
- employer or customer data;
- private production hostnames or network details;
- real tenant information;
- fabricated screenshots;
- invented validation results;
- unperformed work presented as complete.

When a step has not been executed, its state must remain `Planned`, `Pending`, `Not Started`, or another accurate status.

## Documentation Model

Detailed implementation and validation work belongs in:

- `docs/` for architecture and requirements;
- `phases/` for implementation work packages;
- `runbooks/` for repeatable operational checks and troubleshooting;
- `templates/` for evidence capture;
- `checkpoints/` for phase-completion decisions;
- `diagrams/` for architecture and flow diagrams.

This file should remain the high-level technical scope document.
