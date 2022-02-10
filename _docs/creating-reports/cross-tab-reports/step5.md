---
layout: default
title: Step 5 Report Options
nav_order: 5
parent: Creating a Cross-Tab Report
grand_parent: Creating Reports
---
Step 5 allows you to specify formatting options for the report.

![](/assets/images/xtabwizard5.png)

The options in this step are:

* *Delete Advanced Layout*: click this button, which is only enabled if the report has an [advanced layout]({% link _docs/creating-reports/advanced-layout-designer/using-the-layout-designer.md %}), to remove the advanced layout from the report.

* *Subreport Properties*: click this button to display the [Subreport Properties]({% link _docs/creating-reports/subreports.md %}) dialog so you can define subreports for this report. This button is disabled if you haven't selected any fields for the report.

* *Advanced Report Properties*: click this button to display the [Advanced Report Properties]({% link _docs/creating-reports/advanced-properties.md %}) dialog so you can change some advanced settings. This button is disabled if you haven't selected any fields for the report.

* *Title*: the title for the report. The title, which defaults to whatever you entered for Name, appears at the top of every page of the report. If you want to use an [expression]({% link _docs/reference/function-reference.md %}) rather than fixed text, surround the expression with "{" and "}" (without the quotes). Note that the expression must evaluate to a string value, so use the Str() function if necessary to convert non-string values such as dates and numbers to their string equivalent.

    Here's an example of an expression that displays "Sales for <spelled out month> <year>" (such as "Sales for December 2015") in the report header:

        {"Sales for " + MonthName(Now()) + " " + Str(Year(Now()))}

    Suppose the report has an ask-at-runtime condition on Country and you want to display "Sales for *country*" in the title, where *country* is the country chosen by the user when they run the report. In that case, use the GetConditionValue function:

        {"Sales for " + GetConditionValue(0, 0)}

    {% if site.has_multidatasource %}This expression displays the name of the report and the data source it reports on.

        {Name + "\n" + DataSource}

    (The "\n" is a line break.)
{% endif %}

* *Orientation*: the default choice, *Automatic*, means that if the report is too wide to fit in portrait orientation, it automatically switches to landscape. However, you can override this by choosing either *Portrait* or *Landscape* to force the report to be printed in the desired orientation.

* *Template*: this specifies the [template]({% link _docs/creating-reports/templates.md %}), which determines the overall layout of the report. The default template for a new report is determined by the *Default cross-tab template* setting in the [Options dialog]({% link _docs/configuration/configuration.md %}), but if other templates are available, you may select the desired one from the drop-down list. Note that if your report contains Unicode characters, you may wish to use a "Unicode" template or the report may not display the characters properly when output to PDF.

* *Paper type*: if this option is turned on, which it is by default, the paper type defined in the template is used for the report. Turn this off to use a different paper type, which you can choose from the drop-down list. All standard paper types, such as letter, legal, and A4, are supported. Note that if you choose Custom for the paper type, you can enter the height and width of the custom type.

* *Margin*: these options control the left, right, top, and bottom margins of the report. If these options are turned on, which they are by default, the margins defined in the template are used for the report. Turn these off individually to use a different margin.

* *Localize*: if this option is turned on, which it is by default, the report is "localized" when it's run. Localizing a report meaning translating column headings and other things like "Page 1 of 2" into the language the user running the reports has chosen in the [Options dialog]({% link _docs/configuration/configuration.md %}). If you turn this option off, the report is run with these things in the language the report was created in.

* *Table layout*: by default, {{ site.app_name }} uses absolute positioning to render a report in the Preview window. While that normally works well, if you find that some objects aren't positioned properly, you may wish to use HTML tables to render the report instead. In that case, turn this setting on.

* *Database in Header*: turn this option on to display the name of the database the report is being run against in the header of the report.

* *Always run*: turn this option on to run the report even when there are no records that match your filter condition. This results in a blank report. If this option is turned off, rather than displaying a blank report, {{ site.app_name }} displays a message that there are no records.

* *Location*: by default, row and column totals (subtotals when more than one column or row field is used) are shown at the end of a set of row or column values (the "After Values" setting). Set this to "Before Values" to show subtotals at the start of the set instead. This option is disabled if there's only one row or column field.

* *Totals*: turn this option on, which it is by default, to display row or column totals (subtotals when more than one column or row field is used) or off to omit them. This option is disabled if there's only one row or column field.

* *Grand totals*: turn this option on, which it is by default, to display row or column grand totals at the end of the report or off to omit them.

* *Hide nulls*: by default, values for which there is no data (known as "null;" for example, if the report shows sales by country and product and there are no sales for Widgets in Moldovia) displays as a blank space. If you want to display zero instead, turn this setting on.

* *Distinct*: if you filter on a field from a table that isn't involved in the report, you may end up with what appear to be duplicate records. For example, say your report displays the number of companies by sales territory. If you filter on the Product Name from the Products table being "Apricot Jam" (in other words, you only want to include customers who bought that product), you'd end up with the counts being too high: each customer is counted once for every order they placed for that product. That isn't typically something you'd want, so {{ site.app_name }} can eliminate these duplicate records for you.

    The DISTINCT clause in a SQL statement tells the database to only find records that have distinct values, so adding that clause to the SQL statement means that each customer is only counted once. The *Retrieve distinct records* option allows you to control whether the DISTINCT clause is used or not. "Never" means don't add a DISTINCT clause to the SQL statement for this report and "Always" means do add it. "If filtering on a table not in the report" means only add the DISTINCT clause if you filter on a field from a table that isn't involved in the report.

    You might think that "If filtering on a table not in the report" should always be used. However, there may be times when this isn't the correct behavior. For example, if you want to show fields from the Orders table (Order Date, Product Name, and Quantity Ordered) but filter on Company Name is "Sam's Grocery," {{ site.app_name }} eliminates what it thinks are duplicate records, such as two orders for the same product and same quantity on the same day. Clearly, this isn't right&mdash;you'd end up with some missing data. In that case, set this option to *Never*.

* *Top N*: this option allows you to display only the top records. If you set this option to something other than "No," you can enter a number and indicate whether that number is the number of records you want (the "Count" setting) or a percentage of the total records such as the top 10 percent (the "Percent" setting). Note that "top" refers to the sort order for the report. For example, if the report is sorted alphabetically by Company Name, you'll get the specified number of records in alphabetical order. If the report is sorted in descending by Order Date, you get the specified number of most recent orders.

