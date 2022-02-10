---
layout: default
nav_order: 4
title: Logging In
parent: Home
---
Before you can access {{ site.app_name }}, you have to log in. Enter the user name and password you were assigned (initially, these are both "admin").

{% if site.has_multidatasource %}
You can also choose the data source you wish to use (a data source is a particular database you want to report on). You can change to a different data source any time by choosing the Change Data Source function from the Tools menu.
{% endif %}
{% if site.users_can_register %}

If you don't have a user name, click the *Click here to register if you don't have an account* link and enter your email address when prompted. Your email address is your user name and you'll be emailed a password to use, which you can later change using the Change Password function in the Tools menu if you wish.
{% endif %}

{% if site.allow_password_reset %}

If you don't remember your password, click the *Forgot password?* link and enter your user name. An email will be sent to you with instructions on resetting your password. You'll need to have your email address filled in for this process to work.

{% endif %}


When you first use {{ site.app_name }}, it runs as a {{ site.demo_days }}-day "unactivated" version. This version has all of the features of the full-working program, except it only functions for {{ site.demo_days }} days after running it for the first time. Once the unactivated period has expired, the following message appears on the Login page: "The demo period has expired. Please log in with an administrator account to resolve this issue." As the message suggests, login as "admin" or some other administrative user. See the [Managing Licenses]({% link _docs/configuration/manage-licenses.md %}) topic for information on how to add a license or enter an extension code.
{% if site.manage_dsn %}

{{ site.app_name }} connects to your database using an ODBC data source name (DSN). The first time you run it, no DSNs have been set up in {{ site.app_name }}, so you are prompted to go to the Setup Wizard to do so.
{% endif %}

{% if site.manage_conn_string %}

{{ site.app_name }} connects to your database using a connection string. The first time you run it, the connection string hasn't been set up in {{ site.app_name }}, so you are prompted to go to the Setup Wizard to do so.
{% endif %}

The [Reports Explorer]({% link _docs/creating-reports/reports-explorer.md %}) appears next. You can select an existing report and print or preview it, or create a new report if you are using a [Report Designer license]({% link _docs/licensing.md %}).

To display help information, choose Help Topics from the Help menu.