---
layout: default
title: Scripts
nav_order: 8
parent: Advanced Layout Designer
grand_parent: Creating Reports
---
Scripts allow you to specify code to execute for specific events during a report run. This can be used to display something different than the actual value of a field, to perform custom summarization, and other tasks. {{ site.app_name }} uses scripts for report linking to tell the Preview window when a subreport should be displayed and what to do when the user clicks a hyperlinked field. Writing scripts requires knowledge of the C#, Visual Basic .NET, or JScript .NET languages so it's intended for programmers only.

All the scripts for a report must be written in the same language; this language is specified in the *Script Language* report property.

To edit the scripts for a report, click the Scripts button (![](/assets/images/scriptsbutton.png)) in the Report Designer toolbar.

![](/assets/images/scriptsbrowser.png)

The editor area shows the script code. This is a typical text editor but uses color coding to help with syntax. At the left edge is a strip to display line numbers. Small arrows appear to the right of the line numbers; clicking an arrow collapses or expands a code block.

The Control drop-down list in the toolbar lists the objects in the report. The Event drop-down list beside the Control list displays the events for the selected object. Choosing one from the list either creates a script to handle that event or moves the editor to that script if it already exists.

The Validate button in the toolbar examines the script code and displays any errors it finds as a red X in beside the line numbers at the left edge of the window. Hover your mouse pointer over the X to see the error message.

The scripts for a report are organized like a typical .NET class but without the "class" definition. There may be using statements, fields, properties, and methods. Event handler methods are usually named *ObjectName*_*Event*, where *ObjectName* is the name of the object and *Event* is the event being handled for that object.

If you created a script by selecting an event name from the list at the top, the script is automatically associated with that event for the object. However, you can also do that manually by expanding the Scripts property for an object and choosing the desired handler from the drop-down list for a specific event.

Here's an example where a script is useful: custom summarization. Suppose you want to show the total number of boxes of product units on order, where there are 15 items per box. Add a label to a group footer band of the report and set its data binding to the field containing the units on order. In the Properties Panel, set the Function sub-property of its Summary property to "Custom," the Format String sub-property to "Total boxes: {0}," and the Running sub-property to "Group." Expand the label's Script property and click "..." for the Summary Reset, Summary Row Changed, and Summary Get Result events to create script code for them. Use code like the following for these scripts:

```csharp
// Declare a summary and a box.
double totalUnits = 0;
double box = 15;

private void xrLabel1_SummaryReset(object sender,
    EventArgs e) {
    // Reset the result each time a group is printed.
    totalUnits = 0;
}

private void xrLabel1_SummaryRowChanged(object sender,
    EventArgs e) {
    // Calculate a summary.
    totalUnits += Convert.ToDouble(
        GetCurrentColumnValue("UnitsOnOrder"));
}

private void xrLabel1_SummaryGetResult(object sender,
    SummaryGetResultEventArgs e) {
    // Round the result, so that a pack will be taken
    // into account even if it contains only one unit.
    e.Result = Math.Ceiling(totalUnits / box);
    e.Handled = true;
}

```

The SummaryReset method resets the total number of units to 0 when a group breaks. SummaryRowChanged fires on every record, so it adds the current value of the UnitsOnOrder field to the total. SummaryGetResult is called when the summary value is needed (that is, when the label is about to be printed); it calculates the number of boxes by dividing the total number of units by the units per box.

<!-- This was taken from https://documentation.devexpress.com/#XtraReports/CustomDocument4817. See also https://documentation.devexpress.com/#XtraReports/CustomDocument2615 and https://documentation.devexpress.com/#XtraReports/CustomDocument2617
-->