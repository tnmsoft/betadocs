---
layout: default
title: Calculated Fields
nav_order: 6
parent: Advanced Layout Designer
grand_parent: Creating Reports
---
A calculated field is like a [formula]({% link _docs/creating-reports/formulas.md %}): it allows you to define your own calculation. However, unlike a formula, which is available for all reports, a calculated field belongs to just the report it's defined in.

To create a calculated field, select RESULTSET in the Field List and click the ![](/assets/images/addcalcfield.png) button. A calculated field displays a different icon than a real field (![](/assets/images/calcfield.png)) but can be used as the data source for an object in the Layout Area just like a real field. To edit a calculated field, select it and click the ![](/assets/images/editcalcfield.png) button. Click the ![](/assets/images/deletecalcfield.png) to delete it.

The properties are:

* *Name*: the name of the calculated field. The name must start with a letter or underscore and can only contain letters, numbers, and underscores.

* *Data Member*: the name of the data table in the data set for the report. You can normally leave this blank, but if the data set contains more than one data table, choose the desired one from the list.

* *Data Source*: the name of the result set for the report. You can normally leave this at RESULTSET, but if there's more than one data set, choose the desired one from the list.

* *Expression*: the expression that calculates the value. For literal strings, use single quotes; for example, Country='Germany'. Click the "..." button to display the [Expression Editor]({% link _docs/creating-reports/advanced-layout-designer/expression-editor.md %}).

* *Field Type*: the data type of the field. The choices are:

    <table class="detailtable table-striped">
    <tr>
    <th>Symbol</th><th>Description</th>
    </tr>
    <tr>
    <td>Boolean</td><td>A Boolean field capable of containing true or false (or yes or no) values.</td>
    </tr>
    <tr>
    <td>Byte</td><td>A single byte.</td>
    </tr>
    <tr>
    <td>DateTime</td><td>Used for date/time fields.</td>
    </tr>
    <tr>
    <td>Decimal</td><td>A 128-bit type often used for monetary values. The range of values supported is &#177;7.9 x 10<sup>-28</sup> to &#177;7.9 x 10<sup>28</sup>.</td>
    </tr>
    <tr>
    <td>Double</td><td>A 64-bit number, with a range of &#177;5.0 x 10<sup>-324</sup> to &#177;1.7 x 10<sup>308</sup>.</td>
    </tr>
    <tr>
    <td>Int16</td><td>A 2-byte integer value. The range is -32,768 to 32,767.</td>
    </tr>
    <tr>
    <td>Int32</td><td>A 4-byte integer value. The range is -2,147,483,648 to 2,147,483,647.</td>
    </tr>
    <tr>
    <td>Float</td><td>A 32-bit number, with a range of -3.4 x 10<sup>38</sup> to 3.4 x 10<sup>38</sup>.</td>
    </tr>
    <tr>
    <td>String</td><td>Used for alphanumeric text.</td>
    </tr>
    <tr>
    <td>TimeSpan</td><td>This type contains the span of time between two date/time values.</td>
    </tr>
    </table>
