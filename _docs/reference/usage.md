---
layout: default
title: Reporting on Usage
nav_order: 1
parent: Reference
---
{{ site.app_name }} maintains usage statistics for reports, including who ran a report when and with what database. You can create reports with this information to determine which reports are actually being used, how often, and by whom.

 > You must be in the Administrators group to report on usage.

The table with usage statistics is available in the report wizards in [Step 2]({% link _docs/creating-reports/formatting-values.md %}). As a result, you can use this information in any of the available report types.

Usage has the following fields:

Report ID: the unique ID for the report.

Report Name: the name of the report.

Report Type: the type of report: Quick, Cross-tab, Label, Chart, Gauge, or Dashboard.

Folder: the folder the report is in.

Data Source: the data source the user ran the report against.

Run By User: the name of the user who ran the report.

Run At: the date and time the report was run.

Runtime: The number of seconds it took to run the report.

Tenant: The tenant the report belongs to. Only visible if tenant support is turned on.

> If you're interested in keeping track of high usage of server resources, you can create and schedule a usage report to do so. Set a filter on the report to only retrieve records with the *Runtime* above the desired threshold.