---
title: Gauges
layout: default
nav_order: 6
parent: Dashboard Item Settings
grand_parent: Dashboard Designer
---
# Gauges
The **Gauge** dashboard item displays a series of gauges. Each gauge can communicate two values - one with a needle and the other with a marker on the scale.

![wdd-dashboard-items-gauges](/assets/images/dashboards/img125120.png)

## Providing Data
The **Web Dashboard** allows you to bind various dashboard items to data in a virtually uniform manner. To learn more, see the [Bind Dashboard Items to Data]({% link _docs/dashboard-designer/bind-dashboard-items-to-data/index.md %}) topic.

The only difference is in the data sections that the required dashboard item has. This topic describes how to bind a **Gauge** dashboard item to data.

### Binding to Data in the Web Dashboard
The image below shows a sample Gauge dashboard item that is bound to data.

![wdd-gauge-bindings](/assets/images/dashboards/img125621.png)

To bind the Gauge dashboard item to data, click a placeholder contained in one of the available data sections and select the required data source field in the **Binding** section of the invoked [data item menu](../../ui-elements/data-item-menu.md).

The table below lists and describes the Gauge's data sections.

| Section | Processed as | Description |
|---|---|---|
| **Gauges** | Measure (both _Actual_ and _Target_ values) | Contains data items used to calculate values displayed by gauges. After you add the data item containing **actual** data, you can add the second data item (optional) that contains **target** data. If both items are provided, gauges show the difference between actual and target values, called _delta_. To learn more, see [Delta](delta.md). You can fill several data item containers in the Gauges section and use the **Values** drop-down menu to switch between the provided values. To invoke the Values menu, click the ![DashboardItems_OtherElements](/assets/images/dashboards/img20169.png) icon in the dashboard item caption. |
| **Series** | Dimension | Contains data items whose values are used to label gauges.. |


## Delta
Gauges allow you to display the difference between the _actual_ and _target_ values of a particular parameter. This difference is called **delta**.

Delta is shown with a _delta indicator_ (indicating whether the actual value is less than or greater than the target value) and _delta values_ (representing this difference as an absolute value or a variation).

![wdd-gauge-delta](/assets/images/dashboards/img125316.png)

After you add the data item containing _actual_ data, you can add the second data item (optional) that contains _target_ data. To customize settings that relate to the calculation and display of deltas, open the **Delta Options** section of the [data item menu](../../ui-elements/data-item-menu.md).

![wdd-gauge-options](/assets/images/dashboards/img125312.png)

Use it to define the conditions for displaying delta indication, specify which delta values should be displayed, and introduce the comparison tolerance.The following options are available.

| Option | Description |
|---|---|
| **Value Type** | Specifies which values should be displayed as the main delta value. Additional delta values are selected automatically. |
| **Result Indication** | Specifies the condition for displaying delta indication. |
| **Threshold Type** | Specifies the comparison tolerance in percentage values or in absolute values. |
| **Threshold Value** | Specifies the comparison tolerance value. |


## Gauge Scale
By default, the Gauge dashboard item automatically determines the range of the gauge scales based on the values they display.

![wdd-gauge-scale](/assets/images/dashboards/img125318.png)

You can override this behavior and specify maximum and minimum values on the scale. After you add the data item, open the **Scale Options** section of the [data item menu](../../ui-elements/data-item-menu.md) to customize the gauge scale.

![wdd-gauge-options](/assets/images/dashboards/img125312.png)

Then, set the minimum/maximum value mode to **Custom** and specify this value in the corresponding field. The image below shows a gauge with a minimum value of 1B and maximum 5B.

![wdd--gauge-custom-scale-interval](/assets/images/dashboards/img125319.png)

## Interactivity
To enable interaction between the Gauge and other dashboard items, you can use the interactivity features, as **Master Filtering** and **Drill-Down**.
* [Master Filtering](#masterfiltering)
* [Drill-Down](#drilldown)

### <a name="masterfiltering"/>Master Filtering
You can use the **Gauge** dashboard item as a filter for other dashboard items. To learn more about filtering concepts common to all dashboard items, see the [Master Filtering](../../interactivity/master-filtering.md) topic.

When **Master Filtering** is enabled, you can click a gauge(s) to make other dashboard items only display data related to the selected gauge(s).

![Gauges_MasterFiltering_Web](/assets/images/dashboards/img22508.png)

To enable **Master Filtering**, go to the Gauge's [Interactivity](../../ui-elements/dashboard-item-menu.md) menu and select the required Master Filtering mode.

![wdd-dashboard-items-interactivity-section](/assets/images/dashboards/img125270.png)

To reset filtering, use the **Clear Master Filter** button (the ![wdd-master-filtering-icon](/assets/images/dashboards/img125072.png) icon) in the Gauge's [caption](../../dashboard-layout/dashboard-item-caption.md).

### <a name="drilldown"/>Drill-Down
The built-in drill-down capability allows you to change the detail level of data displayed in dashboard items on the fly. To learn more about drill-down concepts common to all dashboard items, see the [Drill-Down](../../interactivity/drill-down.md) topic.

When drill-down is enabled, you can click a gauge to view the details.

![Gauges_DrillDown_Web](/assets/images/dashboards/img22509.png)

Drill-down requires that the **Series** section contains several dimensions at the top, from the least detailed to the most detailed dimension.

![wdd-gauge-drill-down-arguments-section](/assets/images/dashboards/img125778.png)

> [!NOTE]
> In OLAP mode, you can perform drill-down for either a hierarchy data item or several dimension attributes.

To enable **Drill-Down**, go to the Gauge's [Interactivity](../../ui-elements/dashboard-item-menu.md) menu and turn the **Drill-Down** option on.

![wdd-dashboard-items-interactivity-section](/assets/images/dashboards/img125270.png)

To return to the previous detail level, click the **Drill Up** button (the ![wdd-drill-up-icon](/assets/images/dashboards/img125074.png) icon) in the Gauge's [caption](../../dashboard-layout/dashboard-item-caption.md).

## Layout
The Gauge dashboard item allows you to specify the number of columns or rows by which gauges are arranged. For example, the following image shows gauges arranged into 3 columns.

![wdd-gauges-fixed-columns](/assets/images/dashboards/img125649.png)

To control how gauges are arranged, use the **Layout** section in the Gauge's [Options](../../ui-elements/dashboard-item-menu.md) menu.

![wdd-pie-content-arrangement](/assets/images/dashboards/img125199.png)

The following modes are available.

| Arrangement Mode | Description |
|---|---|
| **Auto** | Automatically resizes gauges to fit within the dashboard item. |
| **Fixed Rows** | Allows you to arrange gauges in a specific number of rows. |
| **Fixed Columns** | Allows you to specify the number of columns in which gauges are arranged. |

To specify the number of rows/columns, use the **Line Count** field.


## Style
The Gauge dashboard item allows you to select the gauge style.

![wdd-gauges-style](/assets/images/dashboards/img125775.png)

The following types are available.
* Full Circular
* Half-Circular
* Left-Quarter Circular
* Right-Quarter Circular
* Three-Fourths Circular
* Linear Horizontal
* Linear Vertical

To select the gauge style, use the style icons in the Gauge [Options](../../ui-elements/dashboard-item-menu.md) menu.

![wdd-gauge-style-options](/assets/images/dashboards/img125777.png)