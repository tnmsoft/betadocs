---
layout: default
title: Stonefield Query 5.0
nav_order: 4
parent: Previous Releases
grand_parent: Home
---

# New Features

* Two factor authentication is now available for users that require additional security. You can enable it via a new tab in options.

* Improved loading times when initially opening a report for the first time.

* Administrator users can now specify that their email settings be used as the default settings. Any users that don't have email settings specified will use the default settings when sending emails.

* It's now much easier to create a SQL Passthrough report with parameters. Stonefield Query will detect each '?' placeholder in the SQL Statement and prompt for a caption and parameter value for it.

* If the current user belongs to a tenant, any reports imported by that user will now also belong to that tenant.

* Formulas created as part of an import are also assigned to the current tenant.

* User names with backslashes are now supported.

* You now get an appropriate error message if you try to delete a tenant that still contains users.

* When entering a server address for FTP, you can now optionally specify a ftp:// prefix if you'd like.

* The author and title properties are now set on generated Excel documents.

* Stonefield Query now supports multiple schedules with the same name (even across tenants).

* The user interface has several new progress indicators.

* The scheduler has a new "New schedule" button.

* When registering for a new user account, you can now choose the password rather than one being generated automatically.

* You now get a warning if you try to edit a report that is already being edited by another user.

* The properties dialog now includes the table each field is from to make fields with the same name easier to identify.

* The ask-at-runtime filter display now includes the connection for a filter condition.

* The ability to email and upload (to FTP) reports can now be restricted by role.

* The tooltip for a formula in the formulas list will display all reports a formula is being used in.

* A new button in step 2 of the report wizards will filter the list of tables to only those tables related to tables already appearing in the selected list.

## Bug Fixes

* A bug that caused some Crosstab reports to not finish rendering was fixed.

* Corrected spelling mistakes and typos in the english language resources.

* Fixed an issue with exclusion filters not working in some cases.

* You can now output reports to various Excel formats, even if the name of the report exceeds 31 characters.

* We now use the culture setting of the current user when outputting to Excel.

* A bug that caused dynamic tags to not work correctly was fixed.

* Fixed an issue with totals in the legend of a chart.

* Fixed an issue where a report with a template that had no detail band field template couldn't be output to data only formats.

* Fixed a bug with the document properties when outputting a batch report to a file.

* When using the "Hide null values" option on a Cross tab report, you will no longer see 0 total values for non-numeric columns.

* Fixed a bug with Cross tab reports not respecting custom font settings for row fields.

* Fixed a bug with the values dialog showing previously retrieved values.

* Fixed an issue with changing the field of an existing filter condition.

* Fixed a display issue with "full format" output types.

* Fixed several issues with tenant support. 

* You can now choose a data group even if there's no "All" datagroup available.

* Fixed a bug that allowed non-administrators to access the template editor.