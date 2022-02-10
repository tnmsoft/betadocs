---
layout: default
title: SQL Passthrough
nav_order: 10
parent: Creating Reports
---
A SQL Passthrough report isn't like other report types. Instead, it's a method for creating one of the existing report types (Quick, Cross-Tab, Chart, or Label) using a pre-defined SQL statement.

To create a SQL Passthrough report, choose *SQL Passthrough* from the New menu.

![](/assets/images/sqlpassthrough.png)

Choose the type of report you'd like to create, and then type or paste your SQL statement into the space provided. You can resize that space by dragging the lower right corner with the mouse.

If you need to specify any parameters for the SQL statement, use a **?** as the placeholder for the value. You can then specify a data type, caption, and value for the parameter in a list below the SQL statement.

Once you click the *OK* button, the SQL statement is executed against the database, which may take a while depending on the size of the query. The results are used to build a report of the type you chose initially. Once finished, the appropriate wizard for that report type opens, allowing you to make final changes to the report.

For a more in-depth discussion of the individual steps in the wizard, please see the appropriate help file topic ([Quick Report]({% link _docs/creating-reports/quick-reports/index.md %}), [Cross-Tab Report]({% link _docs/creating-reports/cross-tab-reports/index.md %}), [Label Report]({% link _docs/creating-reports/label-reports/index.md %}), or [Chart Report]({% link _docs/creating-reports/chart-reports/index.md %})).

When working with the wizard steps in a report created using SQL Passthrough, the *Available Fields* list aren't visible in [Step 2]({% link _docs/creating-reports/formatting-values.md %}) since the fields for a SQL Passthrough report are defined by the SQL statement you entered.

![](/assets/images/SQLPassthroughStep2.png)