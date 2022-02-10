---
layout: default
title: Step 5 Report Options
nav_order: 5
parent: Creating a Quick Report
grand_parent: Creating Reports
---
Step 5 allows you to specify formatting options for the report.

![](/assets/images/quickwizard5.png)

The options in this step are:

* *Edit Advanced Layout*: click this button to create and edit the [advanced layout]({% link _docs/creating-reports/advanced-layout-designer/using-the-layout-designer.md %}) for the report.

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

* *Template*: this specifies the [template]({% link _docs/creating-reports/templates.md %}), which determines the overall layout of the report. The default template for a new report is determined by the *Default template* setting in the [Options dialog]({% link _docs/configuration/configuration.md %}), but if other templates are available, you may select the desired one from the drop-down list. Note that if your report contains Unicode characters, you may wish to use a "Unicode" template or the report may not display the characters properly when output to PDF.

* *Paper type*: if this option is turned on, which it is by default, the paper type defined in the template is used for the report. Turn this off to use a different paper type, which you can choose from the drop-down list. All standard paper types, such as letter, legal, and A4, are supported. Note that if you choose Custom for the paper type, you can enter the height and width of the custom type.

* *Margin*: these options control the left, right, top, and bottom margins of the report. If these options are turned on, which they are by default, the margins defined in the template are used for the report. Turn these off individually to use a different margin.

* *Localize*: if this option is turned on, which it is by default, the report is "localized" when it's run. Localizing a report meaning translating column headings and other things like "Page 1 of 2" into the language the user running the reports has chosen in the [Options dialog]({% link _docs/configuration/configuration.md %}). If you turn this option off, the report is run with these things in the language the report was created in.

* *Table layout*: by default, {{ site.app_name }} uses absolute positioning to render a report in the Preview window. While that normally works well, if you find that some objects aren't positioned properly, you may wish to use HTML tables to render the report instead. In that case, turn this setting on.

* *Respect page width*: if this option is turned on, which it is by default, and you add more fields that can fit on one row in a report, any fields extending beyond the right edge are automatically moved to the next row. That allows you to see all of the data but gets kind of messy. If you turn this option off, fields are allowed to extend beyond the right edge. In that case, moving to the next page in the Preview window shows those fields.

    Here's an example with *Respect page width* turned on:

    ![](/assets/images/respectpagewidthon.png)

    Here's the first page of the report with this setting turned off. Notice that not all of the fields are shown.

    ![](/assets/images/respectpagewidthoff1.png)

    Here's the second page. Notice that it shows the rest of the fields.

    ![](/assets/images/respectpagewidthoff2.png)

* *Auto fit to page*: this setting, which only appears when *Respect page width* is turned off, helps with the issue shown in the image above. Turn this on to scale the data down so it fits on one horizontal page rather than taking more than one page.

    ![](/assets/images/autofittopage.png)

* *Move subtotals*: this setting allows you to control where subtotals are placed if they're too close to the left margin. With this setting turned on (the default), subtotal values that overlap with the subtotal label are moved to the next row; for example:

    ![](/assets/images/movesubtotalson.png)

    With the setting turned off, the subtotal label is narrowed and may span several rows if necessary so the subtotal value can appear on the first row; for example:

    ![](/assets/images/movesubtotalsoff.png)

* *Database in Header*: turn this option on to display the name of the database the report is being run against in the header of the report.

* *Group totals*: by default, group totals are shown in the group footer (the "After Values" setting). Set this to "Before Values" to show totals in the group header instead.

* *Always run*: turn this option on to run the report even when there are no records that match your filter condition. This results in a blank report. If this option is turned off, rather than displaying a blank report, {{ site.app_name }} displays a message that there are no records.

* *Summary report*: if this item is turned on, the report does not print detail information but only those fields that appear in group headers and summarized fields. This option is disabled unless there's at least one group in the report.

* *Distinct*: if you filter on a field from a table that isn't involved in the report, you may end up with what appear to be duplicate records. For example, say your report displays the Company Name and Contact Name from the Customers table. If you filter on the Product Name from the Products table being "Apricot Jam" (in other words, you want a list of customers who bought that product), you'd end up with each customer showing up once for every order they placed for that product. So, if Sam's Grocery ordered it 25 times, they'd appear on the report 25 times. That isn't typically something you'd want, so {{ site.app_name }} can eliminate these duplicate records for you.

    The DISTINCT clause in a SQL statement tells the database to only find records that have distinct values, so adding that clause to the SQL statement means that Sam's Grocery only shows up once. The *Retrieve distinct records* option allows you to control whether the DISTINCT clause is used or not. "Never" means don't add a DISTINCT clause to the SQL statement for this report and "Always" means do add it. "If filtering on a table not in the report" means only add the DISTINCT clause if you filter on a field from a table that isn't involved in the report.

    You might think that "If filtering on a table not in the report" should always be used. However, there may be times when this isn't the correct behavior. For example, if you want to show fields from the Orders table (Order Date, Product Name, and Quantity Ordered) but filter on Company Name is "Sam's Grocery," {{ site.app_name }} eliminates what it thinks are duplicate records, such as two orders for the same product and same quantity on the same day. Clearly, this isn't right&mdash;you'd end up with some missing data. In that case, set this option to *Never*.

* *Top N*: this option allows you to display only the top records. If you set this option to something other than "No," you can enter a number and indicate whether that number is the number of records you want (the "Count" setting) or a percentage of the total records such as the top 10 percent (the "Percent" setting). Note that "top" refers to the sort order for the report. For example, if the report is sorted alphabetically by Company Name, you'll get the specified number of records in alphabetical order. If the report is sorted in descending by Order Date, you get the specified number of most recent orders.