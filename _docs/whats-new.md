---
layout: default
title: What's New in this Release
nav_order: 2
parent: Home
---

# Version 1.1

* A new export option, [Create Tabbed Document]({% link _docs/creating-reports/exporting.md %}), allows you to combine separate group files in to a single spreadsheet. The option is only available when outputting to Excel format.

* A new [Update filter value on run]({% link _docs/creating-reports/filtering/including-records.md %}) option for filter conditions allows you to update the default value for an ask-at-runtime prompt with the latest value used to run the report.

* If you turn on [ask-at-runtime]({% link _docs/creating-reports/filtering/including-records.md %}) for an expression based filter, the expression is now evaluated and used as the default value for the value prompt.

* You can now define parameters in a [report template]({% link _docs/creating-reports/templates.md %}), and the parameters will be added to any report that uses the template. This allows you to create templates that prompt the user for a value, and display or use that value somewhere when running the report. 

* You can now use a cron expression as the trigger for a [schedule]({% link _docs/configuring/scheduling.md %}).

* You can now enter more text for the [title]({% link _docs/creating-reports/quick-reports/step5.md %}) of a report.

* [Tags]({% link _docs/creating-reports/tags.md %}) that aren't accessible or have been deleted are now removed from a report definition when exporting.

* When outputting a cross-tab to an Excel pivot table, the columns are now named using the column headings in the report.

* Improved loading performance and support for large reports in the advanced layout editor.

* Improved support for executing stored procedures with "EXEC" in a [SQL Passthrough]({% link _docs/creating-reports/sql-passthrough.md %}) report.

* Is-one-of filter conditions with no values are now automatically ignored when running a report. 

* When a report is deleted, any schedule that used that report is now automatically updated.

## Bug Fixes

* Fixed a bug with compound filter conditions not working correctly when the query for a report is split.

* Fixed a bug with summary values on charts not handling mixed case values.

* Fixed a bug with the Top N option not working properly for chart reports.

* Fixed a bug with reports using old/saved parameter values when running instead of the entered value.

* Fixed a bug with filter groups getting removed when "is between" filter conditions are automatically converted to a date range. 

* Fields with a lot of text now automatically force Word Wrap to be on. This works around a GDI+ error that occurs otherwise.

* Fixed a bug with custom SQL Statements not handling parameter values properly.

* Fixed an issue with the Contains operator for a filter not working on calculated values.

* Fixed a bug with automatic parameter naming for SQL Passthrough reports.

* Fixed a bug with reports containing the same field more than once.
