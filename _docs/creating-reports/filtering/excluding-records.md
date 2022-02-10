---
layout: default
title: Selecting Which Records to Exclude
nav_order: 2
parent: Filtering
grand_parent: Creating Reports
---
The Filter Conditions section in the Filter page of the report wizards allows you to determine which records to include in the report. The Exclude Conditions section allows you to specify which records to exclude from the report. We call this a "negative" query because it looks for the absence of data, such as all customers you didn't contact in 2007 or all customers who didn't buy Widgets.

You may think that the way to do this is to filter on Contact Date is not between 01/01/2007 and 12/31/2007 or Product Name is not equal to Widgets. However, this doesn't give the results you expect for two reasons:

* If you contacted the customer in 2006 or 2008, you'll get those records since they match the condition Contact Date is not between 01/01/2007 and 12/31/2007. However, that doesn't mean you didn't contact them in 2007. Similarly, you'll get all customers who bought anything other than Widgets but that doesn't mean they didn't buy Widgets at all.

* Because of the way database queries work, the absence of data means no records are retrieved using a normal filter condition. For example, if there are no activity records for a customer in 2007, there is nothing to retrieve from the database, so no customers are displayed.

The solution is to use an exclude filter. This tells {{ site.app_name }} to exclude those records matching the exclude conditions. For example, creating an exclude filter on Contact Date is between 01/01/2007 and 12/31/2007 means you want to exclude customers who have an activity record in 2007, which therefore gives you those customers who did not have an activity record in 2007. To get customers who didn't buy Widgets, use an exclude filter of Product Name equals Widget. This excludes those customers who bought Widgets, so it gives you everyone who didn't buy Widgets.

The way an exclude filter works is that it first takes all records, then it removes those matching the exclude conditions, leaving the rest, which obviously don't match the conditions.

Creating an exclude condition is just like creating a normal filter condition. The only difference is that the conditions you specify for an exclude filter are used to exclude records from the query rather than include as a filter would normally do.

Note that exclude conditions shouldn't be used in place of a normal "not equals" filter. For example, if you want a list of customers who aren't in Germany, use a normal filter condition of Country does not equal Germany rather than an exclude condition of Country equals Germany.