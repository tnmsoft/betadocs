---
title: Range Filter
layout: default
nav_order: 10
parent: Dashboard Item Settings
grand_parent: Dashboard Designer
---
# Range Filter
The **Range Filter** dashboard item allows you to apply filtering to other dashboard items. This item displays a chart with selection thumbs that allow you to filter out values displayed along the argument axis.

![wdd-dashboard-items-range-filter](/assets/images/dashboards/img125127.png)

## Providing Data
The **Web Dashboard** allows you to bind various dashboard items to data in a virtually uniform manner. To learn more, see the [Bind Dashboard Items to Data]({% link _docs/dashboard-designer/bind-dashboard-items-to-data/index.md %}) topic.

The only difference is in the data sections that the required dashboard item has. This topic describes how to bind a **Range Filter** dashboard item to data.

### Binding to Data in the Web Dashboard
The image below shows a sample Range Filter dashboard item that is bound to data.

![wdd-range-filter-bindings](/assets/images/dashboards/img125355.png)

To bind the Range Filter dashboard item to data, click a placeholder contained in one of the available data sections and select the required data source field in the **Binding** section of the invoked [data item menu]({% link _docs/dashboard-designer/ui-elements/data-item-menu.md %}).

The table below lists and describes the Range Filter's data sections.

| Section | Processed as | Description |
|---|---|---|
| **Values** | Measure | Contains data items against which the Y-coordinates of data points are calculated. |
| **Arguments** | Dimension | Contains data items that provide values displayed along the horizontal axis of the Range Filter. Data filtering is performed based on these values. Note that the **Custom Periods** section in the **Options** menu allows you to create [predefined ranges](predefined-periods.md) used to select the required date-time interval. |
| **Series** | Dimension | Contains data items whose values are used to create chart series. |

## Series
The Range Filter dashboard item supports various **Line**, **Area** and **Bar** series types.

To switch between series types, click the data item located in the **Values** section and select the required type from the **Type** section of the [data item menu]({% link _docs/dashboard-designer/ui-elements/data-item-menu.md %}). To show all available types, click the ellipsis button.

![wdd-range-filter-change-series-type](/assets/images/dashboards/img125356.png)

The Range Filter supports the following series types.
* Line
* Stacked Line
* Full-Stacked Line
* Area
* Stacked Area
* Full-Stacked Area
* Bar
* Stacked Bar
* Full-Stacked Bar


## Interactivity
This document describes the features that enable interaction between the Range Filter and other dashboard items. These features include Master Filtering.

### Master Filtering
The Dashboard allows you to use any data-aware dashboard item as a filter for other dashboard items.

**Master filtering** is always enabled for the Range Filter dashboard item. The Range Filter displays a chart with selection thumbs that allow you to filter out values displayed along the argument axis.

![wdd-dashboard-items-range-filter](/assets/images/dashboards/img125127.png)

The Range Filter supports the **Ignore Master Filters** and **Cross Data Source Filtering** options. To learn more, see the [Master Filtering]({% link _docs/dashboard-designer/interactivity/master-filtering.md %}) topic.

### Predefined Periods
The Range Filter dashboard item allows you to add a number of _predefined date-time periods_ that can be used to perform a selection.

![wdd-range-filter-select-custom-period](/assets/images/dashboards/img125361.png)

To learn more about predefined periods, see [Predefined Periods](predefined-periods.md).

## Predefined Periods
The Range Filter dashboard item allows you to add a number of predefined date-time periods that can be used to perform a selection (for instance, _year-to-date_ or _quarter-to-date_).

- [Add Predefined Ranges](#add-predefined-ranges)
- [Select Predefined Ranges](#select-predefined-ranges)

### Add Predefined Ranges
To add predefined ranges, open the Range Filter's [Options]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu and go to the **Custom Periods** section. Click "+" to add a new period.

![wdd-range-filter-custom-intervals](/assets/images/dashboards/img125362.png)

You can specify the following settings for the start/end boundaries.
* **Caption** - Specifies a predefined period caption.
* **Start Mode** - Specifies a mode of the start boundary.
* **End Mode** - Specifies a mode of the end boundary.

The following modes used to set predefined ranges are available.
* **None** - The selection will begin from the start/end of the visible range.
* **Fixed** - Allows you to select a specific date value using the calendar. Use the **Start/End Date** option to set a value.
* **Flow** - Allows you to select a relative date value. The **Interval** option specifies the interval between the current date and the required date. The **Offset** option allows you to set the number of such intervals.
	
	> [!NOTE]
	> Note that the **Offset** option can accept **negative** and **positive** values. Negative values correspond to dates before the current date, while positive values correspond to future dates.

Below you can find some examples of how to set up custom periods:

**Fixed custom periods**

**2018**
- _Start Point_
	- Mode: Fixed
	- Start Date: 01/01/2018

- _End Point_
	- Mode: Fixed
	- End Date: 12/31/2018

**Q1 2017**
- _Start Point_
	- Mode: Fixed
	- Start Date: 01/01/2017

- _End Point_
	- Mode: Fixed
	- End Date: 03/31/2018

**Flow custom periods**

**6 Months**
- _Start Point_
	- Mode: Flow
	- Interval: Month
	- Offset: -5

- _End Point_
	- Mode: None

**Year to date**
- _Start Point_
	- Mode: Flow
	- Interval: Year
	- Offset: 0

- _End Point_
	- Mode: Flow
	- Interval: Day
	- Offset: 0

**Last Month**
- _Start Point_
	- Mode: Flow
	- Interval: Month
	- Offset: -1

- _End Point_
	- Mode: Flow
	- Interval: Month
	- Offset: 0

### Select Predefined Ranges
To select a predefined period, click the **Select Date Time Period** button (the ![wdd-range-filter-custom-period-icon](/assets/images/dashboards/img125360.png) icon) in the Range Filter's [caption]({% link _docs/dashboard-designer/dashboard-layout/dashboard-item-caption.md %}) and select the required period from the list.

![wdd-range-filter-select-custom-period](/assets/images/dashboards/img125361.png)