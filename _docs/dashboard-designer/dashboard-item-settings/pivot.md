---
title: Pivot
layout: default
nav_order: 7
parent: Dashboard Item Settings
grand_parent: Dashboard Designer
---
# Pivot
The **Pivot** dashboard item displays a cross-tabular report that presents multi-dimensional data in an easy-to-read format.

![wdd-dashboard-items-pivot](/assets/images/dashboards/img125126.png)

## Providing Data
The **Web Dashboard** allows you to bind various dashboard items to data in a virtually uniform manner. To learn more, see the [Bind Dashboard Items to Data](../../bind-dashboard-items-to-data.md) topic.

The only difference is in the data sections that the required dashboard item has. This topic describes how to bind a **Pivot** dashboard item to data.

### Binding to Data in the Web Dashboard
The image below shows a sample Pivot dashboard item that is bound to data.

![wdd-pivot-bindings](..//assets/images/dashboards/img125646.png)

To bind the Pivot dashboard item to data, click a placeholder contained in one of the available data sections and select the required data source field in the **Binding** section of the invoked [data item menu](../../ui-elements/data-item-menu.md).

The table below lists and describes the Pivot's data sections.

| Section | Processed as | Description |
|---|---|---|
| **Values** | Measure | Contains data items used to calculate values displayed in the pivot table. |
| **Columns** | Dimension | Contains data items whose values are used to label columns. |
| **Rows** | Dimension | Contains data items whose values are used to label rows. |


## Interactivity
To enable interaction between the Pivot and other dashboard items, you can use the interactivity features. These features include **Master Filtering**.

### Master Filtering
Data displayed in the Pivot dashboard item can be filtered by other master filter items. The image below displays the Pivot dashboard item filtered by [Tree View](../filter-elements.md).

![wdd-pivot-interactivity](..//assets/images/dashboards/img125754.png)

You can prevent the pivot from being affected by other master filter items using the **Ignore Master Filters** button in the Pivot's [Interactivity](../../ui-elements/dashboard-item-menu.md) menu.

![wdd-pivot-interactivity](..//assets/images/dashboards/img125456.png)

To learn more about filtering concepts common to all dashboard items, see the [Master Filtering](../../interactivity/master-filtering.md) topic.


## Conditional Formatting
A Pivot dashboard item highlights cells with a certain color, depending on the cell's value. You can calculate a format rule by measures placed in the **Values** section and dimensions placed in the **Columns** or **Rows** section.

You can use [hidden measures](../../bind-dashboard-items-to-data/hidden-data-items.md) to specify a condition used to apply formatting to visible values. 

![wdd-pivot-cf](..//assets/images/dashboards/img126057.png)

### Supported Format Rules

Format rules that can be applied to different data item types are as follows:
* numeric 
	* **Value**
	* **Top-Bottom**
	* **Average**
	* **Expression**  
	* **Icon Ranges**
	* **Color Ranges**
	* **Gradient Ranges**
	* **Bar** 
	* **Bar Color Ranges** 
	* **Bar Gradient Ranges** 
* string 
	* **Value** (with the condition type set to _Equal To_, _Not Equal To_ or _Text that Contains_)
	* **Expression**
* date-time 
	* **Value**
	* **A Date Occurring** (for dimensions with a continuous date-time group interval)
	* **Expression**
	* **Icon and Color Ranges**
	* **Color Ranges**
	* **Gradient Ranges**
	* **Bar** 
	* **Bar Color Ranges** 
	* **Bar Gradient Ranges** 

Refer to the following topic for more information about format condition types: [Conditional Formatting in Web Dashboard](../../appearance-customization/conditional-formatting.md).

### Create and Edit a Format Rule   

You can create and edit format rules in the **Conditional Formatting** section that is located in the following places:

* The dashboard item's [Options](../../ui-elements/dashboard-item-menu.md) menu

* The [data item menu](../../ui-elements/data-item-menu.md)

Refer to the following topic for information on how to create and edit format rules: [Conditional Formatting in Web Dashboard](../../appearance-customization/conditional-formatting.md).

### Pivot-Specific Format Condition Settings

New appearance settings are applied to data cells that correspond to a row/column intersection. You can set a new intersection of the row and column or use predefined settings.

Note the following specifics:

1. The dashboard does not calculate format rules in a pivot item for percentage values at multiple levels. In this case, the "All Levels" intersection mode is not available.
2. If you create a new format rule for a dimension from the Columns/Rows section, the corresponding format condition dialog does not contain any Pivot-specific settings.

The format rule's **Miscellaneous** section contains pivot-specific options:

![](..//assets/images/dashboards/web-cf-pivot-miscellaneous.png)

| Option | Description |
| --|--|
| **Enabled** | Enables/disables the current format rule. |
| **Intersection Mode** | Specifies the level at which to apply conditional formatting to pivot cells. |  
| **Intersection Row/Column Dimension**  | Applies the format rule to the specified row/column dimension, if you select the _Specific Level_ as the intersection mode.|
| **Apply to Row/Column** | Specifies whether to apply the formatting to the Pivot item's entire row/column.

A Pivot item allows you to specify the field intersection to which a format rule is applied.

| Intersection Level Mode| Description |
| --|--|
| _Auto_ | Identifies the default level. For the Pivot dashboard item, _Auto_ identifies the First Level. |
| _First Level_ |The first level values are used to apply conditional formatting. |
| _Last Level_ | The last level values are used to apply conditional formatting. |
| _All Levels_ | All pivot data cells are used to apply conditional formatting. |
| _Specific Level_ | The specified measures/dimensions are used to apply conditional formatting. |

For example, the Pivot item has three fields in the column area (_Year_, _Category_, and _Product_) and one field in the row area (_State_):

![intersection_levels](..//assets/images/dashboards/intersection_levels.png)

The image below displays different intersection levels with the applied format rule:

![pivot_applied_levels](..//assets/images/dashboards/pivot_applied_levels.png)

To apply a format rule to the row or column Grand Total, change the **Intersection Level Mode** to _Specific level_ and set the _[Grand Total]_ value as the intersection row/column dimension.  


## Layout
This topic describes how to control the Pivot dashboard item layout, the visibility of totals and grand totals, etc.
* [Layout Type](#layouttype)
* [Totals Visibility](#totalsvisibility)
* [Totals Position](#totalsposition)
* [Values Visibility](#valuesvisibility)
* [Values Position](#valuesposition)

### <a name="layouttype"/>Layout Type
If the Pivot dashboard item contains a hierarchy of dimensions in the [Rows](providing-data.md) section, you can specify the layout used to arrange values corresponding to individual groups.

| Layout type | Example | Description |
|---|---|---|
| **Compact** | ![WebPivot_LayoutCompact](..//assets/images/dashboards/img127806.png) | Displays values from different Row dimensions in a single column. Note that in this case totals are displayed at the top of a group, and you cannot change [totals position](#totalsposition). |
| **Tabular** | ![WebPivot_LayoutTabular](..//assets/images/dashboards/img127807.png) | Displays values from different Row dimensions in separate columns. |

To change the Pivot layout, go to **[Options menu](../../ui-elements/dashboard-item-menu.md)** | **Layout** and use the **Layout** option.

### <a name="totalsvisibility"/>Totals Visibility
You can control the visibility of totals and grand totals for the entire Pivot dashboard item. For instance, the image below displays the Pivot dashboard item with the disabled row totals.

![WebPivot_DisableRowTotals_Example](..//assets/images/dashboards/img127808.png)

To manage the visibility of totals and grand totals, go to **[Options menu](../../ui-elements/dashboard-item-menu.md)** | **Layout** and use the following options:
* **Row Totals** / **Row Grand Totals**
* **Column Totals** / **Column Grand Totals**

Moreover, you can control the visibility of totals for individual dimensions/measures. To do this, go to **[Bindings menu](../../ui-elements/dashboard-item-menu.md)**, select the required data item and use its **Options** | **Show Totals** option.

### <a name="totalsposition"/>Totals Position
If necessary, you can change the position of totals/grand totals for the Pivot dashboard item. For instance, in the Image below the Pivot dashboard item whose row totals are moved from bottom to top.

![WebPivot_RowTotals_Bottom_Top](..//assets/images/dashboards/img127809.png)

To manage totals position, go to **[Options menu](../../ui-elements/dashboard-item-menu.md)** | **Layout** and use the following options:
* **Row Totals Position**
* **Column Totals Position**

### <a name="valuesvisibility"/>Values Visibility
The Pivot dashboard item can contain several measures in the [Values](providing-data.md) section. In this case, you can hide summary values corresponding to specific measures. For instance, the image below shows the Pivot with hidden _Quantity_ values.

![WebPivot_ValuesVisibility](..//assets/images/dashboards/img127811.png)

To do this, go to **[Bindings menu](../../ui-elements/dashboard-item-menu.md)**, select the required measure and use its **Options** | **Show Values** option.

### <a name="valuesposition"/>Values Position
The Pivot dashboard item allows you to control the position of headers used to arrange summary values corresponding to different measures. For instance, you can display values in columns or in rows.

![WebPivot_ValuesPosition](..//assets/images/dashboards/img127810.png)

To manage this position, go to **[Options menu](../../ui-elements/dashboard-item-menu.md)** | **Layout** and use the **Values Position** option.

## Expanded State
If the [Columns or Rows](providing-data.md) section contains several data items, the Pivot column and row headers are arranged in a hierarchy and make up column and row groups.

![wdd-pivot-expand-collapse.png](..//assets/images/dashboards/img125647.png)

You can collapse and expand row and column groups using the ![Pivot_Layout_ExpandCollapse_DownArrow](..//assets/images/dashboards/img20154.png) and ![Pivot_Layout_ExpandCollapse_UpArrow](..//assets/images/dashboards/img20155.png) buttons. However, the current expanded state of column and row groups do not save in the dashboard definition. If necessary, you can specify the default expanded state using the following options from **[Options menu](../../ui-elements/dashboard-item-menu.md)** | **Initial State**:
* **Auto Expanded Column Groups** - Specifies whether column groups should be collapsed or expanded by default;
* **Auto Expanded Row Groups** - Specifies whether row groups should be collapsed or expanded by default.