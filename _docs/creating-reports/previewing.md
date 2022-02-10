---
layout: default
title: Previewing a Report
nav_order: 3
parent: Creating Reports
---
To preview a report, click the report name in the Reports Explorer or click the ![](/assets/images/printicon.png) button.

![](/assets/images/preview.png)

The Report Preview toolbar provides the following functions:

![](/assets/images/previewtoolbar.png)

Charts preview in a slightly different window without a toolbar. However, both preview toolbars also have a button for Export Options and Back (for navigating back from a drillthrough, for example).

If you turn on the *Create bookmark on this field* setting for a grouped field, the Preview window includes a "document map" with links to jump to the various values of the field.

![](/assets/images/previewdocmap.png)

The search button displays a dialog in which you can enter text to search for in the report.

![](/assets/images/previewsearch.png)

Enter the text to search for and click Find Next to find and highlight the next instance of that text. Turn on *Match whole word only* to match what you type as a whole word or *Match case* for a case-sensitive search. You can search up or down from the current location in the report by choosing the appropriate direction.

The export button exports the report to the type of file specified in the drop-down list. The types of files supported are:

* *Pdf*: select this to output to a Portable Document Format (PDF) file. This type of file can be opened in Adobe Acrobat Reader or other PDF reader applications.

* *Xls*: this outputs the fields that appear in the report to a Microsoft Excel 97-2003 spreadsheet with minimal formatting.

* *Xls Full Format*: this outputs the report to a Microsoft Excel 97-2003 spreadsheet with formatting so it closely resembles the preview.

* *Xlsx*: this outputs the fields that appear in the report to a Microsoft Excel 2007 or later spreadsheet with minimal formatting.

* *Xlsx Full Format*: this outputs the report to a Microsoft Excel 2007 or later spreadsheet with formatting so it closely resembles the preview. In the case of a cross-tab report, the Excel document contains a PivotTable that works just like the cross-tab report.

* *Rtf*: this outputs to a Rich Text Format (RTF) file. This type of file can be opened in many types of word processors including Microsoft Word.

* *Mht*: this outputs the report to an MHTML (short for MIME HTML) document. MHTML includes external resources, such as images, in the HTML document.

* *Txt*: this outputs the fields that appear in the report to a text file. The text file is formatted as fixed-length fields, meaning that each field takes up a fixed amount of space and there are no separators between fields. Records are terminated with a carriage return.

* *Csv*: this outputs the fields that appear in the report to a delimited (also known as comma-separated values or CSV) text file. Each field in the file only takes up as much space as needed, and a comma is used to separate fields. Records are terminated with a carriage return.

* *Bmp*,  *Gif*,  *Jpeg*,  .png*,  *Tiff*: these output the report to the type of image file selected. Note that since an image can contain only one page, the entire report is output to one long page.

* *Xml*: this outputs the data for the report to an XML document.

Note that if the *Output each group as separate file* [export option]({% link _docs/creating-reports/exporting.md %}) is turned on, a separate file for each group is created and the individual files are zipped up into a single file which is downloaded to your browser. Also, if the *Password* option is filled in and you output to something other than a PDF file, the file is added to an encrypted ZIP file using the same name as the output file but with a "zip" extension.

Click the Export Options button to display the [export options dialog]({% link _docs/creating-reports/exporting.md %}); this dialog allows you to specify email and FTP settings. The email and FTP buttons use these settings to determine who to email the report to or where to upload the report to. If you didn't set any export options, you'll get a warning message indicating that the options weren't set up when you click those buttons.

If no records were found that match the specified filter, one of two things happens:

* If you turned on the *Run report with no records* option in step 5 of the [report wizard]({% link _docs/creating-reports/templates.md %}), a blank report is output.

* If you turned that option off, a message that there are no records displays.
