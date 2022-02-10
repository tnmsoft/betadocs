---
layout: default
title: Creating a Dashboard
nav_order: 10
has_children: true
parent: Creating Reports
---
A dashboard is a set of reports that appears in its own window, outside of {{ site.app_name }}. In fact, when a dashboard is run, the normal {{ site.app_name }} user interface may not appear.

![](/assets/images/dashboardpreview.png)

You typically run a dashboard to view important information about your business. You may run a dashboard at the start of the day and leave the dashboard window open all day, or open and close it as you see fit. The charts in the dashboard refresh themselves at an interval you specify (the default is every 30 seconds) so the data is always current.

You run a dashboard by previewing it. Note that the preview displays in a separate tab in your browser and doesn't include the normal preview toolbar since the functions in that toolbar don't apply to dashboards.

You can create a shortcut on your desktop that displays the dashboard by dragging from the address bar of your browser to your desktop. Simply double-click that shortcut to open the dashboard in your browser (note that you may be asked to log in).

There are three steps in the Dashboard Wizard:

* *[Step 1: Information]({% link _docs/creating-reports/dashboards/step1.md %})*: specify the dashboard name, comments, and tags.

* *[Step 2: Report Selection]({% link _docs/creating-reports/dashboards/step2.md %})*: choose the reports for the dashboard.

* *[Step 3: Dashboard Layout]({% link _docs/creating-reports/dashboards/step3.md %})*: specify how the reports are arranged.

To move from one step to another in the wizard, click the next or previous buttons or choose a specific step number from the toolbar at the bottom.

The bottom right of the wizard has buttons to cancel editing the dashboard or finish and save it.
