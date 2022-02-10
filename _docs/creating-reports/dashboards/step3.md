---
layout: default
title: Step 3 Dashboard Layout
nav_order: 3
parent: Creating a Dashboard
grand_parent: Creating Reports
---
Step 3 allows you to control the layout of the reports in the dashboard and how often they refresh.

![](/assets/images/dashboardwizard3.png)

By default, {{ site.app_name }} lays out reports horizontally, from left to right, in the order they appear in the *Selected reports* list in step 2. You can rearrange the order by dragging a report to the desired position, either beside or below another report.

To change the properties of a report in the dashboard, click the report. The properties available are:

* *Width*: the width of the report in the dashboard. This is a relative value; if one report has a width of 1 and another has a width of 2, the second one is twice as wide as the first.

* *Height*: the height of the report in the dashboard. This is a relative value; if one report has a height of 1 and another has a height of 2, the second one is twice as tall as the first.

* *Refresh interval*: a dashboard automatically refreshes the data in each of its reports at an interval you determine. The default is every 30 seconds but you can set it to a different value if you wish.