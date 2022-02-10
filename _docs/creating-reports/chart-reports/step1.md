---
layout: default
title: Step 1 Information
nav_order: 1
parent: Creating a Chart Report
grand_parent: Creating Reports
---
The first step in this wizard is to enter the following information:

![](/assets/images/chartwizard1.png)
{% if site.has_datagroups %}
* *Show all data groups*: turn this on to see all tables in all modules in step 2 of the wizard.

* *Data group*: the module to report on. Only those modules installed on your system and you have rights to appear. This doesn't appear if *Show all data groups* is turned on.

{% endif %}
* *Name*: the name of the report. Although you can go to another next step without entering a valid name, you cannot click Finish to save the report.

* *Comments*: any comments entered here appear in the Information window for the report in the [Reports Explorer]({% link _docs/creating-reports/reports-explorer.md %}). You can expand the text area for entering comments by dragging the handle in the lower-right corner of the area.

* *Tags*: the tags for the report. Click in the Tags area to display a drop-down list of tag names. Select one from the list to add that tag to the report. To remove a tag, click the "x" to the left of its name. You can add as many tags as you wish to a report.
{% if site.has_multidatasource %}

* *Data sources*: {{ site.app_name }} allows you to report on data from more than one data source in the same report (a data source is a particular database you want to report on). To do that, click in the data sources area to display a drop-down list of data sources to include in the report. Select one from the list to add that data source to the report. To remove a data source, click the "x" to the left of its name. You can add as many data sources as you wish to a report. If none are selected, the report includes data from the currently selected data source only.
{% endif %}

Note that if the report has an [advanced layout]({% link _docs/creating-reports/advanced-layout-designer/using-the-layout-designer.md %}), a message appears informing you of that.