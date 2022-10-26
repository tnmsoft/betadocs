---
title: Pies
layout: default
nav_order: 4
parent: Dashboard Item Settings
grand_parent: Dashboard Designer
---
# Pies
The Pie dashboard item displays a series of pies or donuts that represent the contribution of each value to a total.

![wdd-dashboard-items-pies](/assets/images/dashboards/img125125.png)

## Providing Data
The **Web Dashboard** allows you to bind various dashboard items to data in a virtually uniform manner. To learn more, see the [Bind Dashboard Items to Data](../../bind-dashboard-items-to-data.md) topic.

The only difference is in the data sections that the required dashboard item has. This topic describes how to bind a **Pie** dashboard item to data.

### Binding to Data in the Web Dashboard
The image below shows a sample Pie dashboard item that is bound to data.

![wdd-pies-bindings](..//assets/images/dashboards/img125650.png)

To bind the Pie dashboard item to data, click a placeholder contained in one of the available data sections and select the required data source field in the **Binding** section of the invoked [data item menu](../../ui-elements/data-item-menu.md).

The table below lists and describes the Pie's data sections.

| Section | Processed as | Description |
|---|---|---|
| **Values** | Measure | Contains data items that define the share of pie segments. In case of negative measure values, Pie uses their absolute values. |
| **Arguments** | Dimension | Contains data items that provide values used to label pie segments. |
| **Series** | Dimension | Contains data items whose values are used to label pie charts. |


## Interactivity
To enable interaction between the Pie and other dashboard items, you can use interactivity features like **Master Filtering** and **Drill-Down**.
* [Master Filtering](#masterfiltering)
* [Drill-Down](#drilldown)

### <a name="masterfiltering"/>Master Filtering
You can use the Pie dashboard item as a filter for other dashboard items. To learn more about filtering concepts common to all dashboard items, see the [Master Filtering](../../interactivity/master-filtering.md) topic.

The Pie dashboard item supports filtering by **arguments**, **series** or **points**.
* Filtering **by arguments** allows you to make other dashboard items display only data related to selected argument values by clicking a pie segment.
	
	![Pies_FilteringByArguments_Web](..//assets/images/dashboards/img22485.png)
* When filtering **by series** is enabled, you can click a pie to make other dashboard items display only data related to the selected pie.
	
	![Pies_FilteringBySeries_Web](..//assets/images/dashboards/img22486.png)
* When filtering **by points** is enabled, you can click a single pie segment to make other dashboard items display only data related to the selected segment.
	
	![wdd-pies-master-filter-points](..//assets/images/dashboards/img125780.png)

To configure filtering type, open the Pie's [Interactivity](../../ui-elements/dashboard-item-menu.md) menu and select **Arguments**, **Series** or **Points** as a target dimension.

![wdd-chart-interactivity-set-points](..//assets/images/dashboards/img125061.png)

To reset filtering, use the **Clear Master Filter** button (the ![wdd-master-filtering-icon](..//assets/images/dashboards/img125072.png) icon) in the Pie's [caption](../../dashboard-layout/dashboard-item-caption.md).

### <a name="drilldown"/>Drill-Down
The drill-down capability allows you to change the detail level of data displayed in the Pie dashboard item. To learn more about drill-down concepts common to all dashboard items, see the [Drill-Down](../../interactivity/drill-down.md) topic.

The Pie supports drill-down on **argument** or **series** values.
* To drill down on **arguments**, click a pie segment to view a detail diagram for the corresponding argument value.
	
	![Pies_DrillDownOnArguments_Web](..//assets/images/dashboards/img22487.png)
	
	Drill-down on arguments requires that the **Arguments** section contains several data items, from the least detailed to the most detailed item.
	
	![wdd-pies-interactivity-arguments](..//assets/images/dashboards/img125781.png)
* When drill-down on **series** is enabled, you can click a pie chart to view a detail diagram for the corresponding series value.
	
	![Pies_DrillDownOnSeries_Web](..//assets/images/dashboards/img22488.png)
	
	Drill-down on series requires that the **Series** section contains several data items, from the least detailed to the most detailed item.
	
	![wdd-pies-interactivity-series](..//assets/images/dashboards/img125782.png)

> [!NOTE]
> In OLAP mode, you can perform drill-down for either a hierarchy data item or several dimension attributes.

To specify drill-down type, go to the Pie's [Interactivity](../../ui-elements/dashboard-item-menu.md) menu and set **Arguments** or **Series** as the target dimension.

![wdd-chart-interactivity-set-series](..//assets/images/dashboards/img125060.png)

To return to the previous detail level, click the **Drill Up** button (the ![wdd-drill-up-icon](..//assets/images/dashboards/img125074.png) icon) in the Pie's [caption](../../dashboard-layout/dashboard-item-caption.md).


## Layout
The Pie dashboard item allows you to specify the number of columns or rows in which pies are arranged. For example, the following image show pies arranged into 3 columns.

![wdd-pie-content-arr-fixed-column.png](..//assets/images/dashboards/img125197.png)

To control how cards are arranged, use the **Layout** section in the Pie's [Options](../../ui-elements/dashboard-item-menu.md) menu.

![wdd-pie-content-arrangement](..//assets/images/dashboards/img125199.png)

The following modes are available.

| Arrangement Mode | Description |
|---|---|
| **Auto** | Automatically resizes pies to fit within the dashboard item. |
| **Fixed Rows** | Allows you to arrange pies in a specific number of rows. |
| **Fixed Columns** | Allows you to specify the number of columns in which pies are arranged. |

To specify the number of rows / columns, use the **Line Count** field.


# Labels
Pies display **data labels** that contain descriptions for pie segments, and provide **tooltips** with additional information.

![wdd-pie-labels](..//assets/images/dashboards/img125620.png)

To configure data labels and tooltips, open the Pie's [Options](../../ui-elements/dashboard-item-menu.md) menu and go to the **Labels** section.

![wdd-pies-data-labels-options](..//assets/images/dashboards/img125618.png) ![wdd-pies-tooltips-options](..//assets/images/dashboards/img125619.png)

Here you can set argument, value, percent or their combinations as data labels or tooltips.


# Style
The Pie dashboard item allows you to select whether diagrams should be painted as **pies** or **donuts**.

![wdd-pie-style-pie](..//assets/images/dashboards/img125202.png)![wdd-pie-style-donut](..//assets/images/dashboards/img125201.png)

To select the diagram style, go to the **Style** section of the Pie's [Options](../../ui-elements/dashboard-item-menu.md) menu and use the **Pie** or **Donut** buttons.

![wdd-pie-style-settings](..//assets/images/dashboards/img125200.png)