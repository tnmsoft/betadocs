---
layout: default
title: Formatting Values
nav_order: 12
parent: Creating Reports
---
The Field Properties settings in the report wizards allow you to change how a value is formatted in a report. These settings are accessible by clicking the Field Properties button in step 2 of the Quick Report, Cross-Tab Report, and Label Report Wizards; for the Chart Wizard, the settings are in step 3.

If the *Use default format* option is turned on, which it is by default, {{ site.app_name }} uses the defined format for the field. If the format for the field changes in the future, the report uses the new format automatically. If you wish to customize the format for the field, turn this setting off.

If *Use default format* is turned off, you can specify how the field should be formatted. For numeric fields, choose the desired format from the drop-down list of choices:

* *Currency, 2 decimal places*: this displays the currency symbol, the thousands separator, and two places after the decimal. The format string for this is "{0:c2}." For example, 4132 formatted using this setting displays as $4,132.00 in North America and &#128;4.132,00 in Germany.

* *Currency, no decimal places*: this displays the currency symbol, the thousands separator, and whole numbers. The format string for this is "{0:c0}." For example, 4132 formatted using this setting displays as $4,132 in North America and &#128;4.132 in Germany.

* *Thousands separator, 2 decimal places*: this displays the thousands separator and two places after the decimal. The format string for this is "{0:#,##0.00}." For example, 4132 formatted using this setting displays as 4,132.00 in North America and 4.132,00 in Germany.

* *Thousands separator, 2 decimal places, blank if zero*: this displays the thousands separator and two places after the decimal but displays as blank if the value is zero. The format string for this is "{0:#,##0.00;-#,##0.00;""}." For example, 4132 formatted using this setting displays as 4,132.00 in North America and 4.132,00 in Germany.

* *Thousands separator, no decimal places*: this displays the thousands separator and whole numbers. The format string for this is "{0:#,##0}." For example, 4132 formatted using this setting displays as 4,132 in North America and 4.132 in Germany.

* *Thousands separator, no decimal places, blank if zero*: this displays the thousands separator and whole numbers but displays as blank if the value is zero. The format string for this is "{0:#,##0;-#,##0;""}." For example, 4132 formatted using this setting displays as 4,132 in North America and 4.132 in Germany.

* *Percentage, 2 decimal places*: this displays a percentage to two decimal places. The format string for this is "{0:##0.00%}." For example, 0.94 formatted using this setting displays as 94.00% in North America and 94,00% in Germany.

* *Percentage, no decimal places*: this displays a percentage with no decimal places. The format string for this is "{0:##0%}." For example, 0.94 formatted using this setting displays as 94% in both North America and Germany.

You can also choose *Custom/empty format*. This allows you to enter a custom format string, which takes the form of "{0:*format*}," where *format* is a set of format symbols defining how the field is formatted. Commonly used format symbols are:

<table class="detailtable table-striped">
<tr>
<th>Symbol</th><th>Description</th>
</tr>
<tr>
<td align="center">c<i>n</i></td><td>Displays the value using the currency settings based on the TopicLink([Locale],[_04A0XWFXE]) setting (for example, "$" as the currency symbol, "," as the thousands separator, and "." as the decimal separator in North America) and the number of decimal places specified as <i>n</i>. For example, 4132 formatted as c2 displays as $4,132.00 in North America and &#128;4.132,00 in Germany.</td>
</tr>
<tr>
<td align="center">0</td><td>A place holder for a digit, padded with a zero if necessary. For example, 4132 formatted as 000000 displays as 004132.</td>
</tr>
<tr>
<td align="center">#</td><td>A place holder for a digit, blank if necessary. For example, 4132 formatted as #####0 displays as 4132.</td>
</tr>
<tr>
<td align="center">,</td><td>Displays the thousands separator symbol based on the Locale setting (for example, "," in North America). You only have to specify the character once, not once every three places. For example, 4132 formatted as #,##0 displays as 4,132 in North America and 4.132 in Germany.</td>
</tr>
<tr>
<td align="center">.</td><td>Displays a decimal separator symbol based on the Locale setting (for example, "." in North America). For example, 4132 formatted as #,##0.00 displays as 4,132.00 in North America and 4.132,00 in Germany.</td>
</tr>
<tr>
<td align="center">%</td><td>Multiplies the value by 100 and appends a percentage sign. For example, 0.132 formatted as ##0.00% displays as 13.20%.</td>
</tr>
<tr>
<td align="center">d<i>n</i></td><td>For a numeric value, left-pads the value with zeros. For example, 10 formatted as d6 displays as 000010.</td>
</tr>
<tr>
<td align="center">d</td><td>For a date/time value, displays the value using the Short Date setting based on the Locale setting. For example, January 10, 2013 2:22:30 PM displays as 1/10/2013 in the U.S. and 10/01/2013 in France.</td>
</tr>
<tr>
<td align="center">D</td><td>Displays a date/time value using the Long Date setting based on the Locale setting. For example, January 10, 2013 2:22:30 PM displays as Thursday, January 10, 2013 in the U.S.</td>
</tr>
<tr>
<td align="center">g</td><td>Displays a date/time value using the Short Date setting based on the Locale setting, including the time without seconds. For example, January 10, 2013 2:22:30 PM displays as 1/10/2013 2:22 PM in the U.S.</td>
</tr>
<tr>
<td align="center">G</td><td>Displays a date/time value using the Short Date setting based on the Locale setting, including the time with seconds. For example, January 10, 2013 2:22:30 PM displays as 1/10/2013 2:22:30 PM in the U.S.</td>
</tr>
<tr>
<td align="center">t</td><td>Displays a date/time value using the Short Time setting based on the Locale setting. For example, January 10, 2013 2:22:30 PM displays as 2:22 PM in the U.S.</td>
</tr>
<tr>
<td align="center">T</td><td>Displays a date/time value using the Long Time setting based on the Locale setting. For example, January 10, 2013 2:22:30 PM displays as 2:22:30 PM in the U.S.</td>
</tr>
</table><br />

You can specify how positive, negative, and zero values are displayed by separating the three formats with semi-colons. For example, {0:#,##0.00;-#,##0.00;""} formats positive numbers as #,##0.00, negative numbers as -#,##0.00, and zero as blank.

Other symbols can be used as well; see MSDN (such as <a href="http://msdn.microsoft.com/en-us/library/0c899ak8.aspx" target="top">http://msdn.microsoft.com/en-us/library/0c899ak8.aspx</a>, <a href="http://msdn.microsoft.com/en-us/library/dwhawy9k.aspx" target="top">http://msdn.microsoft.com/en-us/library/dwhawy9k.aspx</a>, and <a href="http://msdn.microsoft.com/en-us/library/az4se3k1.aspx" target="top">http://msdn.microsoft.com/en-us/library/az4se3k1.aspx</a>)

For date/time fields, the choices are shown in the following table. Note that not all choices are available for all types of reports; for example, Quarter is only available for cross-tab reports.

<table class="detailtable table-striped">
<tr>
<th>Format</th><th>Description</th><th>Example</th>
</tr>
<tr>
<td>Date</td><td>Displays only the date portion of the date.</td><td>09/25/2015</td>
</tr>
<tr>
<td>Date and time, 12 hour format</td><td>Displays the date and time in 12 hour format without seconds.</td><td>09/25/2015 1:15 PM</td>
</tr>
<tr>
<td>Date and time, 12 hour format (seconds)</td><td>Displays the date and time in 12 hour format with seconds.</td><td>09/25/2015 1:15:00 PM</td>
</tr>
<tr>
<td>Date and time, 24 hour format</td><td>Displays the date and time in 24 hour format without seconds.</td><td>09/25/2015 13:15</td>
</tr>
<tr>
<td>Date and time, 24 hour format (seconds)</td><td>Displays the date and time in 24 hour format with seconds.</td><td>09/25/2015 13:15:00</td>
</tr>
<tr>
<td>Time, 12 hour (HH:MM:SS)</td><td>Displays the time in 12 hour format with seconds.</td><td>1:15:00 PM</td>
</tr>
<tr>
<td>Time, 12 hour (HH:MM)</td><td>Displays the time in 12 hour format without seconds.</td><td>1:15 PM</td>
</tr>
<tr>
<td>Time, 24 hour (HH:MM:SS)</td><td>Displays the time in 24 hour format with seconds.</td><td>13:15:00</td>
</tr>
<tr>
<td>Time, 24 hour (HH:MM)</td><td>Displays the time in 24 hour format without seconds.</td><td>13:15</td>
</tr>
<tr>
<td>Day</td><td>Displays the day number.</td><td>25</td>
</tr>
<tr>
<td>Day of week</td><td>Displays the spelled-out day.</td><td>Friday</td>
</tr>
<tr>
<td>Abbreviated day of week</td><td>Displays the abbreviated spelled-out day.</td><td>Fri</td>
</tr>
<tr>
<td>Month</td><td>Displays the spelled-out month.</td><td>September</td>
</tr>
<tr>
<td>Abbreviated month</td><td>Displays the abbreviated spelled-out month.</td><td>Sep</td>
</tr>
<tr>
<td>Month/year</td><td>Displays the spelled-out month and year.</td><td>September 2015</td>
</tr>
<tr>
<td>Abbreviated month/year</td><td>Displays the abbreviated spelled-out month and year.</td><td>Sep 2015</td>
</tr>
<tr>
<td>Year</td><td>Displays the year.</td><td>2015</td>
</tr>
<tr>
<td>Hour</td><td>Displays the hour.</td><td>10</td>
</tr>
<tr>
<td>Quarter</td><td>Displays the quarter as a digit</td><td>3</td>
</tr>
<tr>
<td>Quarter/Year</td><td>Displays the quarter and year.</td><td>Q3 2015</td>
</tr>
</table>
