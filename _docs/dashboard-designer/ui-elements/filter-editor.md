---
title: Filter Editor
layout: default
nav_order: 5
parent: UI Elements
grand_parent: Dashboard Designer
---

# Filter Editor

The Filter Editor dialog allows you to specify filter criteria for [data sources](../../provide-data/create-a-new-data-source.md), [SQL queries](../../provide-data/working-with-sql-data-sources/manage-sql-queries.md), and [dashboard items]({% link _docs/dashboard-designer/dashboard-item-settings/index.md %}).

## Use Filter Editor
The Filter Editor displays filter criteria as a tree where individual nodes specify simple filter conditions. The root node is the logical operator that combines all the conditions. Click this node and select the desired type to change the logical operator.

![Filtering_FilterEditor_LogicalOperator](/assets/images/dashboards/filtering_filtereditor_logicaloperator132422.png)

Click the plus button next to the operator to add a new condition or group.

![Filtering_FilterEditor_AddConditionMenu](/assets/images/dashboards/filtering_filtereditor_addconditionmenu132418.png)

To set a new condition, specify the dimension (including [hidden dimensions]({% link _docs/dashboard-designer/bind-dashboard-items-to-data/hidden-data-items.md %})):

![Filtering_FilterEditor_SelectField](/assets/images/dashboards/filtering_filtereditor_selectfield132426.png)

Then specify a comparison operator:

![Filtering_FilterEditor_ComparisonOperators](/assets/images/dashboards/filtering_filtereditor_comparisonoperators132427.png)

Set an operand value type in the dedicated value box:

![Filtering_FilterEditor_SelectOperand](/assets/images/dashboards/filtering_filtereditor_selectoperand132419.png)

The following operand types are available:

* **Value** - Allows you to compare dimension and static values.
	
	![Filtering_FilterEditor_ValueDropdown](/assets/images/dashboards/filtering_filtereditor_valuedropdown132420.png)
* **Property** - Compares different dimension values.
	
	![Filtering_FilterEditor_FieldsDropdown](/assets/images/dashboards/filtering_filtereditor_fieldsdropdown132425.png)
* **Parameter** - Allows you to compare dimension and [dashboard parameter](../../data-analysis/dashboard-parameters.md) values.
	
	![Filtering_FilterEditor_ParameterDropdown](/assets/images/dashboards/filtering_filtereditor_parameterdropdown132421.png)

Click the filter condition's **Remove** ![web-filter-editor-remove-button](/assets/images/dashboards/web-rd-filter-editor-remove-button129484.png) button to delete the condition.

## Advanced Mode
**Advanced Mode** allows you to enter a custom filter string.

![Filtering_FilterEditor_TextMode](/assets/images/dashboards/filtering_filtereditor_textmode132423.png)

Consider the following syntax conventions when you create text-based filter conditions:

* Insert a dimension by enclosing its name in square brackets (for example, **[Category]**).
* Denote string values with apostrophes (for example, **'Bikes'**).
* Enclose date-time values with hashtags (for example, **#2019-06-01#**).
* Reference [dashboard parameters](../../data-analysis/dashboard-parameters.md) by adding a question mark before their names (for example, **[Category] = ?categoryParam**)

This editor supports intelligent code completion (which suggests functions, parameters, and available data columns as you type).

![Filtering_FilterEditor_TextMode_Autocompletion](/assets/images/dashboards/filtering_filtereditor_textmode_autocompletion132424.png)

You can add a comment to your expression to explain it and make the expression more readable. Comments can be multi-line, and begin with `/*` and end with `*/`.

The **Warning** ![expression-editor-error-icon](/assets/images/dashboards/expression-editor-error-icon118339.png) icon appears if a condition contains errors.

