---
layout: default
title: Stonefield Query 5.1
nav_order: 4
parent: Previous Releases
grand_parent: Home
---

# New Features

* You can now specify a page field for Cross Tab reports.

* When you rename a report, any custom file names stored with the export options for that report are now cleared.

* You can now set a duration for the repeat interval of a scheduled task.

* A user with a Report Viewer license can now edit the filter conditions of a report. 

* If a schedule fails because one of the reports didn't match any records, we now display a more specific error message about this.

* When sending emails using the credentials of an Administrator account, email address of the user account is now used as the From address. This allows an email service like SendGrid to send from a previously verified domain.

* A new report management interface is available under the tools menu. This allows you to change the roles or tenant setting for multiple reports at the same time. You can also delete multiple reports using this interface, rather than having to delete them one at a time.

* Fields with a display expression can now be output to the Excel Data Only format. 

* Chart reports now automatically switch to landscape if the width of the chart exceeds the width of the page in portrait.

* Dynamic tables for SQL Passthrough reports should no longer appear in the available tables list.

* Fixed a bug whre a tag with subtags wasn't visible, even if it had relevant reports.

## Bug Fixes

* Fixed an issue with drill downs not working properly with a pie chart.

* Advanced layouts are now properly applied when previewing a report from the main explorer view.

* A user that doesn't have the ability to email or upload (FTP) a report will no longer see the corresponding options when exporting a report.

* Fixed a bug that prevented deleting an existing advanced layout.

* If there is a problem with a schedule, it no longer prevents all other schedules from loading.

* Fixed an issue with subreports not working properly with a report that has an advanced layout.

* Fixed an issue with the involved fields list of a formula including fields from other tables.

* Fixed a bug with ignored filter conditions still being applied to the query.

* Fixed an issue with subreports not running under the correct user context.

* Fixed an issue with template styles not being utilized in some cases.

* Fixed a display issue with chart point labels.

* Summary objects should now be positioned correctly when the corresponding object in the detail band is wrapped to the next line.