---
layout: default
title: Tags
nav_order: 2
parent: Creating Reports
---

Tags allow you to categorize a report. You can mark a report as being a management report, a weekly report, a favorite report, and one of your reports. You do that by assigning as many tags to the report as you wish. Reports are displayed in the Reports Explorer grouped by tag. If a report has more than one tag, it'll appear in more than one group.

A tag can be a sub-tag of another tag. For example, you may have a Management Reports tag with Daily, Weekly, and Monthly sub-tags. Sub-tags appear within the section for the parent tag.

![](/assets/images/subtags.png)

Tags can be dynamic. A dynamic tag is one that you don't add to a report; in fact, dynamic tags don't even appear in the list of tags you can add to a report. Instead, all reports that match a certain criteria automatically belong to that tag. For example, you might have a dynamic tag that's for all reports you created.

One dynamic tag that's built-in and can't be edited or deleted is called "All Reports." All reports automatically use this tag. The main purpose of the All Reports tag is to provide a place for reports you didn't tag to be displayed.

You can manage tags using the Tags dialog, which you can access using the Tags function in the Tools menu. Note that depending on how security is set up, the Tags dialog may not be available to all users.

![](/assets/images/tageditor.png)

The list shows which tags have already been defined and buttons to edit, copy and delete them. There's also a column of values that shows how many reports each tag has been assigned to. To add a tag, click the Create New Tag button. To edit the properties of a tag, click Edit button for the tag.

{% if site.has_tenants %}
![](/assets/images/edittagtenant.png)
{% else %}
![](/assets/images/edittag.png)
{% endif %}

The properties for a tag are:

* *Tag name*: the name of the tag.

* *Parent tag*: the parent tag this is a sub-tag of. Leave it blank it it's a top-level tag. This property isn't available for dynamic tags.

* *Expression*: the expression to use for a dynamic tag; leave this blank for a regular tag. You can use any valid expression, including [built-in functions]({% link _docs/reference/function-reference.md %}). For example, this expression includes any report created or modified in the last five days:

        DateDiff(Now(), Report.CreatedAt) <= 5 or
            DateDiff(Now(), Report.ModifiedAt) <= 5

    The Now function gives today's date and the DateDiff function determines the number of days between two dates. CreatedAt and ModifiedAt are properties of reports containing the date a report was created and modified, respectively. Properties are specified using "Report.*PropertyName*", where *PropertyName* is the name of the property. So, DateDiff(Now(), Report.CreatedAt) is the number of days between today and when the report was created, and DateDiff(Now(), Report.CreatedAt) <= 5 is true if the number of days is less than or equal to 5.

    Here's another expression:

        Report.CreatedBy = "BJONES"

    This tag is automatically used by any report created by a user named BJONES.{% if site.has_tenants %}

* *Tenant*: this control, which only appears if you're an administrative user, allows you to define which tenant the tag belongs to. Choose the desired tenant from the drop-down list or choose *No tenant* if the tag is available to all tenants.
{% endif %}

To specify that members of a role can view this tag and assign it to reports, drag the role from the *Available roles* list to the *Roles that can access this tag* list. To remove permissions for a role, drag it back to the *Available roles* list; members of that role cannot see the tag or assign it to reports. The Administrator role doesn't appear in any list because members of that role have full permission to all reports.

To delete a tag, click the Delete button for the tag. This doesn't delete any reports; it just removes that tag from any reports that use it.