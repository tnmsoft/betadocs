---
layout: default
title: Expression Editor
nav_order: 9
parent: Advanced Layout Designer
grand_parent: Creating Reports
---
The Expression Editor appears when you click the "..." button for the *Condition* property of a [formatting rule]({% link _docs/creating-reports/advanced-layout-designer/formatting-rules.md %}) or for the *Expression* property of a [calculated field]({% link _docs/creating-reports/advanced-layout-designer/calculated-fields.md %}). This dialog helps with entering a valid expression.

![](/assets/images/expressioneditorbrowser.png)

There are several sections in this dialog:

* The large edit box at the top is where you enter the expression.

* The list of symbols across the dialog acts as a toolbar; click a button to insert that symbol into the current cursor position in the expression. The three buttons at the right are for And, Or, and Not.

* *Functions* displays a list of the built-in functions. Note that these functions are different than the ones listed in the *Expressions and Function Reference* topic; the functions in that topic are used in {{ site.app_name }} formulas while these ones are used in advanced layout report expressions.

* *Operators* shows the various operators you can use, such as + and -.

* *Fields* displays the fields in the result set for the report.

After entering the desired expression, click OK to save it.