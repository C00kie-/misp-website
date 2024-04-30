---
title: MISP 2.4.151 released (Black friday threat intel rush release)
date: 2021-11-23
layout: post
banner: /img/blog/graph-syria.png
---

# MISP 2.4.151 released

MISP 2.4.151 released including a host of bug fixes and a bunch of new features

# New features

- New background processor by @righel
- Improvements to the CLI tools
- Bug fixes and improvements

# New background processor

- MISP has been using CakeResque for its background jobs for the better part of a decade. Whilst it has served us well, the library has been stale for a long time and carries a (for us) unnecessary complexity and is generally the most difficult part of the application to debug
- Luciano "@righel" Righetti has implemented a completely new, compatible background processing engine using Supervisord
- Queue and execute jobs the same way as you are used to from before, monitor worker progress via the tools provided by supervisord in addition to MISP
- No scheduling capabilities, these were an unnecessary overhead for us before as we relied on corn jobs as our preferred scheduling mechanism anyway
- Expect more improvements to this library over the course of the next months, but feel free to switch to using it already now
- Currently it is completely optional and the old background processor will still be supported for a while
- Be aware that manual setup steps are required to get the new processor working, refer to [the upgrade guide](https://github.com/MISP/MISP/blob/2.4/docs/background-jobs-migration-guide.md) on the procedure, if you decide to start using it already now

# Various CLI changes

- Jakub Onderka has been doing a fair bit of refactoring and improvement of the CLI libraries
- additional administrative tools added to help monitor and manage your MISP instance (such as redis memory diagnostics, mysql table optimisation tool, etc)

# Option to move the system settings to the database

- Traditionally all system config settings were stored in the config.php file, with a new configuration thanks to Jakub Onderka's implementation the settings can be moved to the database rather than the file.
- This should help with persistence for containerised installations

# Various improvements

- The previous version introduced a new STIX library as a replacement for the old one. This change did end up causing some update issues for some installations, the built in updater is now aware of this change and should allow you to easily update via the UI/API updater, with the new STIX library working as intended
- A long list of improvements, thanks to all contributors! For a detailed list of changes, head over to the [changelog](/Changelog.txt)

# MISP Modules

- New [Passive SSH expansion](https://github.com/D4-project/passive-ssh) expansion module.
- Updated [Recorded Future](https://misp.github.io/misp-modules/expansion/#recordedfuture) expansion module included links and related data.
- New [CIRCL hashlookup expansion](https://circl.lu/services/hashlookup/) module added.

The [MISP modules changelog is available](/Changelog-misp-modules.txt).

# MISP Taxonomies

- Updated taxonomies for [Interactive Cyber Training setup and environment](/taxonomies.html#_interactive_cyber_training_audience).
- Updated [fr-classification](/taxonomies.html#_fr_classif) to match IGI1300. 

[MISP Taxonomies changelog](/Changelog-misp-taxonomies.txt) is available.

# MISP Galaxy

- Updated to MITRE ATT&CK version 10.
- Multiple updates in malpedia, threat actor galaxy and Office 365 techniques.

[MISP Galaxy changelog](/Changelog-misp-galaxy.txt)

# MISP Objects

- New JA3 server object added.
- New Security playbook object added.
- New submarine object added
- New Passive SSH object added.
- Updated device object.
- New hashlookup object added.
- New edr-report object added.

[MISP objects changelog](/Changelog-misp-objects.txt)

# Acknowledgement

We would like to thank all the [contributors](/contributors), reporters and users who have helped us in the past months to improve MISP and information sharing at large. This release includes multiple updates in [misp-objects](/objects.html), [misp-taxonomies](/taxonomies.html) and [misp-galaxy](/galaxy.html)
.

As always, a detailed and [complete changelog is available](/Changelog.txt) with all the fixes, changes and improvements.

