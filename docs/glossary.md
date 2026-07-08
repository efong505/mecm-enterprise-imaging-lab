# Glossary

## Purpose

This glossary defines common terms used throughout the MECM Enterprise Imaging Lab.

The goal is to help the learner build vocabulary while moving through the lab phases. Definitions should stay practical, plain-language, and tied to the lab context.

## Terms

### MECM / Configuration Manager Current Branch

Microsoft Endpoint Configuration Manager, also known as Configuration Manager Current Branch, is an enterprise management platform used for endpoint management, software deployment, patching, inventory, compliance settings, and operating system deployment.

### Site Server

The main server that hosts Configuration Manager site roles and coordinates management activity for the lab environment.

### Primary Site

A Configuration Manager site that manages clients directly. In this lab, the primary site is the main learning environment.

### Site Database

The SQL Server database used by Configuration Manager to store site data, client data, inventory, configuration, deployment information, and status.

### Distribution Point

A site system role that stores content for clients, such as applications, packages, boot images, operating system images, and task sequence content.

### PXE

Preboot Execution Environment. PXE allows a client to start from the network and contact deployment infrastructure before a local operating system loads.

### Boot Image

A Windows PE image used to start the deployment environment for operating system deployment.

### Operating System Image

A Windows image, often a WIM file, used as the base operating system source for deployment.

### Task Sequence

A structured set of steps used by Configuration Manager to deploy or configure an operating system, install applications, apply drivers, and perform post-install actions.

### Client Agent

The Configuration Manager software installed on a managed endpoint. It allows the client to receive policy, report inventory, install software, and report health.

### Boundary

A network location definition used by Configuration Manager to associate clients with site resources such as distribution points.

### Boundary Group

A collection of boundaries used to organize client assignment and content location behavior.

### Content Distribution

The process of sending deployment content from the site server or content source to distribution points.

### Discovery

The process Configuration Manager uses to locate resources such as users, groups, systems, or network locations.

### Collection

A logical grouping of resources such as devices or users. Collections are commonly used to target deployments.

### Deployment

An instruction that makes software, updates, task sequences, or settings available or required for a target collection.

### Log File

A text-based record used to troubleshoot Configuration Manager components and client actions. Logs are central to MECM troubleshooting.
