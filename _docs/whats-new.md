---
layout: default
title: What's New in this Release
nav_order: 2
parent: Home
---

# Version 1.0

* The first time a user [logs in]({% link _docs/logging-in.md %}), they are now prompted to take a tour of the reports explorer.

* Added new [template]({% link _docs/creating-reports/templates.md %}) objects, "GroupFooterSummaryTypeTemplate" and "SummaryFieldTypeTemplate". These allow you to display the summary type being performed in a group footer or report footer respectively. See the new "Standard with Summary Type" template for an example of how to use it. 

* [Administrators]({% link _docs/configuration/security.md %}) can now restrict acccess to email settings.

* You can now change the location of point labels for Pie, Bar, and Line [charts]({% link _docs/creating-reports/chart-reports/step5.md %}).

* You can now add a shadow to chart types that support it.

* Chart reports now support using a date field as the Category.

* The [advanced report designer]({% link _docs/creating-reports/advanced-layout-designer/index.md %}) can now be used to edit the layout of Charts.

* You can now set [templates]({% link _docs/creating-reports/templates.md %}) for a chart report. The default template for charts is the new basic template called Standard Chart.

* [Cross-tab reports]({% link _docs/creating-reports/cross-tab-reports/index.md %}) now support templates without a header band.

* Cross-tab reports now support multiple embedded [subreports]({% link _docs/creating-reports/subreports.md %}).

* [Formulas]({% link _docs/creating-reports/formulas.md %}) created when inside a report wizard will automatically be added to the report.

* You can now search formulas using the *real* name of the formula field (e.x. CALC20220193203922).

* When working with date values in a [filter condition]({% link _docs/creating-reports/filtering/including-records.md %}), the entire date is now selected when you move to a date input. This allows you to immediately start typing a new value and it will automatically clear the old value. 

* You now get a warning if you enter an invalid date range for an "is between" filter condition.

## Bug Fixes

* Fixed a problem with email not using SSL, even if the option was turned on.

* Fixed an issue with the connection string plugin not appearing under some circumstances.

* Fixed an issue with empty tags being created when importing a report. 

* Fixed a bug with embedded subreports not working correctly in a cross-tab.

* Fixed an issue with horizontal pagination not working property in a cross-tab.

* Scheduled tasks should no longer temporarily lock a license.

* Fixed a bug that caused date formats to be applied to a summary column.

* Fixed a bug that occurred when uploading a logo image if tenants are supported.

* Fixed a display issue in Security that caused user names to appear on the same line in the user list.

* Fixed an issue with Exclusion filters not appearing in report wizards.

* Fixed an issue with field width when using metric units.

