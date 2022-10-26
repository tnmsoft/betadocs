---
title: Dashboard Parameters
layout: default
nav_order: 3
parent: Data Analysis
grand_parent: Dashboard Designer
---
# Dashboard Parameters
You can use **dashboard parameters** when it is necessary to pass data of a certain type to a dashboard (e.g., to pass a specific value to the data source filter string or a calculated field).


## Creating Parameters
To create a dashboard parameter in the Web Dashboard, perform the following steps.
1. Invoke the [Dashboard Menu](../../ui-elements/dashboard-menu.md) and select **Parameters**.
2. In the **Parameter List**, click the **Add New Parameter** button. The following settings will be displayed for the created parameter.
	
	![WebDashboard_Parameters_NewParameter](../../../../images/img126106.png)
3. Specify the following parameter's settings.
	* **Name** - Specifies the parameter name.
	* **Description** - Specifies the parameter's description. 
		
		The parameter's description is the value displayed in the **Parameter Name** column of the [Dashboard Parameters](requesting-parameter-values.md) dialog.
	* **Visible** - Specifies whether or not the parameter is visible in the [Dashboard Parameters](requesting-parameter-values.md) dialog.
	* **Allow Null** - Specifies whether or a not null value can be passed as a parameter value.
	* **Allow Multiselect** - Specifies whether or not multi-selection is enabled for the current parameter.
	* **Select All Values** - Specifies whether or not all parameter values should be selected in the initial state. Note that this option is in effect when **Allow Multiselect** is set to **true**.
	* **Type** - Specifies the parameter type.
	* **Default Value** - Specifies the default parameter’s value.
	* **Look-Up Settings** - Specifies the parameter's look-up editor settings. To learn more, see the next step.
4. Depending on the selected **Look-up Settings** option, you need to specify the following settings.
	* **No Look-Up** - 
		Allows you to specify the required parameter value manually in the [Dashboard Parameters](requesting-parameter-values.md) dialog.
	* **Static List** - 
		Allows you to select a parameter value defined in a static list. To add predefined parameter values, use the **+** button.
	* **Dynamic List** - 
		Allows you to select a parameter value defined in a data source. To provide access to data source values, specify the following options.
		1. First, select the required **Data Source** from the list of available data sources. For the SQL data source, select the required **Data Member** that specifies the query/data member from the selected **Data Source**.
		2. Then, specify data members for the dashboard parameter's value and display name using **Value Member** and **Display Member**, respectively.
		3. If necessary, specify the data member used to sort parameter values using the **Sort By** option. The **Sort Order** specifies the required sort order.

## Passing Parameter Values
In this topic, it describes how to pass the created dashboard parameter to the dashboard. For instance, you can include a dashboard parameter to a _WHERE_ clause of the SQL query or you can filter a dashboard dynamically according to the required parameter value(s).

The created dashboard parameter can be used in the following scenarios:
* [SQL Queries](#query)
* [Filtering](#filtering)
* [Conditional Formatting](#formatrules)
* [Calculated Fields](#calculatedfields)
* [Window Calculations](#windowscalculations)

### <a name="query"/>SQL Queries
The Web Dashboard provides the capability to bind a dashboard parameter and the existing [SQL query](../../provide-data/working-with-sql-data-sources/pass-query-parameters.md)/[stored procedure](../../provide-data/working-with-sql-data-sources/stored-procedures.md) parameter. This can be useful when you need to [filter the SQL query](../../provide-data/working-with-sql-data-sources/filter-queries.md) dynamically by including the parameter value in the _WHERE_ clause.

![wdd-configure-query-param-page2](../../../../images/img124955.png)

Do the following to bind a dashboard parameter to an SQL query or stored procedure parameter in the [Dashboard Data Source Wizard](../../ui-elements/dialogs-and-wizards/dashboard-data-source-wizard.md):
* Select the existing query or stored procedure parameter, or use the **Add** button to create a new query parameter.
* Set the **Expression** as a parameter value and click the ellipsis button to invoke the Expression Editor for this parameter.
* In the Expression Editor, add the required dashboard parameter from the Parameters column.

### <a name="filtering"/>Filtering
You can filter the specified [query](../../provide-data/working-with-sql-data-sources/filter-queries.md) of the SQL Data Source, the entire [Excel Data Source](../../provide-data/filter-data-sources.md)/[Object Data Source](../../provide-data/filter-data-sources.md) or [apply filtering](../../data-shaping/filtering.md) to a specific dashboard item according to the current parameter value(s) using the Filter Editor.

In the Filter Editor, you can compare a field value with different objects such as static values, values of another field or parameter values. To switch between values, click a down arrow glyph in the operand value placeholder to expand the list of available objects. Select the **Parameter** object to compare a field value with a parameter value.

![wdd-filter-editor-change-object](../../../../images/img126182.png)

Then, click the operand value to invoke the list of available parameters and select the existing parameter or create a new one.

![wdd-parameters-filtering](../../../../images/img126539.png)

### <a name="formatrules"/>Conditional Formatting
You can apply conditional formatting to a specific dashboard item according to the current parameter value when creating the **Expression** [format condition](../../appearance-customization/conditional-formatting.md). Use this capability to format dashboard item elements dynamically, depending on the current parameter value.

![wdd-parameters-conditional-formatting](../../../../images/img128229.png)

To switch between values, click the down arrow glyph in the operand value placeholder to expand the list of available objects and select the **Parameter** object to create a format rule with a parameter.

### <a name="calculatedfields"/>Calculated Fields
You can use parameters when constructing [expressions](../../provide-data/calculated-fields.md) for [calculated fields](../../provide-data/calculated-fields.md). This allows you to evaluate values of the calculated field dynamically depending on the current parameter value.

![wdd-parameters-calculated-field](../../../../images/img126509.png)

To include a parameter in the expression, double-click the required parameter in the Fields pane.

### <a name="windowscalculations"/>Window Calculations
You can use parameters when customizing expressions for [window calculations](../calculations.md). This allows you to apply a calculation dynamically, depending on the current parameter value.

![wdd-parameters-window-calculations](../../../../images/img126562.png)

To create the calculation with a parameter, select the **Custom** calculation and click **Edit**. In the invoked Expression Editor double-click the required parameter.

## Requesting Parameter Values
The Web Dashboard provides a built-in **Dashboard Parameters** dialog, which provides the capability to change dashboard parameter values. This dialog is created automatically, depending on the parameter type and visibility settings.

![Parameters_DashboardParametersDialog_Web](../../../../images/img21818.png)

To invoke the Dashboard Parameters dialog in the Web Dashboard, click the **Parameters** button (the ![Parameters_ParametersButtonWin_Title](../../../../images/img21814.png) icon) in the [dashboard title](../../dashboard-layout/dashboard-title.md).

Select the required parameter values in the Dashboard Parameters dialog and click the **Submit** button to apply the changes. To restore the default values, click the **Reset** button.