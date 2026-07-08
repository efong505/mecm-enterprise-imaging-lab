# Lab Requirements

## Purpose

This document captures the expected requirements for the MECM Enterprise Imaging Lab before implementation begins.

The purpose is to help the learner think through the required systems, roles, resources, and assumptions without committing secrets or pretending that infrastructure has already been configured.

## Core Requirements to Identify

Document the following before starting the build:

- Virtualization platform to be used for the lab
- Number of virtual machines planned
- Operating system versions planned for each server and client
- Domain name strategy for the isolated lab
- IP addressing approach
- DNS approach
- Storage capacity available
- Memory and CPU available
- Internet access requirements
- ISO or installation media sources
- MECM / Configuration Manager Current Branch installation media source
- SQL Server installation media source
- Windows ADK and WinPE add-on requirements

## Suggested Server Roles

A basic learning lab may include:

| Role | Notes |
|---|---|
| Domain Controller | Provides AD DS and DNS for the practice domain. |
| MECM Site Server | Hosts the MECM primary site role for the lab. |
| SQL Server | Hosts the site database, either colocated or separate depending on design. |
| Distribution Point | Provides content distribution and imaging support. |
| Test Client | Receives the MECM client and later OS deployment testing. |

## Readiness Questions

Before starting implementation, answer:

1. Is the lab isolated from production systems?
2. Are all names, addresses, and credentials lab-only?
3. Is there enough compute capacity for all planned VMs?
4. Is the learner documenting assumptions before making changes?
5. Has the lab owner identified where screenshots and notes will be stored?

## Status

This file is a starter planning document. Fill it in as the lab design becomes more specific.
