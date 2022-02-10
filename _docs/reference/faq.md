---
layout: default
title: Frequently Asked Questions
nav_order: 2
parent: Reference
---
## Database Issues
**I'm not getting the results I expect in a report. It looks like some records are missing.**

The first thing to check is that you have the correct filter for the report. If the filter is too restrictive, you won't see all the records you expect. The second thing to check is that {{ site.app_name }} is accessing the correct database. Finally, if your database has a "reindex" or "database maintenance" feature, use that feature to ensure the database indexes are accurate.

## Error Messages

**When I run a report, I get an error message. What should I do?**

If a dialog appears asking you to create a support ticket, type any information you think would be useful and click the OK button to create the ticket. You will receive a response to the ticket by email, but note that this means the email information in the [Options]({% link _docs/configuration/configuration.md %}) dialog has to be set up correctly.

## Other Problems

**{{ site.app_name }} seems quite slow when I run a report.**

This can be caused by a lot of things, some of which you likely can't control (such as a busy network, a slow network, etc.) and others you can. Note that rendering a lot of pages can take some time, so try using a filter that returns a smaller set of records.

**{{ site.app_name }} seems slow loading reports after I log in.**

If you have a lot of reports (hundreds or even thousands), it can take a little while to load all those reports. A few things you can do to improve performance are:

* Close the "All reports" tag so it doesn't have to load every single report after you log in.

* Close other report tags so they aren't open.

* Use Google Chrome as your browser; it's much faster than Microsoft Internet Explorer and Firefox.

* If a view of all reports is necessary, use Flat View since performance is better.

* If you're using Internet Explorer, make sure your browser isn't displaying the site in Compatibility View. To change that, choose the Tools (gear) icon, select "Compatibility View Settings," and turn off "Display intranet sites in compatibility view."

**A report I want to schedule doesn't appear in step 2 of the Schedule Wizard.**

Only reports without [ask-at-runtime]({% link _docs/creating-reports/filtering/including-records.md %}) filter conditions are displayed, since a schedule can't stop to ask for the values of such a report.

**Some of the data in my report uses characters in languages other than English, such as Thai or Chinese. When I preview the report, it displays these characters correctly. However, when I output to PDF, they appear as boxes.**

Unicode characters are only displayed properly when the font contains appropriate glyphs (/assets/images/ that represent characters). Thus, you need to use a font, such as Arial Unicode MS or MS Gothic, whicht contains all the necessary glyphs for the desired language. You can use one of the "Unicode" templates, which use Arial Unicode MS, or create your own [template]({% link _docs/creating-reports/templates.md %}). If you're interested in reading about glyphs, see the <a href="http://www.microsoft.com/typography/unicode/cscp.htm" target="top">Character sets and codepages</a> article on the Microsoft web site.

**I'm getting an "unknown error" when trying to activate my license.**

This error can occur if you're using a proxy server on your network. To tell your browser about these settings, do the following:

* Open the Windows Control Panel.

* Choose Network and Internet.

* Choose Internet Options to open the Internet Properties dialog.

* On the Connections tab, click the *LAN settings* button. Turn on *Use a proxy server for your LAN* and enter the proxy server address and port number.

**Labels don't appear on the x-axis of my chart.**

This can happen if the labels are very long. In that case, increase the height of the chart in step 5.

## Features

**Can you create formulas?**

Yes, you can create formulas for a report using [Formula Editor]({% link _docs/creating-reports/formulas.md %}).

**Can you suppress sections of the report?**

{{ site.app_name }} has a "summary report" feature that suppresses all detailed fields that have not been grouped. Also, you can use the [Advanced Report Designer]({% link _docs/creating-reports/advanced-layout-designer/using-the-layout-designer.md %}) to change anything you wish in headers, footers, etc.

**Can you parse string fields, such as looking for data in the first two positions of a field?**

You can create a filter that uses the "contains" or "begins with" operator.

**How do I backup reports and {{ site.app_name }}'s data files.**

The App_Data subdirectory of the {{ site.app_name }} program folder contains everything you need to back up: reports, templates, user settings, and the database containing users, roles, tags, and other settings. Be sure to backup App_Data and all subdirectories.

## Reporting

**How do I sort on a field that doesn't appear in the report?**

You can only sort on fields that are included in the report. If you want to sort on a field that doesn't appear in the report, add the field to the report and in the [Field Properties dialog]({% link _docs/creating-reports/formatting-values.md %}), turn off the *Display in report* setting. This tells {{ site.app_name }} to not display that field in the report but to still retrieve it from the database. You can then sort on this field in the sort step of the report wizard.

**How can I show a count of each group in a summary report?**

Turn on the *Include count in group footer* setting for the grouped field.

**How do I use more than 10 values in a "is one of" filter?**

You can chain "is one of" conditions by specifying 10 values for the first one, then adding another condition using "or" as the connection, specifying the same field, choosing "is one of" for the operator, and entering another 10 values.

**When I preview a report, I see the top half of a line of text at the bottom of one page and the bottom half on the top of the next page.**

This is caused by word wrapping lines with certain printer drivers. To resolve this issue, in step 2 of the Quick Report Wizard, click Field Properties and on the Format page, turn off *Word wrap* for all fields but those that contain multiple lines of text.

**I'm using the Pervasive database engine and when I filter on a certain character field, I'm not getting all the records I expect.**

This can happen when character fields are padded with binary zeros instead of spaces. See <a href="http://support.pervasive.com/t5/PSQL-Knowledge-Base/Disabling-ANSI-Padding-for-ODBC-applications/ta-p/11423" target="top">http://support.pervasive.com/t5/PSQL-Knowledge-Base/Disabling-ANSI-Padding-for-ODBC-applications/ta-p/11423</a> for a solution to this issue. Note that on a 64-bit system, the correct Registry key may be
HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\ODBC\ODBC.INI\*DSNname*.

**How can I turn off pagination in a report? I want a report that's just one long page.**

In step 5 of the report wizard, turn off *Use template paper type*, set the paper type to Custom, and enter a large value for Height, such as 100000.

**The layout of my report doesn't look quite right: some things aren't in the correct location.**

By default, {{ site.app_name }} uses absolute positioning to render a report in the Preview window. While that normally works well, under some conditions, you may wish to use HTML tables instead. In that case, turn off the *[Use table layout]({% link _docs/creating-reports/templates.md %})* setting in step 5 of the report wizard.
