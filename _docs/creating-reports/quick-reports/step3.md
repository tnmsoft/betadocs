---
layout: default
title: Step 3 Grouping and Sorting
nav_order: 3
parent: Creating a Quick Report
grand_parent: Creating Reports
---
Step 3 lets you choose the order in which records appear in the report. For example, you may wish to have a report sorted by city and within city, chronologically by a certain date field.

![](/assets/images/quickwizard3.png)

There are three types of sorting:

* *Grouping*: this sorts the data in the report by the different values of the grouped field. For example, if the report shows invoices grouped by customer name, all of the invoices for each customer appear together. Groups have three sections: a group header which shows the current group value (such as the name of the customer), the detail lines for that group (for example, the invoices), and a group footer, which shows summary information for the group (such as the number of invoices and the total amount for that customer). The groups are sorted by the grouped field (for example, invoices for Alfreds Futterkiste come before those for Consolidated Holdings) unless there's a group sort field.

* *Group sorting*: this sorts the data by the summary value of a field within a group. For example, suppose the report is grouped by customer and group sorted by invoice amount. In that case, all of the invoices for each customer appear together but the groups are sorted by the total of the invoices for the customers. In that case, invoices for Consolidated Holdings might come before those for Alfreds Futterkiste if Consolidated Holdings total sales are greater.

* *Sorting*: this sorts the data by the specified field. If there's no grouping for a report, sorting is the only way the report is ordered. For example, if the report is sorted by invoice date, invoices are shown in chronological order. If there is grouping, sorting takes place within a group. For example, if the report shows invoices grouped by customer name and sorted by invoice date, the groups are sorted by customer, all of the invoices for each customer appear together, and the invoices are in chronological order.

For each of these types, you can specify whether the sort is in ascending (from lowest to highest) or descending (highest to lowest) order by clicking the appropriate button: ![](/assets/images/sortasc.png) or ![](/assets/images/sortdesc.png).

## Normal fields
The *Normal fields* list displays the fields in the report you haven't grouped or sorted on. To group or sort on a field, drag it from this list to the appropriate area of this page. To remove a field from the group or sort areas, drag it back to this list. Note that if you are not allowed to sort or group on a field, a warning message is displayed and the field is moved back to the *Normal fields* list.

The only option for a field in the *Normal fields* list is *In group header*. This setting, which is disabled unless there's at least one grouped field, allows you to include non-grouped fields in the group header for a grouped field. For example, suppose you group on City from the Customers table but want to show the Region in the group header as well. Turn this option on and select City from the drop-down list to place both City and Region in the group header. All fields that appear in group headers appear in a [summary report]({% link _docs/creating-reports/templates.md %}).

## Grouped fields
The *Grouped fields* list displays the fields the report is grouped on. To group on a field, drag it from the *Normal fields* list to the *Grouped fields* list. You can have as many groups as you want, although having too many groups makes the report more complex and harder to read.

In addition to sort order, grouped fields have four other options, displayed below the *Grouped fields* list when you select a grouped field:

* *Include count in group footer*: if this option is turned on, a count of the number of records in the group appears at the end of the group in the report.

* *Group starts on*: this option controls pagination:

    <table class="detailtable table-striped">
    <tr>
    <th>Setting</th><th>Description</th>
    </tr>
    <tr>
    <td>Continue on same page</td><td>Continues the next group on the same page as the current one.</td>
    </tr>
    <tr>
    <td>Start on new page</td><td>Starts the next group on a new page.</td>
    </tr>
    <tr>
    <td>Start on new page and reset page number</td><td>Starts the next group on a new page and starts page numbering from 1 again when the group changes.</td>
    </tr>
    <tr>
    <td>Start on new page if it won't fit on current page</td><td>Starts the next group on a new page if the entire group won't fit on the current page.</td>
    </tr>
    </table><br />

* *Create bookmark on this field*: if this option is turned on, the different values of this field are displayed in a table of contents when the report is output to PDF. You can jump to the appropriate place in the report by clicking an item in the table of contents.

* *Stack fields in group header*: with this option turned on, each field in the group header appears on its own line. This can make the group heading fairly tall, so turn this option off to place all fields in the group header on the same line (although if there are a lot of fields, they may wrap to another line).

## Group sort field
To sort the groups for a report on a summary value, drag a field to the *Group sort field* area. You can only have one group sort field and you'll get a warning message if you don't have any grouped fields because group sorting works on groups. In addition to sort order, you can also choose the summary type to use. The default is Sum but you can also choose from Average, Highest, Lowest, Count, or Count Distinct. The difference between Count and Count Distinct is that Count counts the number of records while Count Distinct counts the number of records having unique values in this field. For example, if there are 100 order records but all orders were placed this week, using Count on the Order Date field would display 100 but Count Distinct would display 7 (assuming at least one order was placed every day this week).

## Sorted fields
The *Sorted fields* list displays the fields the report is sorted on. To sort on a field, drag it from the *Normal fields* list to the *Sorted fields* list. You can have as many sorted fields as you want. The only option for a sorted field is the sort order.