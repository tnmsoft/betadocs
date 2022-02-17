---
layout: default
title: Managing Reports
nav_order: 3
parent: Configuration
---
You may find a need for a report that is similar to an existing report. The Copy function allows you to copy an existing report; you may then edit the copy to create the desired report. To select the Copy function, click the ![](/assets/images/copyicon.png) button beside the report name. You are prompted for the name for the copy of the report. After entering it and clicking OK, the copy of the report appears in the list in the Reports Explorer.

To delete the selected report, click the ![](/assets/images/deleteicon.png) button beside the report name. You are asked to confirm that the report should be deleted. If you confirm its deletion, the report is removed from the list in the Reports Explorer. Note that if a report has more than one tag, deleting it from one tag deletes it from all other tags.

> <span class="glyphicon glyphicon-info-sign" aria-hidden="true"></span> This button may not be enabled for all reports.

If you need to delete multiple reports at once, or assign a tenant or role to multiple reports, you can use the Manage Reports dialog to do so.
{% if site.has_tenants %}
![](/assets/images/managereportstenant.png)
{% endif %}

{% unless site.has_tenants %}
![](/assets/images/managereports.png)
{% endunless %}
 The Manage Reports dialog displays a list of all reports in alphabetical order. You can one or several reports by clicking in the left-most column beside each report. You can also select all reports in the list by clicking in the top left hand corner of the report list.

Once you've selected the report(s) you'd like to manage, you can choose one or more roles to apply to them. You also have the option of changing the tenant for all selected reports.", "")

After making changes, you can save them with the  ![](/assets/images/savechangesbutton.png) button, or cancel them with the ![](/assets/images/cancelchangesbutton.png) button.

You can delete all of the selected reports by clicking the ![](/assets/images/deletereportsbutton.png), then confirming the action on the dialog that appears.