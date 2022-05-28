---
layout: default
nav_order: 6
title: Licensing
parent: Home
---

{{ site.app_name }} is licensed on a per-user basis. That means each user who wants to create and/or run reports requires a license. Here's how licensing works:

* Until {{ site.app_name }} has been activated, it runs in "unactivated" mode. You can use it this way for up to {{ site.demo_days }} days after the first time it was run. To activate the software, use the [License Manager]({% link _docs/configuration/manage-licenses.md %}) to add a license.

* Licensing information is stored in a file named SFQuery.lic in the Licenses subdirectory of the program folder.

* There are two types of licenses: Report Designer and Report Viewer. A Report Designer license allows a user to create new reports, edit reports, and copy reports. With a Report Viewer license, the user can only run reports.

* There's a subset of these license types: Subscription. A normal license can be used even if your [software maintenance]({% link _docs/software-maintenance.md %}) expires because you've purchased the software. A subscription license, on the other hand, isn't purchased outright but is instead paid for on a subscription basis similar to subscribing to a magazine. If you stop making subscription payments, the license becomes inactive and you can no longer use the software.

* Users in the Administrator role (such as the ADMIN user) are the only ones who have access to the [Security]({% link _docs/configuration/security.md %}) dialog. In that dialog, an administrative user can define user names and specify which users use which license type. For example, Mary may be assigned a Report Designer license while Bob gets a Report Viewer license.

* When you log in, {{ site.app_name }} does two checks. The first is how many users are currently running {{ site.app_name }}. If all licenses are currently in use (for example, five users are currently in {{ site.app_name }} and there are five licenses in total), you are informed of this and returned to the Login page. The second check is whether another user is logged in with the same user name. If so, you are informed of this and returned to the Login page. So, {{ site.app_name }} licensing is sometime called "concurrent use" because only as many users as there are licenses can be logged in at the same time.

The Setup function in the Tools menu, which is only available for users in the Administrator role, can be used to [manage licenses]({% link _docs/configuration/manage-licenses.md %}).