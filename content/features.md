
---
title: MISP features and functionalities
aliases:
    - /features.html
---

## Features of MISP, the open source threat sharing platform. 

A threat intelligence platform for sharing, storing and correlating Indicators of Compromise of targeted attacks, threat intelligence, financial fraud information, vulnerability information or even counter-terrorism information. Discover how MISP is used today in multiple organisations. Not only to store, share, collaborate on cyber security indicators, malware analysis, but also to use the IoCs and information to detect and prevent attacks, frauds or threats against ICT infrastructures, organisations or people.</header>

![](/img/banner.jpg "{ class='img-responsive'}") 

- A **complete and robust threat intelligence sharing platform** that can be deployed on-premise, in the cloud, or as a SaaS solution, suitable for organizations of all sizes. 
- **Threat intelligence, ranging from indicators, through techniques to tactics, can be easily described in MISP**, from machine-readable actionable data to detailed reports in Markdown format.
- A flexible reporting system is integrated into MISP, enabling the description of threat intelligence with cross-references to the machine-readable components, including objects and attributes.
- A **fast and efficient database for atomic data points, indicators to complex objects and selectors**, enabling the storage of both technical and non-technical information related to cybersecurity intelligence as well as broader intelligence contexts.
- Automatic **correlation** engine, revealing relationships between attributes and indicators of malware, attack campaigns, analyses or other described threats. The correlation engine handles the interlinking of matching attributes as well as more advanced correlation patterns such as fuzzy hashing overlaps (e.g. ssdeep) and CIDR block matching. Correlations can also be enabled or event disabled at different levels of granularity.
- A **flexible data model**, where complex [objects](https://www.misp-project.org/objects.html) can be expressed and **linked together to express threat intelligence, incidents or connected elements**.
- Built-in **sharing functionality** to ease information exchange, using different, customisable, models of distribution. MISP can automatically synchronize events and attributes as well as higher level threat intelligence among different MISP instances. Advanced filtering functionalities can be used to meet each organization's sharing policy including a **flexible sharing group** capability and granularity up to the atomic attribute level.
- An **intuitive user-interface** for end-users to create, update and collaborate on events and attributes/indicators, in addition to a **graphical interface** to navigate seamlessly between events and their correlations as well as an **event graph** functionality to create and view relationships between objects and attributes. Advanced filtering functionalities and [warning lists](https://github.com/MISP/misp-warninglists) to help the analysts to contribute events and attributes and limit the risk of false-positives.
- A comprehensive **workflow system** to facilitate automatic, customisable data pipelines in MISP, including data qualification, automated analysis, modification, and publication control.
- **Storing data** in a structured format, enabling automated use of the database for various purposes, with extensive support for cybersecurity indicators, fraud indicators (e.g., in the financial sector), and broader intelligence contexts.
- All intelligence and information stored in MISP is accessible via the UI but also an [extensive ReST API described as OpenAPI](https://www.misp-project.org/openapi/).
- **Export**: Generate outputs in various formats, including various native IDS formats, OpenIOC, plain text, CSV, MISP JSON, STIX (XML and JSON) versions 1 and 2, NIDS exports (Suricata, Snort, and Bro/Zeek), RPZ zones, and cache formats for forensic tools. Additional formats, such as PDF, can be easily added and are available via the [misp-modules](https://github.com/MISP/misp-modules) or customised as built in export modules.
- **Import**: Support for free-text import, URL import, bulk import, batch import, and importing from formats a long list of formats, including MISP's own standard format, STIX 1.x/2.0, CSV, or various proprietary formats. Additional formats can be easily added via the [misp-modules](https://github.com/MISP/misp-modules) system.
- Flexible **free-text import** tool to simplify the integration of unstructured reports into MISP, with automatic detection and conversion of external reports via provided URLs and text reports with an automatic conversion into MISP reports, objects, and attributes.
- A user-friendly system to **collaborate** on events and attributes allowing MISP users to propose changes or updates to attributes/indicators or provide own perspectives or counter-analyses to shared information.
- An **extensive data analyst feature** allowing analysts to add opinions, relationships, or comments to any intelligence in MISP, which can be shared using MISP's sharing mechanisms.
- **Data sharing**: Automatically exchange and synchronize information in real-time with other parties and trust groups using MISP, with support for granular sharing levels and custom sharing groups.
- **delegating of sharing**: allows for a simple, pseudo-anonymous mechanism to delegate the publication of MISP data to communities.
- Flexible **API** to integrate MISP with your own solutions. MISP is bundled with [PyMISP](https://github.com/MISP/PyMISP) which is a flexible Python Library to fetch, add or update events attributes, handle malware samples or search for attributes. An exhaustive restSearch API to easily search for indicators in MISP and exports those in all the format supported by MISP.
- Built in tooling to build, test and analyse complex queries directly in the MISP GUI using a highly context aware, templated API client.
- **Adjustable taxonomy** to classify and tag events following your own classification schemes or [existing classification](https://github.com/MISP/misp-taxonomies). The taxonomy can be local to your MISP but also shareable among MISP instances.
- **Intelligence vocabularies** called MISP galaxy and bundled with existing [threat actors, malware, RAT, ransomware or MITRE ATT&CK](https://www.misp-project.org/galaxy.html) which can be easily linked with events, reports and attributes in MISP.
- **Expansion modules in Python** to expand MISP with your own services or activate already available [misp-modules](https://github.com/MISP/misp-modules).
- **Sighting support** to get observations from organizations concerning shared indicators and attributes. Sighting [can be contributed](https://www.circl.lu/doc/misp/automation/index.html#sightings-api) via the MISP user-interface and the API as MISP data or STIX sighting documents.
- **MISP Standard Format** support is integrated into MISP and used by a long list of tools and organisations worldwide. The [MISP standard format](https://www.misp-standard.org/) is stable and backward compatible with older datasets.
- **STIX support**: Import and export data in STIX versions 1 and 2 formats, leveraging the powerful [misp-stix library](https://github.com/misp/misp-stix).
- **Integrated encryption and signing of the notifications** via GnuPG and/or S/MIME depending on the user's preferences.
- **Dashboard feature**: Integrated into MISP, allowing users and organizations to create and share custom composited dashboard configurations as well as build bespoke monitoring solutions directly in a drag and drop interface.
- **Real-time** publish-subscribe channel within MISP to automatically get all changes (e.g. new events, indicators, sightings or tagging) in ZMQ (e.g. [SkillAegis](https://github.com/MISP/SkillAegis)) or Kafka publishing.
- **Flexible logging** subsystems to help with the auditing of the system as well as the user-base's actions on the system, with various output formats supported as well as a wide range of transport mechanisms for centralised logging needs.
- **Customisable RBAC**, allowing configurations of MISP to be run both as a permissive in-house tool as well as tightly regulated community instances.
- **Information signing and validation** for more diverse and sensitive information sharing communities.
- **Batteries included**: A long list of tooling for backups, integration with identity providers and authentication systems, information leakage prevention safety nets (such as [MISP-Guard](https://github.com/MISP/misp-guard)) as well as system monitoring tools.
- **Open-source commitment**: MISP and its copyright is fully owned by an interlocked license among all contributors, ensuring that no single organisation or company can ever change the license or model of MISP. Users of MISP can rely on the tool never turning into a closed source / proprietary / semi-open multi-tier model tool.

## Main advantages

The main benefit of using MISP is its ability to serve as a **comprehensive and robust platform for threat intelligence sharing and collaboration**, enabling organizations of all sizes to:

- **Centralize and manage intelligence:** Store, structure, and analyze both technical and non-technical threat intelligence efficiently.
- **Enhance collaboration:** Share information securely and flexibly with trust groups, leveraging granular sharing mechanisms and real-time synchronization.
- **Improve detection and response:** Correlate indicators, enrich intelligence, and automate workflows to enhance detection, analysis, and response capabilities.
- **Foster integration and interoperability:** Seamlessly integrate with existing tools and systems using APIs, modular extensions, and support for standard formats like STIX and MISP's own standardized format.
- **Enable actionable insights:** Provide actionable, machine-readable intelligence while also supporting detailed reporting for strategic and operational decision-making.

MISP empowers cybersecurity teams with a scalable, flexible, and user-friendly platform to streamline their threat intelligence processes and improve their collective defense capabilities.

### Sharing with humans 
Data you store is immediately available to your **colleagues** and **partners**. Store the event id in your ticketing system or be informed by the signed and encrypted email notifications. 
### Sharing with machines 
By generating **Snort/Suricata/Bro/Zeek IDS rules, STIX, OpenIOC**, text or csv exports MISP allows you to **automatically** import data in your detection systems resulting in **better and faster detection** of intrusions. Importing data can also be done in various ways: **free-text import, OpenIOC, batch import**, sandbox result import or using the preconfigured or **custom templates**. If you run MISP internally, data can also be uploaded and downloaded automagically **from and to externally hosted MISP instances**. Thanks to this automation and the effort of others you are now in possession of valuable indicators of compromise with no additional work. 

### Collaborative sharing of analysis and correlation 
How often has your team analyzed to realise at the end that a **colleague had already worked on another, similar, threat**? Or that an external report has already been made? When new data is added MISP will immediately show **relations with other observables and indicators**. This results in more efficient analysis, but also allows you to have a better picture of the TTPs, related campaigns and attribution. The **discussion** feature will also enable conversations between multiple analysts resulting in **win-win** for everyone. ![](/img/blog/automation-icon.png "{class='img-responsive'}")
