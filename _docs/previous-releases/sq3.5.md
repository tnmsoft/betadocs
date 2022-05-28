---
layout: default
title: Stonefield Query 3.5
nav_order: 6
parent: Previous Releases
grand_parent: Home
---

# New Features

* A new report type, Batch Report, is now available. A batch report allows you to combine multiple reports in to a single output file in CSV, TXT, PDF, or XLSX formats. 

* Another new report type, SQL Passthrough, is also available for advanced users. A SQL Passthrough report allows you to build a report by entering a SQL Statement, then executes that SQL Statement against your database. The resulting report will have a report field that corresponds to each column in the data set retrieved from the database. 

* Several performance improvements have been made to the initial login process. 

* The automatic values retrieval that occurs when entering a value for a filter condition may now be turned off by the developer to improve performance. 

* When retrieving the values for a field, the resulting list is now sorted.

* Access to tags can now be controlled by setting permissions for them.

* Access to dashboards can also now be controlled by setting permissions for them.

* You can now specify a custom prompt for ask-at-runtime filter conditions. For example, if you have a filter condition on a field called "Year", the default caption for the ask-at-runtime prompt is "Year equals". However, you can now customize this to "Enter a year".

* Improved how error messages are displayed when they occur while running a report. 

* You can now specify a Stonefield Query role as an email recipient. When you do so, each user in that role with a defined email address will receive a copy of the email. 

* When entering email addresses for a scheduled task, a quick pick list will now appear showing previously entered email addresses and the available role values that can be specified. 
 
* Tags in the Tags dialog now show a count indicating how many reports each tag is assigned to.

* A conditional format now has the option to "Use default value" for each of the background and foreground colors.

* When exporting a report, if there's already a report selected in the main interface, that same report is the default selection when exporting. 

* The interface for the Setup dialog has been improved. 

* Most sections of the application (Report wizards, Formulas, Options, Schedules, Security, and Tags) now have footers to make the UI more consistent. 

* When removing users, roles, and tenants in the security dialog, you are now prompted to confirm the removal. This should prevent accidental deletions. 

* Several UI improvements were made to the layout step (Step 5) of the report wizards. In many cases, options now have shorter captions so that more settings are visible without needing to scroll. More detailed descriptions of each option are still available as tooltips. The buttons available in step 5 have been moved to a better location. 

* Improved the layout of column headers when the corresponding fields are wrapped to the next line. 

* Charts that specify a series field now have better tooltips. 

* The width of a CrossTab report field can now be defined manually (the default setting is Autofit like it is in Quick reports). 

* You can now specify an alignment value for fields in the column of a CrossTab report. 

* You can now turn on "Start each group on new page" for row fields in a CrossTab report.

* You can now specify the range of values for a chart axis. 

* The values in the chart legend (when visible) are now separated from the category with a hyphen to improve readability. 

* You can specify any character you like to use as a separator when outputting to CSV format. 

* You can now upload a report to FTP from a scheduled task. 

* The "Display nulls as 0" setting is now also supported when exporting a CrossTab report to Excel formats. 

* You can now remove the column header object from a template, and reports that use that template won't display column headers. 

* When outputting a report with embedded subreports to data based output types, the subreport contents will now appear in the output. 

* When a report used as a subreport has ask-at-runtime filter conditions added, you no longer need to remove and re-add the subreport from any parent reports that use it in order to set up the new parameter.

* A new function, Split, is now available. This function splits up a string into subsections by a defined separator character and returns the subsection corresponding to the passed-in numeric value.

* If a formula expression divides by 0, a specific error indicating this problem is now displayed.

* All built-in functions can now accept arguments with null values.

* Formula fields now have better support for working with dynamic fields in the data dictionary.

* Grouping formulas with ask-at-runtime filter conditions now prompt for new values when a report that uses the formula is run.

* You can now use the new constant NewLine to add a carriage return to the expression of a formula.

* When testing connection strings and DSNs from Setup, more detailed error information is now retrieved from the server if there's a problem.

* Cancelling a report now frees up system resources more quickly.

* More complex custom SQL Statements are now supported.

* You can now create schedules with a / character in the name. 

* When entering a custom SQL Statement for a report, you can enter placeholder "?" characters instead of the parameter values. Then, any ask-at-runtime condition values for the report will be used as the values for those parameters. 

* Date and time values for schedules are now converted between local time and server time in case the web server is in a different time zone than the users.

* The status display icon for a scheduled task will now appear as a yellow warning icon if a schedule hasn't been run yet, and as a green gear icon if the schedule is currently running.

* Access to each individual item in the Tools menu can now be assigned or revoked for specific roles.

* Added support for nesting a specific join to ensure that it's evaluated first by the database engine.

## Bug Fixes

* Fixed an issue that occurred when running a report linked to another report that could cause the filters conditions on the linked report to be changed. 

* A bug that caused schedules to run under the wrong user was fixed. 

* The scheduler now properly returns an error code when a schedule doesn't run properly.

* Enumerated field plugins now trim any values retrieved from the database before attempting a lookup. 

* The LookupFieldConverter now supports fields that use value converters as lookin or return fields. 

* Fixed a bug that caused charts to be sorted incorrectly under some circumstances.

* Fixed a bug that would occur if a TimeSpan field had an empty format string. 

* The word wrap setting is now respected when outputting to Excel 

* Fixed a bug with filter conditions on Date fields that used the "equals" operator.

* Group counts now work properly in summary reports. 

* Fixed an issue with using the "Count" function on a Date column in a summary report.

* Fixed an issue that occurred if you clicked the "Save to disk" button more than once in quick succession. 

* Fixed an issue that caused security resources to be saved for new reports, even if the report itself was never saved.

* Fixed a bug with loading and saving reports with customized joins.

* Fixed several issues with summary reports and numeric columns. 

* Fixed an issue with the chart report preview. 

* Fixed an issue that occurred when using a field with a value converter as a drilldown parameter. 

* Fixed a bug copying a report with a / in the name, which would cause the copy to be created in a subfolder.

* Fixed a bug that allowed the same schedule to be saved twice. 

* Fixed several issues with subtables. 

* Fixed an issue that occurred when adding a license serial # with trailing spaces. 

* Fixed several issues with using a chart report as a subreport. 

* Fixed several issues with specifying custom SQL Statements that involve multiple database objects. 

* Fixed an issue where a copied report would use the custom file name of the original report if one was defined. 

* Fixed an error that occurred when an embedded subreport encountered a problem while running. 

* Fixed an issue that occurred when a request from the Web client was quickly cancelled. For example, if you preview a report and then quickly close the preview window. 

* Fixed a bug that occurred if a project didn't have multiple data sources. 

* Fixed a bug where the "UseTableLayout" wasn't being set properly for regular (non-dashboard) report types.

* Fixed a bug with chart drill downs not working properly when the child report has a filter on an enumerated field.

* Fixed a bug with the filter table drop down not showing all tables in the current datagroup.

* Fixed an issue that allowed tenant specific formulas to be visible to users not in that tenant. 

* Removed the summary type option from grouped fields, since it makes no sense to summarize a grouped field. 

* Fixed an issue that would occur if you entered an extension code in lower case. 

* Fixed an issue where an apostrophe in the report name was causing an error when previewing the report.

* Fixed an issue where a scheduled task set to upload to FTP would reset the FTP Password value each time the schedule was edited. 

* Fixed an issue with the wrong initial date and time values being used if a user had 12 hour time display turned on. 

* Fixed a bug where Administrator users were unable to log in to the setup page to resolve data source errors.

* Fixed a bug that prevented adding new licenses in some cases. 

* Context sensitive help now works for wizards that only have a single help page.

* Fixed an issue that would occur if you created a report, then tried to use that report as a subreport in another new report without refreshing the browser. 

* Fixed an issue with the chart series type not being set properly when editing existing chart reports. 

* If a field is detected in a conditional format expression that isn't included in the report, that field is now added retrieved from the database so the conditional expressions works.