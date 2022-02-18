---
layout: default
title: Step 2 Data Selection
nav_order: 2
parent: Creating a Cross-Tab Report
grand_parent: Creating Reports
---
Step 2 allows you to select which fields appear in the report.

![](/assets/images/xtabwizard2.png)

## Available fields
The *Available fields* list shows the fields for the table selected in the Table drop-down list. You can choose fields from more than one table for a report; simply choose the desired table, add the fields you want from that table to the report, then select another table and do the same. Fields that are actually [formulas]({% link _docs/creating-reports/formulas.md %}) have a suffix of "[Formula]."

Click the ![](/assets/images/displayonlyrelated.png) button to have the Table drop-down list show only tables that are directly related to tables already selected for the report.

To scroll the list of fields, drag the scroll bar at the right of the list or use your mouse wheel.

{{ site.app_name }} by default displays fields in alphabetical order. This makes it easy to find a field in the list. However, sometimes it makes more sense to display fields in the order they appear in the table. For example, for typical address fields, you would see this order alphabetically:

* Address
* City
* Contact Name
* Country
* Customer Name
* Postal Code
* Region

whereas they'd appear like this in table order:

* Customer Name
* Contact Name
* Address
* City
* Region
* Postal Code
* Country

Click the ![](/assets/images/sortorder.png) button to display fields in table order. Click ![](/assets/images/sortname.png) to display them alphabetically.

If there are a lot of fields in the *Available fields* list, it may be difficult to find the one you want. Click the ![](/assets/images/filtericon.png) button and type some text in the box that appears; the list of available fields now displays only those fields containing that text somewhere in the name or caption. Click the button again to return to the full list.

The ![](/assets/images/valuesicon.png) button displays a list of the unique values in the field. This is handy if you're not sure what data a field contains. This button may be disabled for certain fields.

The ![](/assets/images/editicon.png) button appears beside fields that are [formulas]({% link _docs/creating-reports/formulas.md %}). Click this button to edit the formula. To create a new formula, click the *Create New Formula* button.

## Selected fields
The *Selected fields* list shows the fields included in the report. To add a field to the list, click the ![](/assets/images/add.png) button beside the field name in the *Available fields* list. To remove a field from the *Selected fields* list, click the ![](/assets/images/deleteicon.png) button.

Like the *Available fields* list, the *Selected fields* list includes the ![](/assets/images/valuesicon.png) button to display a list of the unique values in the field and the ![](/assets/images/editicon.png) button to edit a formula.

To scroll the list of fields, drag the scroll bar at the right of the list or use your mouse wheel.

## Field Properties
Clicking the Field Properties button displays the Field Properties dialog. This dialog allows you to specify how the field is formatted.

![](/assets/images/xtabfieldproperties1.png)

At the top of the dialog is a list of the selected fields in the report. Choose the desired field to edit its properties.

The Display page has the following options:

* *Heading*: the column heading. You can specify multiple lines for the heading by pressing Enter where a new line should start. You can expand the text area by dragging the handle in the lower-right corner of the area.

* *Auto-fit column*: if this option is turned on, which it is by default, the column is automatically sized to accommodate the widest value in the column, including the column heading.

* *Width*: if the *Auto-fit column* option is turned off, this is used as the width for the field in the report. This value can be reduced to fit more columns on the page; the field contents and column heading automatically wrap within the reduced width as necessary.

* *Suppress repeating values*: if this option is turned on (the default) and this field is a row field, only the first occurrence of a value is printed; the field in subsequent records appears blank and the cells are merged together.

![](/assets/images/xtabfieldproperties2.png)

See the [Formatting Values]({% link _docs/creating-reports/formatting-values.md %}) topic for details on how to format values in a report.

![](/assets/images/xtabfieldproperties3.png)

The Style page has the following options:

* *Use default font*: if this option is turned on, which it is by default, this field uses the font specified in the [template for the report]({% link _docs/creating-reports/templates.md %}), even if the default font is changed after the field is added to the report. To change the font, turn this option off and choose the desired font name, size, and style.

* *Use default foreground color*: if this option is turned on, which it is by default, this field uses the text color specified in the [template for the report]({% link _docs/creating-reports/templates.md %}), even if the color is changed after the field is added to the report. To change the color, turn this option off and choose the desired color by clicking the color bar and choosing from the Color dialog.

* *Use default background color*: if this option is turned on, which it is by default, this field uses the background color specified in the [template for the report]({% link _docs/creating-reports/templates.md %}), even if the color is changed after the field is added to the report. To change the color, turn this option off and choose the desired color by clicking the color bar and choosing from the Color dialog.
