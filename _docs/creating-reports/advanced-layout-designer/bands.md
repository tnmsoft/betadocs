---
layout: default
title: Bands
nav_order: 2
parent: Advanced Layout Designer
grand_parent: Creating Reports
---
The Report Designer is a "band-oriented" designer. That is, objects that appear in the report appear in one of several bands. The types of bands available are:

* *TopMarginBand*: determines the margin at the top of the page.

* *BottomMarginBand*: determines the margin at the bottom of the page.

* *ReportHeaderBand*: appears at the start of the report.

* *ReportFooterBand*: appears at the end of the report.

* *PageHeaderBand*: appears at the top of every page.

* *PageFooterBand*: appears at the bottom of every page.

* *DetailBand*: prints once for every record in the report.

* *GroupHeaderBand*: prints at the start of a new group.

* *GroupFooterBand*: prints at the end of a new group (just before a new group is started or at the end of the report).

A report consists of, at a minimum, TopMargin, Detail, and BottomMargin bands; these bands cannot be deleted. In addition, {{ site.app_name }} creates a ReportFooter band to hold report totals, although you can remove this band if you wish, and there is one GroupHeader and possibly a GroupFooter band per grouped field.

A bar showing the band name appears at the left of the Layout Area for a band. The space to the right of the bar is for the objects in that band. Click the box for a band to select the band. Click it a second time to collapse it or again to expand it. To resize a band, position your mouse pointer at the bottom of the band's box and drag up or down. You can also change the height by editing the Height property in the Properties Panel. You cannot make a band smaller than the bottom of the lowest object in the band.

To add a band to the report, select a band or the report in the objects list in the Properties Panel or click one of the existing bands in the Layout Area, then click the appropriate button in the Action secion of the Properties Panel, such as ![](/assets/images/insertbandbutton.png) to add a ReportHeaderBand.

## Properties
The following are properties for bands. Unless noted, these properties don't actually affect the band itself but instead set the property for objects in the band. For example, setting Background Color doesn't make the entire band that color; it just sets the background color of objects in the band that have their Background Color property set to the default. See the [Objects]({% link _docs/creating-reports/advanced-layout-designer/report-objects.md %}) topic for information on the properties of objects.

### Styles section

* *Styles*: the [styles]({% link _docs/creating-reports/advanced-layout-designer/styles.md %}) of the objects in the band. The Detail Band has separate choices for Style, Even Style, and Odd Style.

### Appearance section

* *Background Color*: the background color of the objects in the band.

* *Border Color*: the border color of the objects in the band.

* *Border Dash Style*: the border style of the objects in the band.

* *Border Width*: the width of the border of the objects in the band.

* *Borders*: which borders appear for the objects in the band.

* *Font*: the font of the objects in the band.

* *Foreground Color*: the foreground (text) color of the objects in the band.

* *Padding*: the padding of the objects in the band. Padding is the amount of space around the text as a margin. The sub-properties are All (setting this sets all the others to the same value), Bottom, Left, Right, and Top.

* *Text Alignment*: the text alignment of the objects in the band.

* *Formatting Rules*: the [formatting rules]({% link _docs/creating-reports/advanced-layout-designer/formatting-rules.md %}) of the objects in the band.

### Behavior section

* *DrillDownControl*: this property, which is only available for the DetailBand and GroupHeader bands, is not used in {{ site.app_name }}.

* *DrillDownDetailReport*: this property, which is only available for the DetailBand and GroupHeader bands, is not used in {{ site.app_name }}.

* *Keep Together with...*: this property, which is only available for the DetailBand band, is not used in {{ site.app_name }}.

* *Multi-Column Options*: this property, which is only available for the DetailBand, allows you to specify a multi-column layout for the band. The sub-properties are:

    * *Column Count*: the number of columns to use. Note that this is only used if *Mode* is set to Use Column Count.

    * *Column Spacing*: the amount of space, in whatever the Measure Units for the report is set to, between columns.

    * *Column Width*: the width of the columns in whatever the Measure Units for the report is set to. Note that this is only used if *Mode* is set to Use Column Width.

    * *Layout*: determines how the columns are laid out: DownThenAcross (like a newspaper article) or AcrossThenDown.

    * *Mode*: specifies how columns are sized. UseColumnCount means divide the total space by Column Count to determine how much space each column gets. UseColumnWidth means divide the total space by Column Width to determine how many columns there are, and None means a single-column layout is used.

* *Group Fields*: this property, which is only available for GroupHeader bands, specifies the collection of fields used for the group. Click the + button to add a group field, the - button to delete a group field, or the up and down arrow buttons to rearrange the order of the fields. Click the arrow beside the field name to change the sort order to ascending or descending.

* *Group Union (GroupHeader)*: this property, which is only available for GroupHeader bands, determines whether the records in the group can be printed on different pages (set to None), if the entire group is moved to the next page if there isn't enough room on the current page (set to Whole Page), or if the group header is moved to the next page if there isn't enough room for it and at least one detail row (set to With First Detail).

* *Group Union (GroupFooter)*: this property, which is only available for GroupFooter bands, determines whether the records in the group can be printed on different pages (set to None) or if the last row in the detail is moved to the next page if there isn't enough room for it and the group footer (set to With Last Detail).

* *Level*: this property, which is only available for GroupHeader and GroupFooter bands, determines the grouping level when there's more than one group. The higher the number, the higher the group is. For example, the GroupHeader band with Level set to 1 is printed before the one with Level set to 0.

* *Page Break*: determines if a page break occurs when the band is output. The choices are None, Before the Band, and After the Band. This property isn't available for TopMargin, BottomMargin, PageHeader, and PageFooter bands.

* *Print at Bottom*: if this property, which is only available for GroupFooter and ReportFooter bands, is turned on, the band prints at the bottom of the page.

* *Repeat Every Page*: if this property, which is only available for GroupHeader and GroupFooter bands, is turned on, the band prints on every page. Otherwise, it only prints on the first page for the group.

* *Print On*: controls when the band is printed. The property is only available for PageHeader and PageFooter bands. The choices are:

    * *All Pages*: the band always prints.

    * *Not with Report Header*: the band doesn't print if the ReportHeader band is printed on the same page.

    * *Not with Report Footer*: the band doesn't print if the ReportFooter band is printed on the same page.

    * *Not with Report Header and Report Footer*: the band doesn't print if both the ReportHeader and ReportFooter bands are printed on the same page.

* *Visible*: if this is turned on, the band and the objects in it are output when the report is run. If not, the band and its objects are not output.

* *Scripts*: specifies the [script]({% link _docs/creating-reports/advanced-layout-designer/scripts.md %}) names to execute at various times, such as before and after the band prints.

### Data section

* *Sort Fields*: this property, which is only available for the DetailBand, specifies the collection of fields used for sorting. Click the + button to add a sort field, the - button to delete a sort field, or the up and down arrow buttons to rearrange the order of the fields. Click the arrow beside the field name to change the sort order to ascending or descending.

### Design section

* *Name*: the name of the band.

### Layout section

* *Size*: the height of the band.
