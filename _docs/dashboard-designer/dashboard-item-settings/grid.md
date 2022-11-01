---
title: Grid
layout: default
nav_order: 3
parent: Dashboard Item Settings
grand_parent: Dashboard Designer
---
# Grid
The topics in this section describe the features available in the **Grid** dashboard item, and provide information on how to create and customize grids

![wdd-dashboard-items-grid](/assets/images/dashboards/img125122.png)


## Providing Data {#providing-data}
The **Web Dashboard** allows you to bind various dashboard items to data in a virtually uniform manner. To learn more, see the [Bind Dashboard Items to Data]({% link _docs/dashboard-designer/bind-dashboard-items-to-data/index.md %}) topic.

The only difference is in the data sections that the required dashboard item has. This topic describes how to bind a **Grid** dashboard item to data.

### Binding to Data in the Web Dashboard
The image below shows a sample Grid dashboard item that is bound to data.

![wdd-grid-binding](/assets/images/dashboards/img125397.png)

To bind the Grid dashboard item to data, click a placeholder contained in one of the available data sections and select the required data source field in the **Binding** section of the invoked [data item menu]({% link _docs/dashboard-designer/ui-elements/data-item-menu.md %}).

The table below lists and describes the Grid's data sections.

| Section | Processed as | Description |
|---|---|---|
| **Columns** | Dimension or Measure (depending on the selected column type) | Contains data items that provide values for grid columns. The data item menu allows you to select the [column type](columns.md) and specify their options. |
| **Sparkline** | Dimension | Contains a data item that provides arguments for sparkline columns. To learn more, see [Columns](columns.md). |


## Columns
The Grid dashboard item supports four types of columns.

![wdd-grid-columns-overview](/assets/images/dashboards/img125253.png)
* **Dimension**
	
	A dimension column displays values from the bound data item "as is".  If the dimension column is bound to a data source containing images, it can display images.
* **Hyperlink**
	
	A dimension column allows you to display hyperlinks in the Grid dashboard item. You can provide hyperlinks as a separate data column, or they can be automatically created at run-time from any column using the specified **URI pattern**.
	
	![grid_hyperlink_column](/assets/images/dashboards/grid_hyperlink_column.png)


* **Measure**
	
	A measure column displays summaries calculated against data in the bound data item.
	
	Values in the measure column can be displayed as text or represented by bars.
	
	![wdd-grid-measure-options](/assets/images/dashboards/img125786.png)
	
	To select between these modes, open the column menu and go to the **Options** section.
* **Delta**
	
	A delta column calculates summaries against two measures: the **Actual** value and the **Target** value. When you switch the column type to **Delta**, a new **Target** data item container appears.
	
	![wdd-grid-delta-target-data-section](/assets/images/dashboards/img125787.png)
	
	The difference between these values is displayed within the column.
	
	You can configure delta options in the **Delta Options** section of the [column menu]({% link _docs/dashboard-designer/ui-elements/data-item-menu.md %}).
* **Sparkline**
	
	A sparkline column visualizes the variation of summary values over time.
	
	The sparkline column is bound to the measure providing sparkline values and to the dimension providing a date-time interval. Add the required date-time dimension to the **Sparkline** placeholder to show values depending on time.
	
	![wdd-grid-sparkline-add-date](/assets/images/dashboards/img125788.png)
	
	You can configure sparkline options in the data item's **Sparkline Options** section.

When you drop a data item into the Columns section, the type for the new column is determined automatically based on the data type.

To change the column type, open the [column menu]({% link _docs/dashboard-designer/ui-elements/data-item-menu.md %}) and click the corresponding type button.

![wdd-grid-column-type](/assets/images/dashboards/img125212.png)


## Interactivity
To enable interaction between the Grid and other dashboard items, you can use the interactivity features, as **Master Filtering** and **Drill-Down**.
* [Master Filtering](#masterfiltering)
* [Drill-Down](#drilldown)

### <a name="masterfiltering"/>Master Filtering
You can use the **Grid** dashboard item as a filter for other dashboard items. To learn more about filtering concepts common to all dashboard items, see the [Master Filtering]({% link _docs/dashboard-designer/interactivity/master-filtering.md %}) topic.

The Grid dashboard item supports filtering by rows.

When **Master Filtering** is enabled, you can click a grid row (or multiple rows) to make other dashboard items only display data related to the selected record(s).

![WebViewer_MasterFiltering](/assets/images/dashboards/img22459.gif)

To enable **Master Filtering**, go to the Grid's [Interactivity]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu and select the required Master Filtering mode.

![wdd-dashboard-items-interactivity-section](/assets/images/dashboards/img125270.png)

To reset filtering, use the **Clear Master Filter** button (the ![wdd-master-filtering-icon](/assets/images/dashboards/img125072.png) icon) in the Grid's [caption]({% link _docs/dashboard-designer/dashboard-layout/dashboard-item-caption.md %}).

### <a name="drilldown"/>Drill-Down
The built-in drill-down capability allows you to change the detail level of data displayed in dashboard items on the fly. To learn more about drill-down concepts common to all dashboard items, see the [Drill-Down](../../interactivity/drill-down.md) topic.

The **Grid** dashboard item supports drill-down for rows.When drill-down is enabled, you can click a grid row to view the details.

![wdd-grid-interactivity-drill-down](/assets/images/dashboards/img125412.png)

Drill-down requires that the Columns section contains several dimensions at the top, from the least detailed to the most detailed dimension.

![wdd-grid-interactivity-several-dimensions](/assets/images/dashboards/img125410.png)

> [!NOTE]
> In OLAP mode, you can perform drill-down for either a hierarchy data item or several dimension attributes.

To enable **Drill-Down**, go to the Grid's [Interactivity]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu and turn the **Drill-Down** option on.

![wdd-dashboard-items-interactivity-section](/assets/images/dashboards/img125270.png)

To return to the previous detail level, click the **Drill Up** button (the ![wdd-drill-up-icon](/assets/images/dashboards/img125074.png) icon) in the Grid's [caption]({% link _docs/dashboard-designer/dashboard-layout/dashboard-item-caption.md %}).


## Conditional Formatting
Use conditional formatting to highlight individual cells or rows based on specific conditions. You can apply format rules to the **dimension** and **measure** [column types](columns.md). You can use [hidden measures](../../bind-dashboard-items-to-data/hidden-data-items.md) to specify a condition used to apply formatting to visible values. 

![wdd-grid-conditional-formatting](/assets/images/dashboards/img125791.png) 

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

Refer to the following topic for more information about format condition types: [Conditional Formatting in Web Dashboard]({% link _docs/dashboard-designer/appearance-customization/conditional-formatting.md %}).

### Create and Edit a Format Rule   

You can create and edit format rules in the **Conditional Formatting** section that is located in the following places:

* The dashboard item's [Options]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu

* The [data item menu]({% link _docs/dashboard-designer/ui-elements/data-item-menu.md %})

Refer to the following topic for information on how to create and edit format rules: [Conditional Formatting in Web Dashboard]({% link _docs/dashboard-designer/appearance-customization/conditional-formatting.md %}).

### Grid-Specific Format Condition Settings

The format rule's **Miscellaneous** section contains the following properties that are specific to the Grid item:

![web-cf-grid-miscellaneous](/assets/images/dashboards/web-cf-grid-miscellaneous.png)

 | Option | Description |
 | -- | --| 
 | **Enabled** | Enables/disables the current format rule. |
 | **Applied to Row** | Applies the current format rule to a row. |


## Totals
The Grid dashboard item enables you to add a summary value (a **total**) calculated against displayed values of an individual column, and to show the result under this column. Note that you can add any number of totals for each column. For example, you can obtain the number of column records, average or maximum value, etc.

![wdd-grid-totals](/assets/images/dashboards/img125280.png)
* [Totals Overview](#overview)
* [Create and Edit Totals](#create)

### <a name="overview"/>Totals Overview
You can use the following summary functions when creating totals.
* **Count** - The number of records.
* **Sum** - The sum of the values. 
	
	![func_sum](/assets/images/dashboards/img4460.png)
* **Min** - The smallest value.
* **Max** - The largest value.
* **Average** - The average of the values.
	
	![func_average](/assets/images/dashboards/img4457.png)
* **Auto** - 
	The total is calculated using the type of [summary function](../../data-shaping/summarization.md) specified for the measure corresponding to the current Grid column. Note that in this case, the total is calculated based on values of the corresponding data field from the underlying data source. 
	
	> [!NOTE]
	> Note that the **Auto** type is not supported when the Grid is bound to the OLAP data source.

You can create totals using different sets of summary functions. This depends on the type of the data source field providing data for the target column.

> [!IMPORTANT]
> Note that the **Auto** type is available only for the [measure](columns.md) column.

### <a name="create"/>Create and Edit Totals
To create a total, open a [data item menu]({% link _docs/dashboard-designer/ui-elements/data-item-menu.md %}) and go to the **Totals** section. Click "+" to add a new total.

To change the total type, open the drop down list and select the required type.

![wdd-grid-totals-change-total-type](/assets/images/dashboards/img125281.png)

You can delete the required total by clicking the **Delete** button (the ![wdd-icon-delete-big](/assets/images/dashboards/img126104.png) icon).

![wdd-grid-delete-totals](/assets/images/dashboards/img125282.png)


## Layout
The Grid dashboard item allows you to customize its layout in various ways. You can manage the width of grid columns, specify the visibility of column headers, enable cell merging, etc.

To access the layout settings, use the **Layout** section in the Grid's [Options]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu.

The following settings are available.

![wdd-grid-layout-options](/assets/images/dashboards/img125283.png)
* **Horizontal Lines** - Specifies grid's horizontal line visibility.
* **Vertical Lines** - Specifies grid's vertical line visibility.
* **Banded Rows** - Specifies the different background for odd and even rows.
* **Column Headers** - Allows you to toggle column header visibility.
* **Word Wrap** - Displays cell content on multiple lines if the size of a dashboard item is insufficient to completely display the cell content on a single line.
* **Column Width Mode** - Specifies column widths of the entire Grid using one of the available modes.
