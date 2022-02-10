---
layout: default
title: Step 6 Security
nav_order: 6
parent: Creating a Label Report
grand_parent: Creating Reports
---
The options in Step 6 allow you to determine who can access your report and what they can do with it.

![](/assets/images/wizardstep6.png)

To specify that members of a role can run but not edit or delete the report, drag the role from the *Available roles* list to the *Roles with read permission* list. To specify that members of a role can run, edit, or delete the report, drag the role from the *Available roles* list to the *Roles with full permission* list. To remove permissions for a role, drag it back to the *Available roles* list; members of that role cannot see or run the report. The Administrator role doesn't appear in any list because members of that role have full permission to all reports.

*Report owner*, which only appears if an administrative user is editing the report, allows you to select the user who "owns" the report. The only thing this affects is that the report owner can edit the report even if the security settings for the report would indicate otherwise. The default report owner is the user who created it.