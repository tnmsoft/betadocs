---
layout: default
title: Managing Licenses
nav_order: 2
parent: Configuration
---
The Setup function in the Tools menu, which is only available for administrators, allows you to view, add, or remove {{ site.app_name }} licenses. You can also enter an extension code if {{ site.app_name }} hasn't been activated and the unactivated period ({{ site.demo_days }} days after it's used for the first time) has expired.

For more information on how licensing works, see the [Licensing]({% link _docs/licensing.md %}) topic.

## Licenses

The list at the left shows the serial number for each installed license; click one in the list to select it. To the right are properties about the selected license. You cannot change any of the properties; they are displayed for information purposes only. The properties are:

![](/assets/images/setuplicenses.png)

* *Serial number*: the serial number of the license.

* *Activation code*: the code used to activate the license.

* *License type*: the type of license. A Report Designer license is a full license; users can create or run reports. A Report Viewer license is one in which users can only run reports; the New, Copy, and Edit functions in the Reports Explorer are disabled. A Subscription Report Viewer or Report Designer is a license that expires.

* *Number of seats*: the number of users of the license.

* *Expiry date*: for a Subscription license, this is the date that the subscription expires. After that date, the application cannot be used until the subscription is renewed. For any other license type, this is the software maintenance expiry date.

* *License status*: normally this displays Active. If it displays Inactive, the license has been disabled and isn't currently being used.

To increase the number of licenses, contact {{ site.company }} to obtain a serial number for the additional number of licenses you require. In the License Manager, click the ![](/assets/images/addround.png) button. There are a couple of ways you can add a license:

* If you have a serial number and an Internet connection, type the serial number and click the Activate Online button to activate the license immediately. If something goes wrong (for example, if the web server is down), you get a warning message and have to try again later.

* Contact [Technical Support]({% link _docs/technical-support.md %}) to obtain an activation code. Enter the serial number and the activation code and click the Activate Manually button.

To remove licenses, such as when you want to move a {{ site.app_name }} installation to another system, select the license to remove from the list and click the ![](/assets/images/deleteicon.png) button.

## Extension code

If you do not currently have a license, {{ site.app_name }} runs in unactivated mode. This mode is only allowed for {{ site.demo_days }} days; after that, you can't access any reports unless you activate the software by adding a license or enter an extension code.

If you haven't purchased a license and need more time to evaluate {{ site.app_name }}, you can request that the demo period be extended. Contact [Technical Support]({% link _docs/technical-support.md %}) to obtain an extension code, log in as an administrative user, click the Add Extension Code button, and enter the code.
