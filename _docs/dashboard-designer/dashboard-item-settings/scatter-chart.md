---
title: Scatter Chart
layout: default
nav_order: 2
parent: Dashboard Item Settings
grand_parent: Dashboard Designer
---
# Scatter Chart
The topics in this section describe the features available in the **Scatter Chart** dashboard item, and explain how to create and customize scatter charts in the Web Dashboard.

![wdd-dashboard-items-scatter-chart](/assets/images/dashboards/img125128.png)


## Providing Data
The **Web Dashboard** allows you to bind various dashboard items to data in a virtually uniform manner. To learn more, see the [Bind Dashboard Items to Data]({% link _docs/dashboard-designer/bind-dashboard-items-to-data/index.md %}) topic.

The only difference is in the data sections that the required dashboard item has. This topic describes how to bind a **Scatter Chart** dashboard item to data.

### Binding to Data in the Web Dashboard
The image below shows a sample Scatter Chart dashboard item that is bound to data.

![wdd-scatter-chart-bindings](/assets/images/dashboards/img125600.png)

To bind the Scatter Chart dashboard item to data, click a placeholder contained in one of the available data sections and select the required data source field in the **Binding** section of the invoked [data item menu]({% link _docs/dashboard-designer/ui-elements/data-item-menu.md %}).

The table below lists and describes the Scatter Chart's data sections.

| Section | Processed as | Description |
|---|---|---|
| **X-Axis** | Measure | Contains the data item against which the X-coordinates of data points are calculated. |
| **Y-Axis** | Measure | Contains the data item against which the Y-coordinates of data points are calculated. |
| **Weight** | Measure | Contains the data item whose values are used to calculate the weight of data points. |
| **Arguments** | Dimension | Contains data items that provide scatter chart arguments used to create data points. |


## Interactivity
To enable interaction between the Scatter Chart and other dashboard items, you can use the interactivity features, as **Master Filtering** and **Drill-Down**.
* [Master Filtering](#masterfiltering)
* [Drill-Down](#drilldown)

### <a name="masterfiltering"/>Master Filtering
The Web Dashboard allows you to use any data aware dashboard item as a filter for other dashboard items. To learn more about filtering concepts common to all dashboard items, see the [Master Filtering](../../interactivity/master-filtering.md) topic.

The Scatter Chart dashboard item supports filtering by points that correspond to specific argument values or their combinations.

When Master Filtering is enabled, you can click a point (or multiple points) to make other dashboard items only display data related to the selected point(s).

![wdd-grid-interactivity-master-filtering](/assets/images/dashboards/img125268.png)

To enable **Master Filtering**, go to the Scatter Chart's [Interactivity]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu and select the required Master Filtering mode.

![wdd-dashboard-items-interactivity-section](/assets/images/dashboards/img125270.png)

To reset filtering, use the **Clear Master Filter** button (the ![wdd-master-filtering-icon](/assets/images/dashboards/img125072.png) icon) in the Scatter Chart's [caption]({% link _docs/dashboard-designer/dashboard-layout/dashboard-item-caption.md %}).

### <a name="drilldown"/>Drill-Down
The Drill-Down feature allows you to change the detail level of data displayed in dashboard items. To learn more about concepts common to all dashboard items, see the [Drill-Down](../../interactivity/drill-down.md) topic.

When drill-down is enabled, you can click a point to view the details (or double-click a point in case of enabled Master Filtering).

![wdd-grid-interactivity-drill-down](/assets/images/dashboards/img125267.png)

Drill-down requires that the **Arguments** section contains several dimensions, from the least to the most detailed dimension.

![wdd-scatter-chart-arguments-section](/assets/images/dashboards/img125269.png)

> [!NOTE]
> In OLAP mode, you can perform drill-down for either a hierarchy data item or several dimension attributes.

To enable **Drill-Down**, go to the Scatter Chart's [Interactivity]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu and turn the **Drill-Down** option on.

![wdd-dashboard-items-interactivity-section](/assets/images/dashboards/img125270.png)

To return to the previous detail level, click the **Drill Up** button (the ![wdd-drill-up-icon](/assets/images/dashboards/img125074.png) icon) in the Scatter Chart's [caption]({% link _docs/dashboard-designer/dashboard-layout/dashboard-item-caption.md %}).

## Legend
A legend is an element of a scatter chart that identifies chart points (for instance, colored points corresponding to argument values).

![wdd-scatter-chart-legend](/assets/images/dashboards/img125606.png)

To customize legend options, go to the Scatter Chart's [Options]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu and open the **Legend** section.

![wdd-scatter-chart-legend-options](/assets/images/dashboards/img125601.png)

The following settings are available.

| Setting | Description |
|---|---|
| **Show Legend** | Specifies whether or not to show a legend. |
| **Inside Diagram** | Locates a legend inside or outside the Scatter Chart. |
| **Position** | Sets a legend position and orientation. |


## Axes
Scatter Chart X and Y-axes are numerical axis of values. You can specify various axes settings to change visual data presentation.

To access X and Y-axis settings, go to the Scatter Chart's [Options]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu and open the **Axis X** or **Axis Y** section.

Here you can configure the visibility of axes, their title and grid lines, reverse the axes, etc.

The following options are available.

![wdd-scatter-chart-axis-options](/assets/images/dashboards/img125602.png)

| Options | Description |
|---|---|
| **Always show zero level** | Specifies whether or not the axis' zero level is visible. If this option is unchecked, the visible axis range is defined based on the values plotted in the chart. Note that the **Axis X** section does not contain the **Always show zero level** option. |
| **Reverse** | Allows you to reverse the axis. If the axis is reversed, its values are ordered from top to down. |
| **Grid Lines** | Allows you to hide and show grid lines for the axis. |
| **Visible** | Allows you to hide and show the axis. |
| **Title** | Allows you to hide and show the axis title. You can choose whether to use the default text or specify a custom string using the **Title Text** option. |
| **Logarithmic scale** | Specifies whether or not the axis should display its numerical values using a logarithmic scale. The combo box next to this option allows you to select the logarithmic base from one of the predefined values. |


## Orientation
You can rotate the Scatter Chart so that the [X-axis](axes.md) becomes vertical, and the [Y-axis](axes.md) becomes horizontal.

To rotate a Scatter Chart in the Web Dashboard, open the Scatter Chart's [Options]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu and go to **Common** section. Then, turn the **Rotated** option on.

![wdd-scatter-chart-rotate](/assets/images/dashboards/img125603.png)


## Labels
The Scatter Chart can display **point labels** that contain descriptions for data points, and provide **tooltips** with additional information.

![wdd-scatter-chart-point-label](/assets/images/dashboards/img125604.png)

To manage the visibility of point labels, open the Scatter Chart's [Options]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu and go to the **Labels** section. Then, turn the **Show Point Labels** option on.

Here you can specify the type of content displayed within point labels, configure label overlap mode and set the orientation of point labels.

The following options are available.

![wdd-scatter-chart-labels-option](/assets/images/dashboards/img125607.png)

| Options | Description |
|---|---|
| **Show Point Labels** | Specifies whether or not to show point labels for the current series. |
| **Content** | Specifies the type of content displayed within point labels. You can select _Value_, _Argument_, _Series Name_ or _Argument and Value_ options. |
| **Overlapping Mode** | Specifies the label overlap mode. You can hide overlapping labels or disable a resolving algorithm. |
| **Orientation** | Specifies the orientation of point labels. You can set a default orientation or rotate point labels 90 degrees clockwise or counter clockwise. |
| **Position** | Specifies the position of point labels relative to bars. Point labels can be displayed inside or outside bars. |


## Conditional Formatting

Use conditional formatting to highlight points in a Scatter Chart dashboard item.

![web-cf-scatter-chart-main](/assets/images/dashboards/web-cf-scatter-chart-main.png)

### Supported Format Rules

You can use the following data in rule calculations:

- [measures](../../bind-dashboard-items-to-data/bind-dashboard-items-to-data-in-the-web-dashboard.md) from the **X and Y axis** sections 
- [measures](../../bind-dashboard-items-to-data/bind-dashboard-items-to-data-in-the-web-dashboard.md) from the **Weight** section
- [dimensions](../../bind-dashboard-items-to-data/bind-dashboard-items-to-data-in-the-web-dashboard.md) from the **Arguments** section 
- hidden measures 

Format conditions that can be applied to different data item types are as follows:
* numeric 
	* **Value** 
	* **Top-Bottom**
	* **Average**
	* **Expression** 
	* **Color Ranges**
	* **Gradient Ranges**
* string 
	* **Value** (with the condition type set to _Equal To_, _Not Equal To_ or _Text that Contains_)
	* **Expression**
* date-time 
	* **Value**
	* **A Date Occurring** (for dimensions with a continuous date-time group interval)
	* **Expression**
	* **Color Ranges**
	* **Gradient Ranges**


Refer to the following topic for more information about format condition types: [Conditional Formatting in Web Dashboard](../../appearance-customization/conditional-formatting.md).

### Create and Edit a Format Rule 

You can create and edit format rules in the **Conditional Formatting** section that is located in the following places:

* The dashboard item's [Options]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu

* The [data item menu]({% link _docs/dashboard-designer/ui-elements/data-item-menu.md %})

Refer to the following topic for information on how to create and edit format rules: [Conditional Formatting in Web Dashboard](../../appearance-customization/conditional-formatting.md).

### Format Condition Settings Specific to Scatter Charts

Specify appearance settings and set the condition's value to create a format rule. Available settings depend on the selected format condition type.

The image below displays the **Value** rule settings. The condition colors bubbles if their weight exceeds 200.

![web-scatter-chart-cf-appearance-settings-dialog](/assets/images/dashboards/web-scatter-chart-cf-appearance-settings-dialog.png)

You can apply one of the predefined colors or set a custom color for this condition.

Go to the rule's **Legend** section and set the **Caption** field to specify the legend's text. It enables the **Display in Legend** option and the Scatter Chart item displays information about the applied rule in the legend.

The image below displays the Scatter Chart item with the applied **Greater Than** format rule. The **Display in Legend** option is activated and the rule's caption is displayed in the legend:

![web-scatter-chart-conditional-formatting](/assets/images/dashboards/web-scatter-chart-conditional-formatting.png)

For Range format rules, the legend display text is generated automatically and depends on the range intervals:

![web-scatter-chart-with-range-rule](/assets/images/dashboards/web-scatter-chart-with-range-rule.png)

### Coloring 

A Scatter Chart item paints elements in pale gray if they don't meet the applied format condition. Note that this doesn't apply to elements that are painted by different hues.

Enable coloring for arguments to restore the color scheme:

![web-scatter-chart-color-by-hue](/assets/images/dashboards/web-scatter-chart-color-by-hue.png)

> [!Tip]
> **Documentation:**
> [Web Dashboard - Coloring](../../appearance-customization/coloring.md)
