---
layout: default
title: Styles
nav_order: 4
parent: Advanced Layout Designer
grand_parent: Creating Reports
---
While you can format each objects manually, setting properties such Background Color, Font, and Padding, gets tedious if you have a lot of objects. It also is error-prone; you could forget to set one of the properties for some objects, so they look different than the other objects. It's also hard to make overall changes, such as changing the font for every object from Arial to Tahoma. Instead, use styles.

Like styles in Microsoft Word and other applications, styles in {{ site.app_name }} allow you to define a consistent appearance for certain types of objects. For example, perhaps all objects in the DetailBand should use Tahoma 10pt but objects in the GroupHeader bands should use Tahoma 10pt Bold. This can easily be done by creating two styles and then  setting the Style property of each object to the appropriate style. Later if you decide to use a different font, simply change the style and all objects using that style use the new font without having to edit each one manually. [Templates]({% link _docs/creating-reports/templates.md %}) use styles extensively for a consistent appearance for all objects.

{{ site.app_name }} automatically creates styles for the report based on the styles defined in the [template]({% link _docs/creating-reports/templates.md %}) for the report. The styles include ColumnHeadingStyle, used for column heading, DetailBandFieldStyle, used for objects in the detail band, and SummaryFieldStyle, used for summary objects such as grand totals. You can edit any of these styles or create new ones if you wish.

## Editing styles
To create a new style, choose *Create New Style* from the *Style* drop-down list. To edit a style, click the arrow to the left of the Style heading.

The properties for a style are:

* *Name*: the name of the style. The name must start with a letter or underscore and can only contain letters, numbers, and underscores.

* *Font*: the font settings for the object.

* *Text Alignment*: the text alignment of the object.

* *Padding*: the amount of space around the text as a margin. The sub-properties are All (setting this sets all the others to the same value), Bottom, Left, Right, and Top.

* *Background Color*: the background color of the object.

* *Foreground Color*: the foreground (text) color of the object.

* *Border Color*: the color of the object's border. This is only applicable if at least one of the borders appears; see the *Borders* property.

* *Borders*: which borders appear for the object.

* *Border Width*: the width of the border

* *Border Dash Style*: the type of line used for the border: solid, dash, dot, dash-dot, dash-dot-dot, or double. This is only applicable if at least one of the borders appears; see the *Borders* property.

If you haven't set a property's value, it doesn't affect the property of objects using the style. This allows you, for example, to have a style that just sets the font of objects using the style but not change their borders or colors.

## Using a style
To use a style, set an object's Style property to the desired style from the drop-down list. Some objects have three types of styles: Even Style, which is used when the object appears in even-numbered rows, Odd Style, used for odd-numbered rows, and Style, used when Even Style and Odd Style aren't filled in. Even Style and Odd Style allow to create reports where alternating rows have different colors by leaving the Background Color of an even style untouched (meaning it'll be white) and setting it to some color for an odd style.