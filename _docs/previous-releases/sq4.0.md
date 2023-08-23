---
layout: default
title: Stonefield Query 4.0
nav_order: 6
parent: Previous Releases
grand_parent: Home
---

# New Features

* A new linked report type, Side By Side, is now available. When this is used, you can preview a parent and child report beside each other.

* You can specify an optional display expression for report fields. If specified, the value of the expression will be displayed in place of the field value, but sorting will be preserved.

* If enabled for the project, users can now request a password reset email and change their password.

* You can now export a report (File, FTP, Email) directly without previewing it first from the Export Options dialog.

* The new Templates tab in the Options dialog, available from the Tools menu, allows you to copy, delete, or edit your templates.

* A new Expression Builder dialog is available for filter condition expressions, display expressions, and conditional format expressions.

* A warning now appears when refreshing collections since all users will be logged out.

* Browser password managers such as Chrome Smart Lock are now supported in the Login page.

* A new setting in the Options dialog allows you to impose a limit on how much system memory is occupied when a query is split and joined in memory.

* The new Training function in the Help menu allows you to launch an in-app training program that covers the use of the main Reports Explorer.

* The Export Options dialog now has settings organized into groups. Groups are collapsed by default unless any settings in that group have been changed.

* When you click the Values button for a filter condition, existing values for the condition are now pre-selected in the list.

* You can now search the values list when you click the Values button for a field or filter condition.

* Previewing a batch report now opens the report in a new preview tab. To export a batch report, use the Export Options dialog.

* The Schedule Wizard no longer displays tags that don't contain any reports.

* If you have Tenant support enabled, Administrator users will see the Tenant and Last Modified User in the report list. This will make reports with similar names easier to manage in multi-tenant installations.

* The output of a Quick report to the data only formats such as XLSX has been improved.

* You can now show percentage values for the point labels in Pie, Doughnut, and FullStacked chart types.

* We now do a better job calculating the column width of columns in a Cross-tab.

* The output of a Cross-tab report to the data only formats such as XLSX has been improved.

* A new function, GetConditionValue, allows you to retrieve filter values for a running report and use the values in a formula expression.

* The list of available functions no longer includes duplicates or obsolete functions.

* You can now use LIKE as a comparison operator in database expressions.

* If a report has the same filter conditions as a group formula on that report, the values from the report will be used. Note that this only affects non ask-at-runtime filter conditions. You will continue to be prompted if ask-at-runtime is toggled on. 

* A list of commonly used expressions is now available.

* You no longer need to manage the fields included in an expression. If you insert (or type in manually) a field in TableName.FieldName syntax in an expression, the appropriate fields are added automatically.

* There is improved support for ntext type fields in formula expressions.

* You can now search the available field list when editing a formula expression.

* Date functions can now be used with database columns that may have null values.

* Date fields formatted as Date (using {0:d}) now appear with the same format in Excel output.

* You can now specify a Reply To email address in email settings.

* You can now assign more than one tenant to a user.

* The loading performance for reports, formulas, and schedules has been improved.

* You can now show the name of the current database in the report header.

* You no longer have to restart the server after making changes to licenses.

* More kinds of SQL Statements are now supported when creating a SQL Passthrough report, and there's no longer a length limit on the SQL Statement.

## Bug Fixes

* Several issues related to Internet Explorer bugs are fixed. A more modern browser (e.g. Chrome, Firefox, Edge) is still preferred though.

* Fixed a bug where a problem with a field in the data dictionary prevented the project from loading.

* Improved error handling when a query is issued for a table that no longer exists.

* Improved error handling if problem occurs when uploading a report to an FTP site.

* When copying a report, we now remove any tags that come from a different tenant if the current user making the copy belongs to a tenant.

* Fixed a bug where some users were able to log in twice and occupy two licenses.

* Fixed an issue with users with a hyphen in the user name.

* Fixed an issue with schedules with a month based trigger.

* A summary report with more than one grouped field will now be sorted properly.

* Fixed a bug with certain passwords not working.

* The SMTP Client should now use the proper order of commands when communicating with the server.

* Fixed a bug with custom SQL Statements not working if a report's query was being split.

* Fixed a bug with the left function not handling a length parameter longer than the input string.

* Fixed a bug where a user could be both an Administrator and a Tenant Administrator.

* Fixed an issue with a null category value in a chart report.

* Label reports now use the correct dimensions.

* A problem with one report no longer prevents all other reports from loading.

* You can no longer specify a blank password.

* Fixed an issue with drillthrough report links not working.

* Fixed a bug with the site cookie overwriting other cookies from the same web server.

* Fixed a bug with the datasource on a schedule being changed occasionally.

* Fixed a bug with the Setup dialog not saving changes properly.

* You no longer need to click the Save button twice to save a tag.

* Fixed an issue with Chart reports not using advanced layouts.