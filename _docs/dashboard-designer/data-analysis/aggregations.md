---
title: Aggregations
layout: default
nav_order: 1
parent: Data Analysis
grand_parent: Dashboard Designer
---
# Aggregations
The Web Dashboard allows you to prepare underlying data using additional aggregation levels when creating [calculated fields]({% link _docs/dashboard-designer/data-analysis/calculations.md %}). This topic shows how to evaluate calculated fields on a visualization (summary) and intermediate levels.

## Summary Level Aggregations
To compute values of the calculated field on a visualization (or summary) level, you can use a set of predefined aggregate functions. In the Expression Editor, these functions are available within the **Functions** | **Aggregate**.

| Function | Description | Example |
|---|---|---|
| Aggr(SummaryExpression, Dimensions) | Aggregates underlying data using the detail level specified by a predefined set of dimensions and a specified summary function. | Aggr(Sum([Sales]), [Category], [Product]) |
| Avg(Value) | Returns the average of all the values in the expression. | Avg([Profit]) | 
| Count() | Returns the number of values. | Count() |
| CountNotNull(Value) | Returns a number of non-null objects in a collection. | CountNotNull([Orders]) |
| CountDistinct(Value) | Returns the number of distinct values. | CountDistinct([Orders]) |
| Max(Value) | Returns the maximum value across all records. | Max([Profit]) |
| Min(Value) | Returns the minimum value across all records. | Min([Profit]) |
| Mode(Value) | Returns the mode of the values. | Mode([Profit]) |
| Median(Value) | Returns the median of the values. | Median([Profit]) |
| Sum(Value) | Returns the sum of all values. | Sum([Profit]) |
| Var(Value) | Returns an estimate of the variance of a population, where the sample is a subset of the entire population. | Var([Orders]) |
| Varp(Value) | Returns the variance of a population, where the population is the entire data to be summarized. | Varp([Orders]) |
| StdDev(Value) | Returns an estimate of the standard deviation of a population, where the sample is a subset of the entire population. | StdDev([Orders]) |
| StdDevp(Value) | Returns the standard deviation of a population, where the population is the entire data to be summarized. | StdDevp([Orders]) |

These functions can be used for all types of numeric fields.

## Intermediate Level Aggregations
The Web Dashboard can aggregate and summarize data on different levels.
* The reports that provide data to a dashboard allow aggregate and summary options. You can group, sort, summarize, and apply other data shaping operations during report creation.
* [Dashboard items]({% link _docs/dashboard-designer/dashboard-item-settings/index.md %}) aggregate and summarize data at the visualization level using dimensions and measures, respectively. See the following topic to learn more: [Bind Dashboard Items to Data]({% link _docs/dashboard-designer/bind-dashboard-items-to-data/index.md %}).
* The **Aggr** function introduces an intermediate detail level that is not related to the visualization level. This allows you to create custom aggregations at different levels and combine these aggregations with existing visualizations.
