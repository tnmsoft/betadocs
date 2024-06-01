---
layout: default
title: Horizon Reports 1.1
nav_order: 2
parent: Previous Releases
grand_parent: Home
---

# Version 1.1

* [Dashboards]({% link _docs/creating-reports/dashboards/index.md %}) have been updated with a new modern web dashboard control. Dashboards now allow you to display a number of inter-connected data analysis elements such as grids, charts, maps, gauges, and others; all within an automatically-arranged layout. 

* A new [report monitor]({% link _docs/configuration/monitor-reports.md %}) dialog is available. You can use this tool to monitor active reports. If a report is consuming too many server resources, you can also request that the server try to cancel the report from this screen.

* When turning on [Two Factor Authentication]({% link _docs/configuration/configuration.md %}), the generated QR Code now has an issuer defined for apps that require it. 

* The [manage reports]({% link _docs/configuration/managing-reports.md %}) dialog has new "Updated by" and "Updated on" columns. 

* When creating a [new formula]({% link _docs/creating-reports/formulas.md %}), it's no longer necessary to preview the formula before saving. Instead, a warning is shown if the formula hasn't been previewed first. 

* Improved performance in the browser when creating formulas in a project with a large data dictionary.

* You can now include multiple [subreports]({% link _docs/creating-reports/subreports.md %}) in the header of a report.

* Added a preview button to [dashboard wizard]({% link _docs/creating-reports/dashboards/index.md %}) to allow previewing changes before saving.

* You can now use charts and pivot grids directly in a report with an [advanced layout]({% link _docs/creating-reports/advanced-layout-designer/index.md %}).

## Bug Fixes

* Fixed a bug that prevented users from being logged out properly.

* Fixed a bug that occurred when creating new SQL Passthrough reports. 

* The tour prompt that appears for new users should now only appear once.

* Fixed a bug with SFTP upload not uploading the output file properly. 

* Fixed an issue with an "is between" filter on a date value not setting the end time to include the last day.

* A formula with a blank name should no longer cause an error when logging in.