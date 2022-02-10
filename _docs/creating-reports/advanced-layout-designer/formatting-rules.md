---
layout: default
title: Formatting Rules
nav_order: 5
parent: Advanced Layout Designer
grand_parent: Creating Reports
---
Formatting rules allow you to apply conditional formats to objects. In fact, this is how {{ site.app_name }} uses conditional formats for fields in quick reports. This allows you to format negative numbers in red and positive in black, for example, or number greater than 50 in bold.

To access the formatting rules for the report, expand Formatting Rules in the Appearance section of the Properties Panel for any object. Click the + button to add a rule, the - button to delete a rule, or the up and down arrow buttons to rearrange the order of the rules.

The properties for a rule are:

* *Name*: the name of the rule. The name must start with a letter or underscore and can only contain letters, numbers, and underscores.

* *Condition*: an expression that evaluates to a Boolean (true or false or yes or no) value. For literal strings, use single quotes; for example, Country='Germany'. Click the "..." button to display the [Expression Editor]({% link _docs/creating-reports/advanced-layout-designer/expression-editor.md %}).

* *Data Source*: the name of the result set for the report. You can normally set this to RESULTSET, but if there's more than one data set, choose the desired one from the list.

* *Data Member*: the name of the data table in the data set for the report. You can normally leave this blank, but if the data set contains more than one data table, choose the desired one from the list.

* *Background Color*: the background color of the object.

* *Borders*: which borders appear for the object.

* *Border Color*: the color of the object's border. This is only applicable if at least one of the borders appears; see the *Borders* property.

* *Border Dash Style*: the type of line used for the border: solid, dash, dot, dash-dot, dash-dot-dot, or double. This is only applicable if at least one of the borders appears; see the *Borders* property.

* *Border Width*: the width of the border

* *Foreground Color*: the foreground (text) color of the object.

* *Font*: the font settings for the object.

* *Padding*: the amount of space around the text as a margin. The sub-properties are All (setting this sets all the others to the same value), Bottom, Left, Right, and Top.

* *Text Alignment*: the text alignment of the object.

* *Visible*: turn this off if the object should not appear when the condition is true or on if it should appear.

If you haven't set a property's value, it doesn't affect the property of objects using the rule. This allows you, for example, to have a rule that just sets the font of objects using the rule but not change their borders or colors.