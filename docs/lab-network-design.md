# Lab Network Design

## Purpose

This document is used to plan the lab network before any MECM implementation work begins.

The goal is to describe the practice topology clearly enough that another learner could understand the intended layout, server roles, naming approach, and isolation boundaries.

This is not a production network design document.

## Design Principles

Use these principles when documenting the lab:

- Keep the lab isolated from production systems.
- Use lab-only names, addresses, and credentials.
- Avoid publishing private environment details.
- Document assumptions before implementation begins.
- Mark anything uncertain as pending instead of pretending it is complete.

## Suggested Logical Topology

A simple MECM imaging lab may include:

| System | Example Role | Notes |
|---|---|---|
| DC01 | Domain Controller / DNS | Provides the practice Active Directory domain and name resolution. |
| CM01 | MECM Primary Site Server | Hosts Configuration Manager site roles used for the lab. |
| SQL01 | SQL Server | Hosts the MECM site database if separated from CM01. |
| DP01 | Distribution Point / PXE | Stores deployment content and supports imaging scenarios. |
| WINCLIENT01 | Test Client | Used for client installation and deployment testing. |

## Network Items to Document

Fill in the following during planning:

- Lab network name
- Lab-only domain name
- IP address range
- Subnet mask
- Default gateway strategy
- DNS server strategy
- DHCP strategy
- PXE boot strategy
- Internet access strategy
- VM switch or virtual network name
- Any isolation controls

## Diagram Placeholder

Network diagrams should be stored in `/diagrams`.

Do not add fake diagrams or screenshots. Add diagrams only when the design has been drafted or implemented.

## Open Questions

Use this section to capture design questions that must be answered before proceeding.

- Will SQL Server be colocated with the MECM server or separated?
- Will the distribution point be colocated or separated?
- Will DHCP be handled by the domain controller, router, or another lab system?
- How will PXE traffic reach the distribution point?
- What client operating systems will be tested?
