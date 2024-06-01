---
layout: default
title: Stonefield Query 6.0
nav_order: 4
parent: Previous Releases
grand_parent: Home
---

# New Features

* Administrators can now create usage reports. When creating a new quick report, use the new "Usage" table to access this data.

* You can now upload report files to SFTP. To specify that the target ftp server should use SFTP, prefix the server name with "sftp://".

* Report parameters are now available in the Advanced Report Designer.

* Previewing a chart now displays the same view as when outputting the chart to a file. You'll still see the old chart view if a chart has click actions (e.g. drillthrough).

* You can now edit the values of parameters for an existing SQL Passthrough report. You'll find these settings under "Advanced Report Properties" in step 5 of the report wizards.

* In addition to being displayed with green colored text, "logged in" users now also have an icon displayed next to their entry in the user list. This should be helpful for users with certain types of color blindness. 

* You can now search formulas by name, report or caption (or tenant in a multi-tenant environment).

* Formulas now display the tenant they belong to in a multi-tenant environment.

* Tenant administrators can now see all schedules for users in their tenant.

* Issues with a field display expression no longer prevent the report from running.

* Added several new loading indicators.

## Bug Fixes

* Fixed a bug where resizing for a springy field was impacting fields in other rows than the current one.

* Fixed several bugs that caused reports to occasionally not load properly. 

* Fixed an issue with having two roles with the same name in a multi-tenant environment.

* Fixed an issue with using filter conditions on a SQL Passthrough report.

* Fixed a bug where parameters were not loaded properly for a SQL Passthrough report when running from a schedule.

* Fixed an issue when importing a report that has tags the current user cannot access.

* Fixed several issues with generating and downloading SupportFiles.zip and SupportPackage.zip.

* Fixed a bug with overlapping point labels in a chart report.

* Fixed a bug with a formatted field as the series field in a chart not showing any data.

* Fixed a bug with Drilldown reports not working properly.

* Fixed an issue with barcodes not being handled properly.

* Fixed a bug with schedules not being set to the correct output type.

* Fixed issue with last day of month setting not working properly for a new schedule.

* Renaming an user will now properly update existing schedules for that user.

* Fixed several permission issues that occurred when importing a report in a multi-tenant environment.

* When choosing a report with the report picker, any previous selection should now be selected by default.

* Fixed issue with editing schedules not setting the output type properly upon resaving.

* Autocomplete in browsers should no longer try to fill any values besides those on the login page.

* Fixed a timing issue with filter values when loading a report.

* Fixed a bug with directly exporting a report to file.

* Fixed a bug that was changing the data source when saving an existing schedule.

* Fixed a bug with progress spinner not turning off when a report was cancelled.

* Fixed an issue with side by side dashboards.