---
title: FlowIntel 1.3.1 released and MISP integration 
banner: /img/flowintel-case.png 
author:
 - MISP Project team
date: 2024-12-09
tags: ["MISP", "Threat Intelligence", "release", "case management", "FlowIntel"]
layout: post
---

# FlowIntel 1.3.1 released and MISP integration

[FlowIntel](https://github.com/flowintel/flowintel) is a lightweight and flexible platform built to help teams manage their tasks and cases efficiently. It offers a range of features, from detailed documentation tools to integration with external platforms, ensuring that workflows remain seamless and adaptable to various needs.

With this release, FlowIntel introduces robust integration with MISP, enabling the export of indicators and TTPs from FlowIntel to MISP. It also includes full support for all MISP taxonomies and galaxies, ensuring consistent labeling and categorization. Additionally, the integration with [MISP Modules](https://misp.github.io/misp-modules/expansion/) allows for extended capabilities through expansion modules.

## FlowIntel Main features

### Cases and tasks

A case in FlowIntel includes detailed notes, a history of all actions performed as well as a list of tasks. Tasks represent specific actions required to progress or resolve a case. These tasks may include subtasks as well as have users assigned to the individual (sub-)tasks. They also support multiple Markdown-based notes, and allow for file attachments. Notes within tasks can also be exported in either PDF or DOCX formats for documentation or reporting purposes.

#### Case view

![Case view in FlowIntel](/img/flowintel-case.png)

#### Task view

![Task view in FlowIntel](/img/flowintel-task.png)

### Template

A case and its tasks can be converted into a reusable template. Individual tasks can also be turned into templates. These templates can then be used to create new cases, complete with pre-created tasks, notes, tags, and other associated details.

![Template in FlowIntel](/img/flowintel-template.png)


### MISP

In one of the [latest releases](https://github.com/flowintel/flowintel/releases/tag/1.2.0), support for MISP-Objects was introduced, expanding FlowIntel's integration capabilities with MISP. MISP-Objects can now be stored within a case and sent to MISP through connectors. This functionality allows users to either create new MISP events or enrich existing ones directly from FlowIntel.

#### MISP Objects 

![MISP Objects and FlowIntel](/img/flowintel-objects.png)


#### Connectors for MISP Objects

![Connectors and MISP Objects](/img/flowintel-connectors.png)


### Analyzer

Cases and tasks in FlowIntel support notes that can be sent to analyzers for processing. The analyzers' results can then be received and stored as either MISP-Objects or additional notes within the platform. This feature was developed with the help of the [MISP-Modules website](https://github.com/MISP/misp-modules/tree/main/website).

![Analyzer in FlowIntel](/img/flowintel-analyzer.png)

![Analyzer in FlowIntel](/img/flowintel-analyzer2.png)

## Availability

[FlowIntel](https://github.com/flowintel/flowintel) is free and open-source, released under the AGPLv3 license! Sharing, liking, or providing feedback about your experience are valuable ways to contribute and support the project. By contributing, you become a co-owner and help ensure the long-term viability of the project as an open-source initiative.

## Funding 

The [FETTA (Federated European Team for Threat Analysis)](https://www.circl.lu/pub/press/20240131/) project aims to address this issue by creating a federated team that spans across borders, providing Cyber Threat Intelligence (CTI) products and tooling. FlowIntel is co-funded by CIRCL and the FETTA project under the Digital Europe Program, European Union is co-funding the project through the European Cybersecurity Competence Centre (ECCC). 

