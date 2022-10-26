---
title: Filter Elements
layout: default
nav_order: 15
parent: Dashboard Item Settings
grand_parent: Dashboard Designer
---
# Filter Elements
Filter elements represent a special type of dashboard item that allows you to apply filtering to other dashboard items.

![wdd-dashboard-items-filters](/assets/images/dashboards/img125353.png)


## Filter Elements Overview
The Web Dashboard allows you to create filter elements that used to filter other dashboard items.
* [Combo Box](#combo-box)
* [List Box](#list-box)
* [Tree View](#tree-view)
* [Date Filter](#date-filter)

To add the required filter element to the dashboard, use corresponding buttons into the **Filter** section of the **Toolbox**.

![wdd-toolbox-filter-elements](/assets/images/dashboards/wdd-toolbox-filter-elements125330.png)

### Combo Box
The **Combo Box** dashboard item allows you to select a value(s) from the drop-down list.

You can switch the combo box type in the Combo Box's [Options](../../ui-elements/dashboard-item-menu.md) menu. The table below demonstrates available Combo Box's types.

| Standard | Checked |
|---|---|
| The **Standard** type allows you to select only a single value. | The **Checked** type allows you to select multiple values in the invoked drop-down list. |
| ![wdd-combo-box-standard-type](/assets/images/dashboards/img125341.png) | ![wdd-combo-box-checked-type](/assets/images/dashboards/img126666.png) |

By default, the Combo Box's dropdown contains an 'All' item that allows you to select/deselect all items in the Combo Box. To hide this item, turn off the **Show 'All' Value** option in the Combo Box's [Options](../../ui-elements/dashboard-item-menu.md) menu.

### List Box
The **List Box** dashboard item allows you to select a value(s) from the list.

You can switch the list box type in the List Box's [Options](../../ui-elements/dashboard-item-menu.md) menu. The table below demonstrates available List Box's types.

| Checked | Radio |
|---|---|
| The **Checked** type allows you to select multiple values in the list box. | The **Radio** type allows you to select only a single value in the radio group. |
| ![wdd-list-box-radio-type](/assets/images/dashboards/img125342.png) | ![wdd-list-box-checked-type](/assets/images/dashboards/img126667.png) |

### Tree View
The **Tree View** dashboard item displays values in a hierarchical way and allows you to expand/collapse nodes.

![wdd-treeview](/assets/images/dashboards/img125343.png)

You can manage the initial expanded state of filter values using the **Auto Expand** option in the Tree View's [Options](../../ui-elements/dashboard-item-menu.md) menu.

### Date Filter

The **Date Filter** dashboard item allows you to filter dashboard data based on the selected data range.

![datefilter](/assets/images/dashboards/datefilter-web-autoheight.png)

See [Date Filter](../date-filter.md) for details.


## Providing Data
The Web Dashboard allows you to bind various dashboard items to data in a consistent manner, the only difference being the data sections that these dashboard items comprise. To learn more about common binding concepts, see the [Bind Dashboard Items to Data](../../bind-dashboard-items-to-data.md) topic.

This topic describes how to bind **filter elements** to data using the Web Dashboard control.

### Binding Overview
All filter elements provide the **Dimensions** data section, which accepts dimensions used to provide filter values.

To bind the filter elements to data, click a placeholder contained in one of the available data sections and select the required data source field in the **Binding** section of the invoked [data item menu](../../ui-elements/data-item-menu.md).

To learn about the specifics of binding various filter elements to data, see the table below.

| Dashboard Item | Data Sections | Description |
|---|---|---|
| **Combo Box** | ![wdd-filter-elements-combobox-bindings](/assets/images/dashboards/img126759.png) | The Combo Box filter element can contain several dimensions at the **Dimensions** data section. In this case , the drop-down list will contain combinations of dimension values. |
| **List Box** | ![wdd-filter-elements-listbox-bindings](/assets/images/dashboards/img125344.png) | The List Box filter element can contain several dimensions at the **Dimensions** data section. In this case, the list will contain combinations of dimension values. |
| **Tree View** | ![wdd-filter-elements-treeview-bindings](/assets/images/dashboards/img125345.png) | The Tree View filter element can contain several dimensions at the **Dimensions** data section. In this case, dimension values are displayed in a hierarchical way. This can be the set of dimensions with different group intervals (e.g., Year/Quarter/Month) or the set of related dimensions (e.g., geographical data such as continents/countries/cities). |

## Interactivity
This document describes filtering capabilities supported by filter elements. You can use filter elements to apply master filtering to other dashboard items or introduce hierarchical filtering by adding several connected filters.

### Master Filtering
The Dashboard allows you to use any data aware dashboard item as a filter for other dashboard items ([Master Filter](../../interactivity/master-filtering.md)).

> [!IMPORTANT]
> Note that filter elements do not support Master Filter selection modes. You can switch the selection mode by [changing the type](filter-elements-overview.md) of the required filter element.

Depending on the filter element type, you can select a value(s) to make other dashboard items display only data related to the selected value(s).

![wdd-filter-elements-interactivity](/assets/images/dashboards/img125351.png)

You can also create a set of related filter elements containing relevant filter values. For instance, in the image below, the _State_ filter element contains states related to the 'United States' value, while the _City_ filter element contains cities related to the 'New York' value.

![wdd-filter-elements-ignore-group-filter](/assets/images/dashboards/img125352.png)

Disable the **Ignore Master Filters** option in the [Interactivity](../../ui-elements/dashboard-item-menu.md) menu for the required filter element to allow the applying of filtering to this element.