---
layout: default
title: Subreports
nav_order: 13
parent: Creating Reports
---
A report can have one or more subreports. How subreports behave works a little differently in chart reports than it does in quick and cross-tab reports.

## Quick and cross-tab reports
For quick and cross-tab reports, subreports can either be linked to a field, in which case the field appears to be hyperlinked and clicking it in the Preview window runs the subreport, or unlinked, in which case they appear in the header or footer of the report. This allows you, for example, to add a chart to a quick report.

The *Subreport Properties* button in step 5 of the report wizards displays the Subreport Properties dialog so you can manage subreports. This button is disabled if you haven't selected any fields for the report.

![](/assets/images/subreportproperties.png)

To add a subreport to the report, click the ![](/assets/images/addround.png) button. The dialog expands and displays the following options:

* *Linked report type*: specifies how the subreport is linked to the main report. The choices are:

    * *Embedded*: this means the subreport always appears; you don't have to click a linked field. It may be linked to a field or not.

    * *Drilldown*: this means the subreport is linked to a field and doesn't appear until you click the hyperlink for the field; when you do that, it appears within the report, right under the field you clicked. Clicking the link again hides the subreport.

    * *Drillthrough*: this means the subreport is linked to a field and appears in another preview window when you click the hyperlink for the field.

    * *Side By Side*: this works likes *Drillthrough*, but instead of a separate preview window, the current preview window is split in two, with the subreport appearing to the right of the parent report.

* *Linked to a field*: this option, which only appears when *Linked report type* is set to *Embedded*, specifies whether the subreport is linked to a field or not. If this is turned off, the subreport appears in either the report header or footer. If this is turned on and *Linked field* (discussed next) is set to a field, the subreport appears below that field in the report.

* *Linked field*: this is the field the subreport is linked to.

* *Location*: for an unlinked subreport, the choices are *Report header* and *Report footer*. For a linked subreport, the choices are *Group header* and *Group footer* if the field is grouped. If the field isn't grouped, this option doesn't appear because the only place the subreport can appear in below the field in the detail band.

* *Report*: the name of the report to use as a subreport. Click the "..." button to display a list of existing reports, organized by tag. Select the desired report to use as a subreport from the list.

The section below the subreport name allows you to pass values to the ask-at-runtime filter conditions of the subreport. See the **Values to pass** section below for information.

## Chart reports
For chart reports, subreports are linked to a data point (such as a bar in a bar chart); clicking the data point runs the subreport.

The *Drillthrough Properties* button in step 5 of the Chart Report Wizard displays the Drillthrough Properties dialog so you can manage subreports. This button is disabled if you haven't selected any fields for the report.

![](/assets/images/drillthroughproperties.png)

To add a subreport to the report, click the ![](/assets/images/addround.png) button. The dialog expands and allows you to select a report to use as a subreport. Click the "..." button to display a list of existing reports, organized by tag. Select the desired report to use as a subreport from the list.

## Values to pass
For quick, cross-tab, and chart reports, the section below the subreport name allows you to pass values to the ask-at-runtime filter conditions of the subreport. Without this option, when the report is run, the subreport prompts you for any of its ask-at-runtime filter conditions, which may not make sense. For example, suppose you have a customer report and you've added as a subreport a report showing sales by customer. The subreport has an ask-at-runtime filter condition on the customer number, so for each company, the subreport runs and asks you for the customer number. That seems odd, because it's supposed to be for the customer shown in the report and now it wants you to specify which customer. To make this more seamless, you want to tell the subreport which customer to use. You do that by specifying what value to pass to the ask-at-runtime filter condition of the subreport. In this case, you'd specify that the customer number should be passed to the subreport. Since that value is passed, the report doesn't need to ask you for the customer number, and simply displays the sales for each customer.

The list shows each of the ask-at-runtime conditions for the subreport. The first column shows the field used in the ask-at-runtime condition, the second column allows you to specify the type of value to pass to the report, and the third column specifies the value to pass. The choices for the *Type* column are:

* *Filter Condition*, which means this report contains the same ask-at-runtime filter condition as the subreport, and you want the value you specify when you run this report passed to the subreport. For example, if both reports have an ask-at-runtime filter condition on the order date, you'd want to use the same order date range you specify when you run this report used for the subreport. So, choose Filter Condition and select the field used for the condition in the *Value to pass* drop-down list.

* *Field*, which means you want to pass the value of the field specified in the *Value to pass* column for the current record. For example, for each customer in the report, you want to pass the customer number to the ask-at-runtime filter condition on customer number to the subreport, so choose Field and select the Customer Number field in the *Value to pass* drop-down list.

* *Ignore this condition*, which means you want to ignore this condition (that is, act like you clicked the *Ignore this condition* option in the filter value dialog) and not display the dialog asking you for the value for this condition.

Note that only fields selected for the report appear in the list of fields in the *Value to pass* drop-down list, so be sure to include the desired field in the report. If you don't want that field to actually appear in the report, turn off the *Display in report* setting for that field.
