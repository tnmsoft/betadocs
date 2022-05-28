---
layout: default
title: Stonefield Query 3.0
nav_order: 7
parent: Previous Releases
grand_parent: Home
---

# New Features

* The Reports Explorer now has a toolbar at the top with buttons for the selected report rather than sets of buttons for each report. This makes for a more attractive display and dramatically improves performance in Internet Explorer.

* The Tag Editor has a new interface.

* The report wizards have a new Use Table Layout setting that allows you to decide whether reports are rendered using absolute positioning or table layouts. This is useful if you find that objects are positioned quite where they should be.

* You can now specify what units measurements (such as field width) are in: inches or centimeters.

* Export options for a report now appear in a separate dialog and are also available from the Preview window. Also, a new output destination is available: FTP.

* The Import dialog now has an Import Report button to start the import process. Similarly, the Export Report dialog has an Export Report button.

* The login page now remembers your previous selection for data source.

* The data source now displays in the footer of the Reports Explorer rather than the header.

* Many performance improvements were made.

* Cross-tab reports and charts now support subreports.

* Outputting a cross-tab report to XLSX Full Format now outputs to a Microsoft Excel PivotTable.

* Cross-tab reports now fully support templates.

* The new Suppress Repeating Values setting for fields in cross-tab reports allows you to specify whether row fields display repeating values or not (the default is that they do not).

* The new Display Null as Zero setting in cross-tab reports displays null values as "0" rather than blank.

* As your mouse pointer moves over a data point in a chart, such as a bar in a bar chart, a popup window shows the category and value for the data point.

* Additional chart settings are available: you can now determine whether point labels are visible and if so, how to resolve overlapping labels, and indicate what's displayed in the legend: value, category, or both.

* The Advanced Report Designer is now available within the browser. Note that this version is not as full-featured as the desktop Advanced Report Designer, and is not available for cross-tab or chart reports, so for some types of reports you still may wish to use that version.

* Step 5 of the report wizards has a Delete Advanced Layout button for deleting the advanced layout of a report that has one.

* The desktop Advanced Report Designer now works with cross-tab reports.

* You are now prompted for parameters for the selected report when you edit the layout of a report that has parameters.

* You can now specify the default template to use for quick and cross-tab reports in the Options page.

* New and updated templates placed in the Templates folder are automatically copied to the App_Data\Templates folder.

* Several templates have been updated to be more attractive and there are new ones available.

* As mentioned earlier, cross-tab reports and charts now support subreports.

* Linked reports are now treated a little differently. Rather than having a Link tab in the Field Properties dialog, you set up linking in step 5 when you edit the layout of a report that has parameters. Also, subreports can now be placed in the report header.

* The report picker used when adding a subreport now shows the same tag structure as the Reports Explorer does.

* You can now create a shortcut on your desktop to preview a specific report.

* The Check for Updates function in the Tools menu checks to see if a new version is available.

* Active Directory authentication is now supported so you don't have to add users to Stonefield Query manually.

* The Security page displays both a count of logged-in users plus the logged-in status of each user. You can also force a user to log off.

* You can now use "." as an operator in formulas. For example, an expression like (Orders.ShippedDate * Orders.OrderDate).TotalHours, which determines the number of hours between when an item was ordered and when it's shipped, is now supported.

* You have to preview a formula in the Formula Editor to confirm that it works before saving. If the data type isn't set correctly, the Formula Editor changes it to the data type found after previewing.

* The Monthly schedule type has been split into separate Monthly and Monthly * Day of Month types.

* The Trim function now removes trailing null values as well as spaces.

* The Char and Chr functions now return a string rather than a char value char is rarely used and this saves having to use Char(x).ToString() in a formula.

* The new InList function determines if a set of values contains the specified value.

* A new variant of the LTrim function removes any character from the start of a string.

* The CMonth function was added for backward compatibility.

* The new Download Support Package function creates a support package you can sent to Technical Support for analysis.

* A timeout of one hour is now used on all queries so a report with a lot of data or a slow or busy server no longer times out if it takes less than an hour to run.

* Plugins downloaded from the Internet, such as when an update is sent, are now automatically unblocked rather than requiring you to unblock the DLL manually.

* You can now add a custom setting in web.config to disable forced SSL.

* The new How to Filter Unfavored Table setting in the Advanced Report Properties dialog allows you to customize the filter behavior for outer joins.

* To indicate no tenant, you now choose "No tenant" rather than a blank name from the Tenant list.

## Bug Fixes

* You now get a warning if you try to run a summary report without at least one grouped field.

* Running a report using an outer join between tables and a single filter condition on the unfavored table of the outer join no longer causes an error.

* Running a report with a linked report a second time no longer causes an error.

* The paper size for a report with no template is now Letter if there is no default printer rather than causing an error.

* A SQL Server CASE statement in the expression of a formula is now handled correctly.

* A bug that under some conditions prevented fields from being sized properly in a report was fixed.

* Quick reports now handle showing the percentage of total when there's more than one group in the report. Previously, each group footer showed the group total as a percentage of the grand total, not the next group level.

* A bug that caused extra quotes to appear in data-only output files was fixed.

* A bug that put empty columns into Excel output was fixed.

* Conditional formats in group and report footer objects are now properly supported.

* A bug that caused an error under some conditions when a user doesn't have access to all reports was fixed.

* A bug that didn't handle an expression in a formula such as if(Table.Field=0, 1, 2) was fixed.

* A bug that caused a "you are not eligible for the current version" warning to appear when a new version is installed that's newer than the maintenance expiry date was when an unlimited license was first activated but has since been renewed was fixed.

* A bug that causes some columns in a cross-tab report to be too narrow was fixed.

* The scheduler page now correctly shows when a schedule hasn't been run in Windows 10 (the "not run" code changed in that version).

* A bug that didn't set the values for parameters in advanced layout reports was fixed.

* A conditional format expression with AND or OR now work properly.

* A bug that didn't sort the values in the X-axis of a chart properly when the first series is missing values found in other series was fixed.

* Using Average to summarize the values of an integer field now results in a proper decimal value rather than an integer value.

* Column headings are no longer word-wrapped when outputting to Excel data only to avoid an empty row.

* A bug that caused the total count to be incorrect on a summary report when there's a field set to Count or Count Distinct was fixed. Also, the count is now sized properly for those types of reports.

* A bug that caused an error when a null date value for a field that has a format string was fixed.

* Summary reports grouped on a formatted date field are now sorted properly.

* A bug that caused an error if a template doesn't have a panel in the header and the reports displays group totals in the group header was fixed.

* Chart reports now work properly when they have an advanced layout.

* If you copy a report and specify the name of an existing report, the SFX file for the report is given a unique name so it doesn't ovrwrite the existing SFX file.

* A bug that caused an "invalid seat count" error when activating a license was fixed.

* A "file in use" error that occurred under some conditions after editing a template in the Template Editor was fixed.

* A bug that causes an error when a formula has a value converter was fixed.

* Clicking the browser Refresh button in the ODBC DSN page of the Setup Wizard now refreshes the list of DSNs so you can select one that was just added.

* A bug in which schedules that were renamed caused a new windows scheduler task to be created and orphaned the previous one was fixed.

* If removing a field from a report removes the last grouped field, Summary Report is now automatically turned off since that required grouped fields.

* A bug that caused an error when a return url parameter was missing in the login URL was fixed.

* A bug that caused an error when printing a report from the Preview window was fixed.

* A bug that caused an error when a report is run that has a field that was in a group header dragged to the grouped fields section was fixed.

* Reports that aren't accessible to the current user are hidden properly.

* A bug that caused a field with a multi-line heading to appear with "\n" in the heading was fixed.

* Previously, if you assigned a report with no tenant (that is, everyone can see it) a tag that has a specific tenant, users from other tenants could see that tag if they view the information popover dialog for the report. This was fixed.

* A bug that caused an error when a filter condition compared two fields was fixed.

* Reports with linked reports that have parameters now copy parameter values from parent report since the user can't be prompted for those values.

* The Is Blank filter operator now works correctly with Microsoft SQL Server.

* A bug that caused a licensing problem with unlimited licenses after renewal was fixed.

* Subtable filters now support Like and In operators.

* The license manager now longer checks the activation server for any other license after one fails. This should provide faster startup when there's a problem with the activation server and multiple licenses.

* Cancelling a cross-tab report during rendering no longer waits until rendering is complete.

* If an exception occurs during report loading due to a missing plugin, the loading process now continues rather than stopping.

* A drilldown or drillthrough report that doesn't have any ask-at-runtime filter conditions no longer causes an error when the parent report is run.

* A field using a value converter (for example, to convert string to datetime) with an expression-based filter condition on it in a report now works properly.

* Drilldown and drillthroughs reports now work properly for reports with advanced layouts.

* A bug in which copying a report with a space as the last character in the name failed was fixed.

* The "Use Date Only" checkbox is now supported for filter conditions on date fields that use a value converter.

* A report that has a invalid expression for a filter condition is now loaded properly.

* A bug that caused a user saving an existing task taking ownership of the task automatically was fixed.

* Charts now support DateTime fields for the series field.

* Different forms of the CAST function are now supported in expressions.

* Out of memory exceptions are now handled during data retrieval.

* The MySQL LIMIT clause is now properly supported.

* DateTime fields used in a filter condition with an "equals" operator are automatically converted to "is between" encompassing all hours on the specified date. This same conversion is now done for fields converted to DateTime with a value converter.

* A bug that caused Stonefield Query to think all licenses were in use when no one is logged in under some conditions was fixed.

* A bug in which previewing a chart also changes the chart, causing the preview image to also update, overwriting the chart report stored for the current context, was fixed.

* A bug which prevented dashboards from supporting tenants properly was fixed.

* All recipients are now respected when emailing a report, whether from the Preview window or a schedule.

* The current user is no longer logged out if they have no data source.

* An issue with 24 hour time formats causing an error when saving a schedule was fixed.

* An issue where a field was dragged out of the chart category caused the report to be sorted by both the current and previous category was fixed.

* A bug in which a report task from a previous schedule wasn't cleared when a new schedule is created was fixed.

* A bug that prevented a license from being activated manually was fixed.

* An issue where if you clicked fast enough on three steps at once, you could get two steps to load simultaneously in the browser was fixed.

* A couple of bugs related to dragging the last grouped field out of the grouped field section were fixed: Summary report remained on and couldn't be turned off, and any "In group header" fields had a null value and couldn't be turned off.

* An issue that caused reports to be loaded twice if the Reports Explorer was being loaded while another user saves a report was fixed.

* The Add Extension button in the License Manager is now disabled if all licenses are active.

* In the previous version, if you don't have a DSN set up and while in the ODBC DSN Setup page you click the browser's Refresh button, the Reports Explorer page is displayed but with "Data source: null" displayed and reports don't work. This was fixed.

* If there are no help topics available, the user is now told this rather than navigating to a missing page.

* You are now asked to confirm when you delete a schedule.

* Drill through reports now appear in a new tab when preview is set to appear in new page.

* We now store the current page when navigating to a drill down or drill through and restore that page when navigating back rather than going back to page 1.

* A debug window appeared on a production web server when a parsing error occurred. This has been fixed.

* An issue where running or editing a report in the search window was performing that action on the selected report rather than the one in the search was fixed.

* Since you can't change a normal formula to a grouping formula once it's been saved, when editing an existing formula, that control is now disabled.

* When importing two consecutive reports, selecting the second report wasn't updating the report text in the control. The report was still imported properly however, so this was just a display issue. This has been fixed.

* Errors in report scripts now appear as a warning message rather than freezing the preview window.

* The functions list in the Formula Editor now includes some missing functions such as Cast, If, and GetParameter.

* The title of the preview window is the name of the report if it's in a new tab.

* Two drilldown reports can no longer be linked on the same field.

* A schedule can no longer be saved without a name.

* A bug in which the date display for a filter wasn't respecting the user's setting for 12/24 hour time display was fixed.

* Sorting on a grouping calculated field now works correctly.

* A bug which caused an "Unknown" error message to be displayed rather than a invalid username/password error if a user tried logging in with a blank password was fixed.

* A bug that caused an error when copying a dashboard was fixed.

* A bug that under some conditions caused misalignment issues for reports used in a dashboard was fixed.

* A bug that caused a problem for a cross-tab with two fields with the same name was fixed.

* Fields included in the second level group now use the correct formatting (previously, they used the first level group formatting).

* Expressions in the Subject are now evaluated when outputting to PDF.

* Cross-tab reports now handle a template in which RowHeadingStyle doesn't set the font but DetailBandFieldStyle does, which resulted in the row fields being sized too small for the font being used.

* Permissions are now imported along with reports.

* A bug that caused an error if you closed the Preview window before the report appeared was fixed.

* A bug that sometimes caused the wrong fields to be listed for the selected table was fixed.

* Cross-tab reports now display "Total" properly in multi-row field reports.

* The Icon File configuration setting is now handled properly.

* The Expression setting in the Tag Editor is now hidden if the tag has a parent tag.

* A bug in which formulas created for a specific table might end up being assigned to a different table if the project has multiple tables with the same name was fixed.

* Field captions with expressions are now properly displayed.

* Step 2 of the report wizards now shows the correct default table for the selected data group.

* A bug in which the wrong report is output when exporting a child report after drilling through to it was fixed.

* The Table list in the Filter page now respects the select data group.