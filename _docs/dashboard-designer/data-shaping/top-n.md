---
title: Top N
layout: default
nav_order: 5
parent: Data Shaping
grand_parent: Dashboard Designer
---
# Top N
The **Top N** feature allows you to display only a limited number of values that correspond to the highest or lowest values of a particular measure.

To enable the Top N feature, open the dashboard item [Bindings]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu, select a required data item and go to the _Top N_ section.

![wdd-top-n](/assets/images/dashboards/img124644.png)

Click **ON** and specify the following settings.

| Setting | Description |
|---|---|
| **Measure** | The parameter according to which the top or bottom values will be determined. |
| **Count** | The number of values to be displayed. |
| **Mode** | Specifies whether top or bottom values should be displayed. |
| **Show "Others" value** | If enabled, all values that are not the top/bottom ones are consolidated in the "Others" value. |

You can use the [hidden measure]({% link _docs/dashboard-designer/bind-dashboard-items-to-data/hidden-data-items.md %}) as a parameter according to which the top or bottom values will be determined.