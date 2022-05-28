---
layout: default
title: Stonefield Query 2.0
nav_order: 8
parent: Previous Releases
grand_parent: Home
---

# New Features

* Charts and dashboards are now supported.

* A new type of filtering is available: group filters. A regular filter condition filters at the record level; for example, show all customers with an invoice amount is greater than $100. A group filter condition filters at a group level; for example, show all customers whose total invoice amounts are greater than $100.

* Embedded subreports that aren't linked to a field are now supported: click the new Subreport Properties button in step 5. This can be used, for example, to add a chart to a quick report.

* The Preview window has an updated appearance: the toolbar is now part of the document instead of floating, the Back button for drill-through reports now appears in the toolbar, and the document map is now supported, so if you have a report with "Bookmark on this field" turned on, the links column appears. Also, there are two new output types available: Xls Full Format and Xlsx Full Format, both of which output to Microsoft Excel spreadsheets in a format closely matching the report. The Export to New Window button was removed since it isn't needed.

* The new Search box in the Reports Explorer allows you to find a report by any keyword.

* The new Filter box in step 2 of the report wizards allows you to see only those fields whose names contain the text you specify.

* A new option for quick reports, Move Subtotals to New Row if They Overlap With Subtotal Labels, allows you to control where subtotals are placed if they're too close to the left margin.

* You can now password protect files you export.

* A new Summary option for grouping formulas, Concatenate, allows you to combine the values of a field from several records. This is useful, for example, to create a formula that lists all of the products purchased by a customers in a single record rather than one record per purchase.

* More formats are available for DateTime and TimeSpan values in quick reports and labels, including both 12 and 24-hour formats.

* New formats are available for DateTime values in a cross-tab report: Quarter, Quarter/Year, Month/Year, and Abbreviated Month/Year.

* Status indicators in the Selected Fields list in step 2 of the Quick Report Wizard help you to quickly see whether a field is grouped, sorted, or not displayed in the report.

* New Hour and ISNull functions are available in formulas. Also, the new GetConditionValue function can be used in an expression for the Title of a report or for the custom description of a filter condition.

* New Ends With and Does Not End With filter operators are now available.

* You can now create a daily schedule that repeats every so many minutes.

* Formulas now display "[Formula]" as a prefix so you can quickly see which are real fields and which are formulas.

* The Selected Fields list in step 2 of the report wizards now displays Values and Edit Formula buttons.

* If a field is used more than once in a report with different formats (for example, a DateTime field formatted as both Month and as Date), the format of the field is displayed as a suffix so you can tell which one is which.

* The Formula Editor now has a Security tab so you can specify which roles have permission to edit the formula and which roles have permission to see the formula.

* There are numerous performance improvements, including loading reports and formulas faster.

* The current data source now appears in the header of the Reports Explorer.

* The Advanced Report Designer now supports ignoring an ask-at-runtime condition. It also saves the report as soon as you click the Save button in the Report Layout Designer rather than when you close the Report Layout Designer.

* Expressions now use decimal rather than double as the default for literal numeric values since decimal types are more common.

* Settings that have numeric values, such as font size and top N value, now use a spinner control for easier entry.

* You can now expand and collapse the reports within tags in the Schedule Wizard.

* The new Refresh Server Collections functions in the Tools menu re-reads the data dictionary and security data. This is useful if either has been updated outside of Stonefield Query and you don't want to restart the web server.

* The step buttons at the bottom of each wizard page now have localizable tooltips.

* The Security dialog now shows the last login date and time for the selected user.

* Help is now context-sensitive. For example, if you are in step 2 of the Quick Report Wizard, choosing Help Topics from the Help file displays the help topic for step 2 of the Quick Report Wizard.

* You can now turn off table layout for the Preview window, which may help advanced layout reports appear more accurately.

* The Word Wrap setting in the Field Properties dialog is now always available, not just when Auto-fit Column is turned off, and it defaults to off. Turn this on if you want fields containing a lot of text to span multiple lines.

* The new Upload a Logo Image function in the Tools menu allows you to upload a logo image. This image appears in reports using a template that has a picture linked to the LogoImage parameter, such as the Professional * Blue with Logo template.

## Bug Fixes

* Summary reports now output correctly to Microsoft Excel; previously, all data rather than summarized data was output. Also, record counts in summary reports are now correct.

* Better handling of fields with spaces in their names.

* The file watcher is now turned off when importing, copying, and deleting reports to prevent crashing when deleting a report. Also, when reports are deleting manually (that is, the SFX file is deleted), the browser is updated.

* The description for a filter condition now formats the value properly when the field has a value converter that converts the value to DateTime and the time component is not supposed to be displayed.

* Byte, Single, and TimeSpan fields are now supported by all filter condition operators and can also be used in formulas.

* Fields that have a value converter that change the data type of the output now work properly in reports.

* Copying a report now sets the permissions for that report correctly.

* Fields with dynamic formats are now sized correctly in reports based on those formats.

* Filtering on a formula that isn't included in the report and filtering on a field in a table that isn't in the report now work properly.

* Fields involved in the expression for a calculated field now have value converters applied to them before trying to evaluate the expression.

* A summary report now longer includes a field with Display turned off.

* Saving a report that's linked to a report that no longer exists now works properly.

* Editing a report in the Advanced Report Designer and not entering a value for an ask-at-runtime filter condition no longer causes an error.

* The Is Blank filter operator now works for fields with value converters.

* If you enter an invalid expression for a filter condition, a error message about that problem is now displayed.

* Cross tab reports now properly handle turning on Percentage of Total for non-summed fields.

* If you rename a report, the SFX file is now renamed if the two are the same.

* The SFX file is now given a unique name the first time a report is saved if the default name for the file is already be used by another file.

* Sorting a report on a DateTime field that isn't formatted as date now works properly.

* Using the same DateTime field in a report more than once with a different format for each now works properly.

* Change the connection for a filter group nested inside another filter group now works properly.

* Filter conditions on DateTime fields are now saved in a non-culture specific way so there's no issue creating a report in one culture (such as Germany) and using it in another (such as the U.S.) with a different date format.

* A field using a dynamic format is now displayed correctly in a group header.

* Filtering on a table used in a report with a outer join now works better.

* Removing a field from the group header of another field now works properly.

* Editing a report in the Advanced Report Designer and then previewing it in the browser now displays the updated layout without having to restart the web server.

* In the previous version, if a tenant administrator had a user in their tenant with the full Administrator role, they could change the password of that user and log in as them. This is no
longer possible.

* A bug in which a non-admin tenant user wasn't seeing the Everyone role and couldn't save reports was fixed.

* Tables and fields are now displayed in the correct sort order when Display Real Names is turned on even when the names have delimiters.

* The Schedule Wizard no longer shows a setting for data source when there aren't multiple data
sources available. Also, the user now only sees data sources the user can access, and if the current user belongs to a tenant, they only see one data source.

* A schedule with a problem, such as referencing a report that's been deleted, no longer prevents the UI from loading.

* Outputting a report to file when previewing multiple report in separate windows now outputs the correct report.

* Clicking the Finish button in the Setup Wizard now navigates the browser to the correct page under all conditions.

* Since ask-at-runtime isn't supported for grouping formulas, that control is hidden in the filter controls in the Formula Editor.

* Changing the language in the Options dialog now works correctly.

* A bug that caused an error when previewing a report with a virtual table before saving it was fixed.

* Changing a filter condition's operator to Is Between and then running the report without entering a second value no longer causes an error.

* The information popup that appears when you hover your mouse over a report name in the Reports Explorer now correctly disappears when you move your mouse off the name. Under some conditions in the previous version, the popup would stay.

* A bug that prevented saving a new role in the Security dialog under some conditions was fixed.

* If a field in a report has a summary type, it doesn't make sense to be able to show it in a group header, so that control is now disabled.

* The Login page automatically navigates to the Setup page if no data sources have been defined and this is the first time the ADMIN user has logged in.

* An error in the custom SQL statement for a report is now handled properly.

* Moving a field that was placed under another one back up to its normal position now works properly.

* A bug in which a lower case user name caused an error when changing data source was fixed.

* The Advanced Report Designer now supports boolean ask-at-runtime conditions.

* When a user is added in the Register dialog, the email address they enter is saved as their email address.

* The Options dialog now displays the correct default template for a non-administrative user with a lower-case user name.

* Resizing your browser window now properly resizes controls in the window.

* Passing a filter condition value to a linked report now works correctly.

* Outputting a report to file when the "Output each group to separate file" setting is turned on now works properly.

* The list of reports available to link to in the Field Properties dialog now shows newly created reports.

* CSV and text output from cross-tab reports no longer has formatted number; that is, they no longer have currency, thousands, or decimal symbols.

* Grouping a quick report on DateTime fields using aggregate formatting (such as Year) now works correctly.

* Rearranging filter conditions now properly removes the connection for the new first condition.

* An "is one of" filter condition now only keeps the number of values you actually enter rather than 10, and can have more than 10 values (up to 500).

* Group sorting is now disabled for a summary report since you can use normal sorting in that case.

* You can no longer choose Highest or Lowest for a field's Summary setting if the field isn't numeric or date since that isn't supported.

* You can now use the "is one of" operator with numeric values.

* You can no longer choose the "is blank" operator when comparing to another field.
