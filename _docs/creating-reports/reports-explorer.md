---
layout: default
title: The Reports Explorer
nav_order: 1
parent: Creating Reports
---

The Reports Explorer appears as follows:

![](/assets/images/reportsexplorer.png)

The menu across the top has the following functions:

* *Home*: displays the Reports Explorer.

* *Scheduler*: displays a list of [scheduled reports]({% link _docs/configuration/scheduling.md %}).

* *New*: contains functions to create a new report (if you're using a [Report Designer license]({% link _docs/licensing.md %}); users with Report Viewer licenses cannot create reports) and a new schedule (if you have permission to create schedules).

* *Tools*: contains the [Tags]({% link _docs/creating-reports/tags.md %}), [Options]({% link _docs/configuration/configuration.md %}), [Formulas]({% link _docs/creating-reports/formulas.md %}), [Templates]({% link _docs/creating-reports/templates.md %}), [Manage Reports]({% link _docs/configuration/managing-reports.md %}), [Security]({% link _docs/configuration/security.md %}), [Change Password]({% link _docs/configuration/change-password.md %}), {% if site.has_multidatasource %} [Change Data Source]({% link _docs/configuration/selecting-a-datasource.md %}), {% endif %} [Import Report]({% link _docs/creating-reports/importing-and-exporting-reports.md %}), [Export Report]({% link _docs/creating-reports/importing-and-exporting-reports.md %}), [Setup]({% link _docs/configuration/manage-licenses.md %}),  [Download application log]({% link _docs/reference/support-package.md %}), [Download Support Package]({% link _docs/reference/support-package.md %}), and [Upload a Logo Image]({% link _docs/configuration/adding-a-logo.md %}) functions. Note that some of these functions are only available to administrator users.

* *Help*: has functions to display help, {% if site.has_support_center %} go to the Technical Support page, {% endif %} submit a [support ticket]({% link _docs/technical-support.md %}), display the About dialog, or launch the Reports Explorer training.

* Log off: logs you off and display the [Login page]({% link _docs/logging-in.md %}).

Below the menu are controls for the selected report. To select a report, click in the space to the right of its name in the reports list.

![](/assets/images/currentreport.png)

The name of the report appears at the top. An icon indicates the report type:

* ![](/assets/images/quickreporticon.png): a quick report, a row-and-column style report that's the most common type.

* ![](/assets/images/labelicon.png): a label report, used for address labels, bar code labels, product labels, etc.

* ![](/assets/images/crosstabicon.png): a cross-tab report, similar to a pivot table in Microsoft Excel.

* ![](/assets/images/charticon.png): a chart report, showing a bar graph, pie chart, line graph, etc.

* ![](/assets/images/dashboard.png): a dashboard, which includes other reports or charts.

* ![](/assets/images/batchreporticon.png): a batch report, which combines other reports into a single output file.


Below that is a toolbar with functions for the report:

![](/assets/images/reporttoolbar.png)

Note that the Edit and Copy buttons only appear if you're using a [Report Designer license]({% link _docs/licensing.md %}) since users with Report Viewer licenses cannot edit or copy reports. When a report viewer license is in use, the edit button is replaced with an Edit filters button ![](/assets/images/editfiltersbutton.png) instead.

Information about the report appears to the right of the toolbar: the tags associated with it, who created it and when, who last modified it and when, and comments.

Below the current report section is the reports list showing which reports you can access. It displays an icon indicating the type of report. You can preview a report by clicking its name.

The list is organized by [tag]({% link _docs/creating-reports/tags.md %}). Although you can create as many tags as you wish, one tag is automatically created for you: All Reports, which automatically includes all reports. Because a report can have more than one tag, it might appear in the Reports Explorer more than once. To hide or show the reports for a tag, click the tag bar. For example, in the image above, the Drilldown Tests and New/Modified Reports tags are collapsed but the Labels tag is expanded. The bar also shows the number of reports for the tag.

If you have a lot of reports, it might be hard to find the one you're interested in amongst all the reports in the Reports Explorer. Type something the *Search for Reports* box to display a list of all reports containing that text somewhere in the name or comments of the report. The list contains buttons to edit and preview the report.

![](/assets/images/reportsexplorersearch.png)

If you want to filter the reports displayed in the Reports Explorer to only those using certain tags, click *Flat View*. Click *Folder View* to return to the display showing reports grouped by tag.

![](/assets/images/flatview.png)

Reports in flat view are displayed in alphabetical order without being grouped by tag. To display only reports using a specific tag, click that tag's name in the list at the left; a check mark appears beside the tag. To select reports using more than one tag, click on another tag. As you can see, in this case, only one report uses both of the selected tags:

![](/assets/images/flatview_two_tags.png)

If you want to see reports that use either rather than both tags, click the *Any* button. Click *All* to return to displaying only reports that use all selected tags. Click a tag's name again to turn off its check mark and not use it as a filter.

The bottom of the Reports Explorer shows the data source used for reports (a data source is a particular database you want to report on). {% if site.has_multidatasource %} You can change to a different data source any time by choosing the Change Data Source function from the Tools menu. {% endif %}