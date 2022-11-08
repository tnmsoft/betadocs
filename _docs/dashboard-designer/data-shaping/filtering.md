---
title: Filtering
layout: default
nav_order: 4
parent: Data Shaping
grand_parent: Dashboard Designer
---
# Filtering
Web Dashboard allows you to filter data in the [dashboard items]({% link _docs/dashboard-designer/dashboard-item-settings/index.md %}) or apply filters to a specific measure. You can use [dimensions]({% link _docs/dashboard-designer/bind-dashboard-items-to-data/bind-dashboard-items-to-data-in-the-web-dashboard.md %}) and [hidden dimensions]({% link _docs/dashboard-designer/bind-dashboard-items-to-data/hidden-data-items.md %}) to build filter criteria.

![Filtering_Main](/assets/images/dashboards/filtering_main132414.png)

## Dashboard Item Filter

Filters that are applied to a dashboard item affect only this item. Open a dashboard item's [Filters]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu, go to the **Item Filter** section and click **Edit** to add a filter:

![wdd-invoke-filter-editor](/assets/images/dashboards/wdd-invoke-filter-editor124630.png)

This invokes the [Filter Editor]({% link _docs/dashboard-designer/ui-elements/filter-editor.md %}) dialog where you can specify filter criteria:

![Filtering_FilterEditor_Empty](/assets/images/dashboards/filtering_filtereditor_empty132417.png)

{: .tip }
**Documentation**: [Filter Editor]({% link _docs/dashboard-designer/ui-elements/filter-editor.md %}) 

## Measure Filter

You can apply filters to individual [measures]({% link _docs/dashboard-designer/bind-dashboard-items-to-data/bind-dashboard-items-to-data-in-the-web-dashboard.md %}). If you create multiple measures that only differ in applied filters, you can compare values calculated over different date-time periods or against different categories.

Open a dashboard item's [Binding]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu and select a measure to filter. In the invoked [data item menu]({% link _docs/dashboard-designer/ui-elements/data-item-menu.md %}), open the **Filter** section and click **Edit**. This invokes the [Filter Editor]({% link _docs/dashboard-designer/ui-elements/filter-editor.md %}) dialog where you can specify filter criteria. 

![web-filter-to-measure-menu](/assets/images/dashboards/web-filter-to-measure-menu.png)

{: .tip }
**Documentation**: [Filter Editor]({% link _docs/dashboard-designer/ui-elements/filter-editor.md %})

You can clear the applied filter in the [data item menu]({% link _docs/dashboard-designer/ui-elements/data-item-menu.md %})'s **Filter** section.

{: .note }
The measure filter is technically an expression that uses the `filter(summaryExpression, filterCriteria)` function, where `summaryExpression` is the measure to be filtered and `filterCriteria` is the filter. See the following topic for more information about functions you can use in dashboard expressions: [Expression Constants, Operators, and Functions]({% link _docs/dashboard-designer/data-analysis/expression-constants-operators-and-functions.md %}).

The image below shows a Chart with three measures: 

- _2019 - Opened_ is filtered by year 2019.
- _2020 - Opened_ is filtered by year 2020.
- _Opened_ is the original measure without filters.
 
![web-filter-to-measure-year](/assets/images/dashboards/web-filter-to-measure-year.png)


## Visible Data Filter

You can specify a Visible Data Filter to limit displayed data. This filter type does not filter underlying data used in calculations or intermediate level aggregations.

Open a dashboard item's [Filters]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu, go to the **Visible Data Filter** section and click **Edit** to invoke the Filter Editor, where you can specify a condition:

![web-invoke-visible-data-filter](/assets/images/dashboards/web-invoke-visible-data-filter.png)

For example, a Grid dashboard item has 35 rows and displays sales percentages.

![web-filter-visible-data-filter-original-grid](/assets/images/dashboards/web-filter-visible-data-filter-original-grid.png)

The image below shows the difference between filters (the filter condition is the same): 

- **Dashboard Item Filter**: sales percentages are recalculated based on the visible data.
- **Visible Data Filter**: sales percentages remain the same because this filter type does not affect calculations.

![web-filter-visible-data-filter-grids](/assets/images/dashboards/web-filter-visible-data-filter-grids.png)