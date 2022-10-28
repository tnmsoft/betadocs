---
title: Bind Dashboard Items to Data in the Web Dashboard
layout: default
nav_order: 1
parent: Bind Dashboard Items to Data
grand_parent: Dashboard Designer
---
# Bind Dashboard Items to Data in the Web Dashboard
This topic explains how to bind the newly created dashboard item to data source fields to visualize data.

* [Create Binding](#create)
* [Modify Binding](#modify)
* [Clear Binding](#clear)
* [Specify a Data Source](#specify)

## <a name="create"/>Create Binding
To bind a dashboard item to data, invoke the dashboard item's [Bindings]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu to open binding settings. In this menu you can see a data source (data member)  to which the dashboard item is bound and empty placeholders for data items.

The image below displays the [Grid]({% link _docs/dashboard-designer/dashboard-item-settings/grid.md %}) dashboard item, that binded to _Sales Person_ query of the _SQL Data Source_, and corresponding [data sections]({% link _docs/dashboard-designer/dashboard-item-settings/grid.md %}).

![wdd-bindings-menu](/assets/images/dashboards/img124590.png)

To populate a dashboard item with data, click a placeholder and choose the required field in the invoked list of data source's available fields.

![wdd-add-data-tem](/assets/images/dashboards/img125350.png)

To rename the data item, go to the **Options** section and specify the data item's caption.

![WDD-rename-data-item](/assets/images/dashboards/img124591.png)

> [!NOTE]
> To learn how to bind a specific dashboard item to data, see the **Providing Data** topic for the [required dashboard item]({% link _docs/dashboard-designer/dashboard-item-settings/index.md %}).

## <a name="modify"/>Modify Binding
You can modify data binding by dragging a data item within a data section. To do this, drag the data item to the required position.

![wdd-replace-data-item](/assets/images/dashboards/img124592.png)

## <a name="clear"/>Clear Binding
You can remove the data item by clicking the **Remove** (![WDD-icon-delete-data-source](/assets/images/dashboards/img124585.png)) icon in the data item container.

![wdd-grid-delete-data-item](/assets/images/dashboards/img125482.png)

## <a name="specify"/>Specify a Data Source
A dashboard can contain several data sources. By default, a dashboard item is bound to the first [available data source](../provide-data/manage-data-sources.md).

You can change the default  data source (or a data member / query, optionally) of dashboard items. For this, go to the dashboard item's [Bindings]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu and click the **Data / Filtering** button.

![wdd-data-filtering-section](/assets/images/dashboards/img125086.png)

In the invoked section you can change the data source (data member) for the selected dashboard item. Click **OK** to save the changes.

> [!NOTE]
> Note that this action removes all data items from the current dashboard item.
