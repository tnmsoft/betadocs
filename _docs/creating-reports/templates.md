---
layout: default
title: Templates
nav_order: 17
parent: Creating Reports
---
The template selected for a report specifies the overall layout of the report, such as what text goes in the page header and page footer, what default font to use for fields, how subtotals appear, and so on. It also specifies the paper size and margins. You can completely change the appearance of a report by simply selecting a different template. For example, here's a report using the Standard template:

![](/assets/images/standardtemplate.png)

Here's the same report with the only change being switching the template to Professional - Blue:

![](/assets/images/professionaltemplate.png)

{{ site.app_name }} comes with several built-in templates; they appear in the Template drop-down list in step 5 of the report wizards. These templates can be found in the Templates subdirectory of the App_Data subdirectory of the {{ site.app_name }} program folder. The template selected by default for a new report is the one specified by the *Default template* setting in the [Options]({% link _docs/configuration/configuration.md %}) dialog.

However, you aren't restricted to using these templates. You can use the Template Editor to edit the supplied templates or create your own. Click the *Templates* menu item under the tools menu to nagivate to a template management interface. There, you can *edit*, *copy*, or *delete* existing templates.

![](/assets/images/templateeditor.png)

To copy a template, select it and click the @icon-copy button (you create a new template by copying and then editing an existing one). You are prompted for the name for the new template.

To delete a template, click the @icon-trash button.

To edit the layout of a template, click the ![](/assets/images/document_text_image-edit.png) button. Template layouts are edited using the same Layout Designer window that the Advanced Report Designer tool uses; see the [Advanced Report Designer]({% link _docs/creating-reports/advanced-layout-designer/using-the-layout-designer.md %}) topic for details. You can add rectangles, lines, pictures (such as a company logo), and so forth. The objects in the template appear on every report using that template. You can also specify the paper size. However, due to its nature, there are a few differences between a template and a normal report:

![](/assets/images/template.png)

* Some objects in a template are placeholders, which indicate where a particular object in a normal report is placed and how it's formatted. For example, in the picture above, the Detail Band Field Template object is a placeholder specifying how fields in the Detail band of the report appear and Group Field Template is a placeholder for grouped fields. In some cases, if a placeholder object isn't defined in the template, the corresponding object in the normal report also won't appear.

* Some objects need to be moved or resized as the report width adjusts based on the number of fields that appear in the report. For example, the [ReportTitle] object stretches horizontally so it's as wide as the report and the Page Number object is moved to the right so it's at the right edge of the report.

> <span class="glyphicon glyphicon-info-sign" aria-hidden="true"></span> If you add an image to a template, the image file must exist in {{ site.app_name }}'s folder structure. We recommend putting it into the Images folder and referencing it from there in the template.

## Template components
A template has two types of components that define how a report looks: styles and objects. Styles are like style sheets in Microsoft Word: they define how objects of a certain type should look (font, color, and so on). Objects specify which styles are used by certain fields and which fixed objects should appear in the report, such as lines, boxes, image, etc.

There are templates that come with {{ site.app_name }} for both quick and cross-tab reports.

### Quick report templates
The quick report templates that come with {{ site.app_name }} have the following styles:

* *ColumnHeadingStyle*: used by column headings, such as the Column Heading Template object in the picture above.

* *DetailBandFieldStyle*: used by fields in the detail band, such as the Detail Band Field Template object in the picture above.

* *DetailBandFieldStyleEven*: used by fields in the even-numbered rows of the detail band if it exists.

* *DetailBandFieldStyleOdd*: used by fields in the odd-numbered rows of the detail band if it exists.

* *GroupCountStyle*: used by group counts in the group footer bands.

* *GroupFieldStyle1*: used by grouped fields in the lowest level group header, such as the Group Field Template object in the lower group footer band in the picture above.

* *GroupFieldStyle2*: used by grouped fields in the highest level group header, such as the Group Field Template object in the upper group footer band in the picture above.

* *GroupFooterStyle*: used by the "Totals for" object in a group footer band, such as the Group Footer Template object in the picture above.

* *GroupFooterSummaryFieldStyle*: used by summary fields in a group footer band, such as the Group Footer object in the picture above.

* *GroupHeadingStyle1*: used by the heading for grouped fields in the lowest level group header, such as the Group Heading object in the lower group header band in the picture above.

* *GroupHeadingStyle2*: used by the heading for grouped fields in the highest level group header, such as the Group Heading object in the upper group header band in the picture above.

* *HyperlinkStyle*: used by linked fields such as for drill downs.

* *SummaryFieldStyle*: used by summary fields at the end of the report, such as the Summary Field object in the ReportFooter band in the picture above.

See the [Styles]({% link _docs/creating-reports/advanced-layout-designer/styles.md %}) help topic for information on how styles work in the Layout Designer.

The templates that come with {{ site.app_name }} have the following objects:

* *Title*: displays the value of the ReportTitle parameter, which contains the title of the report. Its Tag property contains "PageFill," which means its width is expanded to fill the page.

* *Filter*: displays the value of the ReportFilter parameter, which contains the filter of the report. Its Tag property also contains "PageFill."

* *Date*: displays the current date.

* *PageNumber*: displays the current page number and total page count (for example, "Page 3 of 5"). Its Tag property contains "PageRight," meaning it's moved to the right edge of the page.

* *ColumnHeadingPanel*: a panel that acts as a container for column headings. Its vertical position determines the location of column headings and its Tag property contains "ColumnHeadingPanel," which is how {{ site.app_name }} knows it's a placeholder for column headings. Its Style property is set to "ColumnHeadingStyle."

* *ColumnHeadingTemplate*: a placeholder for column headings. It's placed inside ColumnHeadingPanel. If it isn't located within a panel, its vertical position determines the location of column headings within the panel; otherwise, the panel determines that. Its Tag property contains "ColumnHeadingTemplate," which is how {{ site.app_name }} knows it's a placeholder for column headings. Its Style property is set to "ColumnHeadingStyle." If this placeholder isn't defined in a template, then any reports using it won't have column headers.

* *GroupHeadingPanel*: a panel that acts as a container for grouped field headings. Its vertical position determines the location of grouped field headings and its Tag property contains "GroupHeadingPanel," which is how {{ site.app_name }} knows it's a placeholder for grouped field headings. Its Style property is set to "GroupHeadingStyle." There may be more than one of these; in that case, both Name and Tag are numbered (such as GroupHeadingPanel2) and Style is set to the appropriate style (such as GroupHeadingStyle2). The higher the number, the higher the group header band it's associated with. For example, if you've grouped on Company Name and within that on Order Date, GroupHeadingPanel2 is used for Company Name and GroupHeadingPanel1 is used for Order Date. If there are more than two grouped fields and only two group heading templates, GroupHeadingPanel1 is used for the third and subsequent group headings.

* *GroupHeadingTemplate*: a placeholder for grouped field headings. It's placed inside GroupHeadingPanel. Its horizontal and vertical position determines the location of grouped field headings and its Tag property contains "GroupHeadingTemplate." Its Style property is set to "GroupHeadingStyle". As with GroupHeadingPanel, there may be more than one of these and the same concepts apply.

* *GroupFieldTemplate*: a placeholder for grouped fields. It's placed inside GroupHeadingPanel. Its horizontal and vertical position determines the location of grouped fields and its Tag property contains "GroupFieldTemplate." Its Style property is set to "GroupFieldStyle". As with GroupHeadingPanel, there may be more than one of these and the same concepts apply.

* *DetailBandFieldTemplate*: a placeholder for detail fields. Its position isn't important but its Tag property contains "DetailBandFieldTemplate." Its Style property is set to "DetailBandFieldStyle".

* *GroupFooterTemplate*: a placeholder for the "Totals for" object in a group footer band. Its horizontal and vertical position determines the location of these objects and its Tag property contains "GroupFooterTemplate." Its Style property is set to "GroupFooterStyle". As with GroupHeadingTemplate, there may be more than one of these and the same concepts apply.

* *GroupFooterSummaryFieldTemplate*: a placeholder for summary fields in a group footer band. Its horizontal and vertical position determines the location of these objects and its Tag property contains "GroupFooterSummaryFieldTemplate." Its Style property is set to "GroupFooterSummaryFieldStyle". As with GroupHeadingTemplate, there may be more than one of these and the same concepts apply.

* *GroupFooterSummaryTypeTemplate*: a placeholder for summarization type in a group footer band. Its horizontal and vertical position determines the location of these objects and its Tag property contains "GroupFooterSummaryTypeTemplate". Its Style property is set to "GroupFooterSummaryFieldStyle". Use this template object to show the type of summary being performed for a given column in a group footer.

* *RecordCount*: displays the record count at the end of the report.

* *SummaryFieldTemplate*: a placeholder for summary fields at the end of the report. Its position isn't important but its Tag property contains "SummaryFieldTemplate." Its Style property is set to "SummaryFieldStyle".

* *SummaryFieldTypeTemplate*: a placeholder for summarization type at the end of the report. Its position isn't important but its Tag property contains "SummaryFieldTypeTemplate." Its Style property is set to "SummaryFieldStyle". Use this template object to show the type of summary being performed for a given column in a report footer.

A template may have other objects as well. For example, the Standard template has lines above and below the column headings and a line above the summary fields in the ReportFooter band. The Professional - Blue template, shown in the picture above, has panels in the PageHeader and GroupHeader bands that contain the placeholder objects and a line about the summary fields in the ReportFooter band.

### Cross-tab report templates
The cross-tab report templates that come with {{ site.app_name }} have the following styles:

* *ColumnHeadingStyle*: used by column headings.

* *DetailBandFieldStyle*: used by data fields in the detail band.

* *DetailBandFieldStyleEven*: used by fields in the even-numbered rows of the detail band if it exists.

* *DetailBandFieldStyleOdd*: used by fields in the odd-numbered rows of the detail band if it exists.

* *HeaderControlsStyle*: used by objects in the page header, such as the title and date.

* *HyperlinkStyle*: used by linked fields such as for drill downs.

* *RowHeadingStyle*: used by row fields if it exists.

* *RowHeadingStyle1*: used by the first row field if it exists.

* *RowHeadingStyle2*: used by the second row field if it exists.

See the [Styles]({% link _docs/creating-reports/advanced-layout-designer/styles.md %}) help topic for information on how styles work in the Layout Designer.

The cross-tab templates that come with {{ site.app_name }} have the following objects:

* *Title*: displays the value of the ReportTitle parameter, which contains the title of the report. Its Tag property contains "PageFill," which means its width is expanded to fill the page.

* *Filter*: displays the value of the ReportFilter parameter, which contains the filter of the report. Its Tag property also contains "PageFill."

* *Date*: displays the current date.

* *PageNumber*: displays the current page number and total page count (for example, "Page 3 of 5"). Its Tag property contains "PageRight," meaning it's moved to the right edge of the page.

* *ColumnHeadingPanel*: a panel that acts as a placeholder for column headings. Its vertical position determines the location of column headings and its Tag property contains "ColumnHeadingPanel," which is how {{ site.app_name }} knows it's a placeholder for column headings. Its Style property is set to "ColumnHeadingStyle."

A template may have other objects as well. For example, the CrossTab Elegant template has a line above the grand totals. Since grand totals are treated like any other line in the detail band of the report, a formatting rule called VisibleForTotalRule is used so it's only visible for the grand totals row. The condition for that rule is [ROWFIELD]='Grand total'. [ROWFIELD] is automatically replaced with the name of the row field, so the rule only takes effect when that field contains "Grand total". The line's Tag property contains "DataFill," which means its width is expanded to match that of the data.

You can also use rules to format the data for the grand totals row differently. If a rule named DetailRule exists, it's automatically applied to rows in the cross-tab. The CrossTab Elegant template has this rule use a bold font when [ROWFIELD]='Grand total'.

## Template parameters

Most built-in templates have several pre-defined parameters, including ReportTitle, ReportDatabase, and ReportFilter. The values for these parameters are set automatically by Horizon Reports when a report is run. You can also define an additional parameter in a template, and then drag the parameter to the report surface to display the value in the output. When a report uses a template with additional parameters, a prompt will appear for each parameter when the report is run. 