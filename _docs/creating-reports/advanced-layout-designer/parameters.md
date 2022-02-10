---
layout: default
title: Parameters
nav_order: 7
parent: Advanced Layout Designer
grand_parent: Creating Reports
---
A parameter is a value either entered by the user or passed to the report that can be used for something. For example, {{ site.app_name }} automatically adds two parameters to reports: ReportTitle and ReportFilter. It passes the title of the report to ReportTitle and the filter condition to ReportFilter. Both are data-bound to label objects in the PageHeader band so the report title and filter condition appear at the top of every page.

A parameter can be used anywhere a field is used, such as being data-bound to a report object like the ReportTitle and ReportFilter parameters.

To add a [parameter]({% link _docs/creating-reports/advanced-layout-designer/parameters.md %}), select Parameters and click the ![](/assets/images/addparameter.png) button. To edit a parameter, select it and click the ![](/assets/images/editcalcfield.png) button. Click the ![](/assets/images/deletecalcfield.png) to delete it.

The properties are:

* *Name*: the name of the parameter. The name must start with a letter or underscore and can only contain letters, numbers, and underscores.

* *Description*: the prompt the user sees when they run the report if *Show in the parameters panel* is turned on.

* *Visible*: turn this on if the user should be prompted for the value or off if not.

* *MultiValue*: turn this on if the user can select more than one value.

* *Type*: the data type of the parameter's value: String, Date, Number (16 bit integer), Number (32 bit integer), Number (floating-point), Number (double-precision floating-point), Number (decimal), Boolean, and Guid.

* *Value*: the default value to use.

* *Look-Up Settings Type*: *No Look-Up* means the user enters values themselves. *Static List* means the user choose values from a list defined in *Look-Up Settings* (see below). *Dynamic List* means the user chooses values from the database (see below).

* *Look-Up Settings*: the sub-choices depend on the setting of * *Look-Up Settings Type*. For *Static List*, the choices are:

    * *Filter String*: allows you to specify a filter condition applied to the values.

    * *Values*: click the + button to add a value, the - button to delete a value, or the up and down arrow buttons to rearrange the order of the values. For each value, enter a description (what the user sees) and value (the actual value used for the parameter).

    For *Dynamic List*, the choices are:

    * *Filter String*: allows you to specify a filter condition applied to the data.

    * *Data Source*: the name of the result set for the report. You can normally set this to RESULTSET, but if there's more than one data set, choose the desired one from the list.

    * *Data Member*: the name of the data table in the data set for the report. You can normally leave this blank, but if the data set contains more than one data table, choose the desired one from the list.

    * *Display Member*: the name of the field containing the values to display to the user.

    * *Value Member*: the name of the field containing the values to use.
