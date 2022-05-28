---
layout: default
title: What's New in this Release
nav_order: 2
has_children: true
parent: Home
---

# Version 6.0

* Administrators can now create usage reports. When creating a new quick report, use the new "Usage" table to access this data.

* You can now upload report files to a SFTP server. To specify that the target ftp server should use SFTP, prefix the server name with "sftp://".

* Report parameters are now available in the [Advanced Report Designer]({% link _docs/creating-reports/advanced-layout-designer/using-the-layout-designer.md %}).

* Previewing a [chart]({% link _docs/creating-reports/chart-reports/index.md %}) now displays the same view as when outputting the chart to a file. You'll still see the old chart view if a chart has click actions (e.g. drillthrough).

* You can now edit the values of parameters for an existing SQL Passthrough report. You'll find these settings under [Advanced Report Properties]({% link _docs/creating-reports/advanced-properties.md %}) in step 5 of the report wizards.

* In addition to being displayed with green colored text, "logged in" users now also have an icon displayed next to their entry in the user list. This should be helpful for users with certain types of color blindness.

* You can now search [formulas]({% link _docs/creating-reports/formulas.md %}) by name, report or caption (or tenant in a multi-tenant environment).

* Formulas now display the tenant they belong to in a multi-tenant environment.

* Tenant administrators can now see all schedules for users in their tenant.

* Issues with a field display expression no longer prevent the report from running.

* Added several new loading indicators.