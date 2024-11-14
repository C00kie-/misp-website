---
title: MISP 2.4.199 and 2.5.2 released with new features, improvements and many fixes.
date: 2024-11-15
layout: post
tags: ["MISP", "Threat Intelligence", "release" ]
banner: /img/blog/object-collapse.png
---


# MISP 2.4.200 and 2.5.2 release - Post Hack.lu/CTI-Summit release

The [Hack.lu/CTI-Summit](https://hack.lu/) once again allowed us to get in touch with the community and sit down to talk about new features and issues to be implemented. As usual, it was a real pleasure to get that much concentrated feedback. In this release, we put a lot of effort trying to fix and create new content as much as possible based on the collected needs of the community.

## Ad-Hoc Workflows

In MISP, we’ve always had the ability to create workflows based on application events, or "triggers" - like when an event is published, or when a tag is attached. Now, with the new Ad-Hoc Workflow feature, we're taking automation a step further. This feature allows you to build workflows that don’t depend on specific events occurring in MISP, opening up new ways to manage and interact with data.

![Ad-Hoc Triggers](/img/blog/2.5.2/adhoc-trigger.png)

Ad-Hoc Workflows can be executed manually or scheduled, offering flexible options for routine or custom tasks. Additionally, the new `run_workflow` module enables workflows to launch other workflows, opening new chains of automation.

![Ad-Hoc Triggers](/img/blog/2.5.2/run_wf_action_module.png)

With these standalone worklows at hand, the first things that came right into our mind was to allow users to apply a workflow directly to an event, similar to how you’d run an enrichment.

![Ad-Hoc Triggers](/img/blog/2.5.2/run-wf-on-event.png)

These new capabilities unlock more automation possibilities, but with great power comes great danger to mess your data up! The increased flexibility means there’s potential to unintentionally alter data, so use this feature thoughtfully.

## Galaxies
## Any Galaxy on the Event view
In the event view, you can now access all available galaxy matrices and select the specific one you'd like to view - a long-overdue feature that will finally give users a way to use their own matrices.

![Ad-Hoc Triggers](/img/blog/2.5.2/galaxy-matrix.png)

## MITRE ATT&CK
Finally, the matrix for MITRE ATT&CK also includes an unfiltered tab `attack-enterprise` that shows all techniques on the same tab. This tab is the one that's opened by default whevener the matrix is diplayed.


### Private Custom Galaxies
Now in MISP, you can create and edit Custom Galaxies. Galaxies can have ownership and distribution levels, allowing galaxies and their clusters to be hidden as needed. Note that, similar to default Clusters, default Galaxies aren't editable.

![Ad-Hoc Triggers](/img/blog/2.5.2/custom-galaxy-add.png)
![Ad-Hoc Triggers](/img/blog/2.5.2/custom-galaxy.png)

it’s now possible to encounter tags from unknown clusters through synchronization. 

With this added flexibility there is a greater chance to encounter tags from unknown Galaxies or Clusters. This small UI issue can be addressed with a new setting `MISP.hide_unknown_cluster`. It will be enabled by default and hides unknown clusters from your tags list.

## Event Reports
There has been many changes for Event Reports. Let's have a quick look at what's new!

### Tags on Event Reports
To improve classification and sorting, users can now attach (global and local) tags on Event Reports.
![Ad-Hoc Triggers](/img/blog/2.5.2/eventreport-tags.png)

### User Variables in Event Reports
- User can define template variable in their user-settings
- These variables can then be replaced in the event-report
- The syntax to use the variable is the handlebars-style notation `{{var_name}}`
- Also added support of hints when editing and UI to specify the template vars
- Enabled more than 1 matrix in event report

![Ad-Hoc Triggers](/img/blog/2.5.2/eventreport-settings.png)

Template variables can now be defined in the user-settings for content that get reused in all event reports. These variables can be with the handlebars-style notation, `{{ var_name }}`. The replacement is done automatically when the report is visualized or exported. The UI has also been updated to support hints to specify these template variables.
![Ad-Hoc Triggers](/img/blog/2.5.2/eventreport-variables.png)

### Export as PDF using Pandoc (through misp-module)
We added a new "Download as PDF" option is in event reports, offering an alternative to the traditional "Save as PDF" print method. This functionality uses the `convert_markdown_to_pdf.py` module from the misp-module project. It converts markdown content (GFM format supporting HTML) to PDF using Pandoc and wkhtmltopdf. Note that these 2 dependencies have to be installed in order for the module to work as intended.
![Ad-Hoc Triggers](/img/blog/2.5.2/eventreport-download.png)

Once again, thanks to Hack.lu/CTI-Summit attendees for all the feedback
