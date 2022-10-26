---
title: Convert Dashboard Items
layout: default
nav_order: 8
parent: Dashboard Designer
---
# Convert Dashboard Items
The Web Dashboard provides the capability to convert data-bound dashboard items to another type.

To convert the selected dashboard item to another type, use the dashboard item's [Convert To](ui-elements/dashboard-item-menu.md) menu.

![wdd-convert-to-dialog](/assets/images/dashboards/img125857.png)

> [!NOTE]
> You can also created a copy of the selected dashboard item using the **Duplicate current item** command.

The Web Dashboard always preserves the following settings for data-bound dashboard items.
* The set of data items used to bind the dashboard item to data.
* Data shaping settings of data items and their names.
* A custom name displayed within the dashboard item caption.

The following settings are kept if the dashboard item is being converted to an item that also supports this feature.
* [Master Filtering](interactivity/master-filtering.md) settings (e.g., the specified master filter mode).
* [Drill-Down](interactivity/drill-down.md) settings (e.g., the target dimension).
* [Conditional Formatting](appearance-customization/conditional-formatting.md) settings.
* [Coloring](appearance-customization/coloring.md) settings.
* [Calculation](data-analysis/calculations.md) settings.

For different types of dashboard items, some specific settings can be preserved. For example, the following settings are preserved.
* Legend settings for the [Chart]({% link _docs/dashboard-designer/dashboard-item-settings/chart.md %})/[Scatter Chart]({% link _docs/dashboard-designer/dashboard-item-settings/scatter-chart.md %}) dashboard items.
* Series types for the [Chart({% link _docs/dashboard-designer/dashboard-item-settings/chart.md %})Range Filter]({% link _docs/dashboard-designer/dashboard-item-settings/range-filter.md %}) dashboard items.
* Element arrangement settings for the [Pie]({% link _docs/dashboard-designer/dashboard-item-settings/pies.md %})/[Card]({% link _docs/dashboard-designer/dashboard-item-settings/cards.md %})/[Gauge]({% link _docs/dashboard-designer/dashboard-item-settings/gauges.md %}) dashboard items.
* Caption settings for the [Pie]({% link _docs/dashboard-designer/dashboard-item-settings/pies.md %})/[Gauge]({% link _docs/dashboard-designer/dashboard-item-settings/gauges.md %}) dashboard items.
* Navigation settings for [Choropleth Map]({% link _docs/dashboard-designer/dashboard-item-settings/choropleth-map.md %})/[Geo Point Maps]({% link _docs/dashboard-designer/dashboard-item-settings/geo-point-maps.md %}).
* The attribute whose values are displayed within shape titles for [Choropleth Map]({% link _docs/dashboard-designer/dashboard-item-settings/choropleth-map.md %})/[Geo Point Maps]({% link _docs/dashboard-designer/dashboard-item-settings/geo-point-maps.md %}).
* Legend settings for the [Choropleth Map]({% link _docs/dashboard-designer/dashboard-item-settings/choropleth-map.md %})/[Geo Point Maps]({% link _docs/dashboard-designer/dashboard-item-settings/geo-point-maps.md %}).
* Clustering settings for [Geo Point Maps]({% link _docs/dashboard-designer/dashboard-item-settings/geo-point-maps.md %}).