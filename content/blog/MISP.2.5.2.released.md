---
title: MISP 2.4.200 and 2.5.2 released - Post Hack.lu/CTI-Summit release with many new features
banner: /img/blog/2.5.2/adhoc-trigger.png
author:
 - MISP Project team
date: 2024-11-19
tags: ["MISP", "Threat Intelligence", "release" ]
layout: post
---

The [Hack.lu/CTI-Summit](https://hack.lu/) once again allowed us to get in touch with the community and sit down to talk about new features and issues to be implemented. As usual, it was a real pleasure to get that much concentrated feedback. In this release, we put a lot of effort trying to fix and create new content as much as possible based on the collected needs of the community.

## Ad-Hoc Workflows

In MISP, we’ve always had the ability to create workflows based on application events, or "triggers" - like when an event is published, or when a tag is attached. Now, with the new Ad-Hoc Workflow feature, we're taking automation a step further. This feature allows you to build workflows that don’t depend on specific events occurring in MISP, opening up new ways to manage and interact with data.

![Ad-Hoc Triggers](/img/blog/2.5.2/adhoc-trigger.png)

Ad-Hoc Workflows can be executed manually or scheduled, offering flexible options for routine or custom tasks. Additionally, the new `run_workflow` module enables workflows to launch other workflows, opening new chains of automation.

![Worflow action module](/img/blog/2.5.2/run_wf_action_module.png)

With these standalone worklows at hand, the first things that came right into our mind was to allow users to apply a workflow directly to an event, similar to how you’d run an enrichment.

![Run Workflow on an Event](/img/blog/2.5.2/run-wf-on-event.png)

These new capabilities unlock more automation possibilities, but with great power comes great danger to mess your data up! The increased flexibility means there’s potential to unintentionally alter data, so use this feature thoughtfully.

## Galaxies
### Any Galaxy Matrix on the Event view
In the event view, you can now access all available galaxy matrices and select the specific one you'd like to view - a long-overdue feature that will finally give users a way to use their own matrices.

![Galaxy Matrix](/img/blog/2.5.2/galaxy-matrix.png)

### MITRE ATT&CK
Finally, the matrix for MITRE ATT&CK also includes an unfiltered tab `attack-enterprise` that shows all techniques on the same tab. This tab is the one that's opened by default whevener the matrix is diplayed.


### Private Custom Galaxies
Now in MISP, you can create and edit Custom Galaxies. Galaxies can have ownership and distribution levels, allowing galaxies and their clusters to be hidden as needed. Note that, similar to default Clusters, default Galaxies aren't editable.

![Custom Galaxy add](/img/blog/2.5.2/custom-galaxy-add.png)
![Custom Galaxy view](/img/blog/2.5.2/custom-galaxy.png)

it’s now possible to encounter tags from unknown clusters through synchronization. 

With this added flexibility there is a greater chance to encounter tags from unknown Galaxies or Clusters. This small UI issue can be addressed with a new setting `MISP.hide_unknown_cluster`. It will be enabled by default and hides unknown clusters from your tags list.

With the ability to hide clusters (and galaxies), a misconfiguration could unintentionally lead to large amounts of data being hidden. To address this, we've introduced a diagnostic widget on the Galaxy index page. This widget serves as a warning system, briefly highlighting unknown default and custom clusters.

![Custom Galaxy diagnostic widget](/img/blog/2.5.2/galaxy-custom-widget.png)


## Event Reports
There has been many changes for Event Reports. Let's have a quick look at what's new!

### Tags on Event Reports
To improve classification and sorting, users can now attach (global and local) tags on Event Reports.
![Tags on event reports](/img/blog/2.5.2/eventreport-tags.png)

### Template Variables in Event Reports
![Event report settings](/img/blog/2.5.2/eventreport-settings.png)

Template variables can now be defined in the user-settings for content that get reused in all event reports. These variables can be with the handlebars-style notation, `{{ var_name }}`. The replacement is done automatically when the report is visualized or exported. The UI has also been updated to support hints to specify these template variables.
![Event report template variables](/img/blog/2.5.2/eventreport-variables.png)

### Export as PDF using Pandoc (through misp-module)
We added a new "Download as PDF" option is in event reports, offering an alternative to the traditional "Save as PDF" print method. This functionality uses the `convert_markdown_to_pdf.py` module from the misp-module project. It converts markdown content (GFM format supporting HTML) to PDF using Pandoc, wkhtmltopdf and mermaid-cli. Note that these 3 dependencies have to be installed in order for the module to work as intended.
![Export event report as PDF](/img/blog/2.5.2/eventreport-download.png)

### Picture Pasting in Event Reports
You can now paste pictures directly into the Event Report editor. This long-awaited feature allows you to save images either on the disk or as an attachment to the event, making the reporting process faster and smoother.

{{<video src="/img/blog/2.5.2/event-report-img-pasting.mp4" title="Event report image pasting demo" >}}

### Manage Imported pictures
![Manage Imported Pictures](/img/blog/2.5.2/manage-imported-pictures.png)
Site admins have the ability to manage images pasted but not saved as attributes. They can assign aliases to these images, allowing for quick and easy inclusion in reports using the following syntax:
```md
![picture_alias](picture_alias)
```

## Extending Event
We've enhanced the extended event functionality to make it more intuitive and slightly more versatile. Previously, you could switch to "extended view" to see the combined content of the parent event and all its child events. Now, we've added the reverse option: a merged view where the parent's data is merged into the child event.

Additionally, we've improved the UI to better indicate whether you're viewing an extended event (parent) or an extending event (child).
![Extending Event child](/img/blog/2.5.2/extending-event-child.png)
![Extending Event parent](/img/blog/2.5.2/extending-event-parent.png)


## First version of the RHEL installer added
With the release of MISP 2.5.x, we've culled the number of target operating systems for the native installer scripts down to a list of just one entry, namely Ubuntu 24.04. Whilst we're rolling out MISP 2.5 on all of our instances, we don't want to leave RHEL users lagging too far behind, so we have released the first iteration of the installer with the 2.5.2 release, introducing a modernised stack also to the RHEL MISP community.

The requirements so far are an up to date RHEL installation, with RHEL 9.4 as the minimum. The current installation still comes with some caveats, it's so far in experimental state until we get more feedback from the community, as well as one feature confirmed not working 100% correctly yet: Worker management using Supervisor works, but when SELinux is set to be enforced, MISP cannot determine the process owner of the worker process. This state is displayed via a new diagnostic state as seen below.

![RHEL worker display](/img/blog/2.5.2/rhel_worker.png)

An update script to bring MISP 2.4.x to 2.5.x on RHEL is still in the works and planned for a future update.

## Long list of fixes

This version also bring a host of fixes, reported and fixed by the community, both introduced with the switch to PHP8 as well as long standing issues from before. Dive into [the changelog](https://www.misp-project.org/Changelog.txt) for an exhaustive list of changes.

Once again, thanks to Hack.lu/CTI-Summit attendees for all the feedback but also all the other contributors that helps us make the tool better. Thank you!

# MISP galaxy, MISP objects and MISP taxonomies new version released

- [MISP Galaxy 2024110700 has been released with many updates and improvements](https://github.com/MISP/misp-galaxy/releases/tag/2024110700)
- [MISP Taxonomies 2024111100 released](https://github.com/MISP/misp-taxonomies/releases/tag/2024111100)
- [MISP objects release 2024111100](https://github.com/MISP/misp-objects/releases/tag/2024111100)

Starting with this release, MISP galaxy, misp taxonomies and misp objects will be tagged using the %Y%m%d00 format for each new version. This change enables users to easily verify whether they are using the latest release. The versioning is now independent of the MISP core software, as the project is also utilized as a standalone tool in various other applications. For details about the changes, feel free to review each release.
