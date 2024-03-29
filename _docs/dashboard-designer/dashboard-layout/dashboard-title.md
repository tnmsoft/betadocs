---
title: Dashboard Title
layout: default
nav_order: 1
parent: Dashboard Layout
grand_parent: Dashboard Designer
---
# Dashboard Title
The **Dashboard Title** is located at the top of the [dashboard surface]({% link _docs/dashboard-designer/ui-elements/dashboard-surface.md %}) and can contain text and image content.

![wdd-dashboard-title](/assets/images/dashboards/img126004.png)

To change title settings, invoke the [dashboard menu]({% link _docs/dashboard-designer/ui-elements/dashboard-menu.md %}) and open the **Title** page.

![wdd-title-page](/assets/images/dashboards/img126668.png)

Here you can specify the following options.
* **Text** - Specifies the dashboard title text.
* **Visible** - Specifies whether or not the dashboard title is visible.
* **Alignment** - Specifies the alignment of the dashboard title.
* **Include Master Filter** - Specifies whether or not to show the state of master filter items in the dashboard title. 
	
	When you hover over the filter icon (![DashboardTitle_MasterFilterIcon](/assets/images/dashboards/img23138.png)), all master filters applied to the dashboard are displayed in the invoked popup.
	
	![wdd-title-master-filter](/assets/images/dashboards/img126020.png)
* **Image** - Allows you to specify the image displayed within the dashboard title. The dashboard definition will contain an image as a byte array.

The dashboard title can contain the following command buttons.
* **Export To** - Allows you to export the entire dashboard.
* **Parameters** - Allows you to modify dashboard parameter values. To learn more about parameters, see [Parameters]({% link _docs/dashboard-designer/data-analysis/dashboard-parameters.md %}).