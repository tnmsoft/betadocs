---
layout: default
title: Stonefield Query 1.5
nav_order: 11
parent: Previous Releases
grand_parent: Home
---

# New Features

* Multi-tenant environments are now supported.

* There were several changes to the Security dialog. The biggest change is that you now have fine control over which features users can access. For example, you can specify that members of a particular role can edit the properties of the fields in a report but not add or remove fields. Also, the Users tab now has an email address setting for each user; the Submit Support Ticket dialog includes the email address of the user so it can be changed if necessary. The License Type dropdown list now just displays Report Designer and Report Viewer. There is no longer a Report tab in the Roles tab.

* You can now specify that a report should not be automatically localized but instead run in the language it was created in.

* Copying a report now gives full rights to the copy to the user who copied it. That way, there is no problem with the user editing or deleting the report.

* Step 6 of the report wizards was changed to make it more clear about which roles have no access, which have read access, and which have full access to the report. Also, an administrative user can now change the "owner" of a report. A user can now see reports they own even if their roles don't have access to the report.

* Fields in the Data section of step 3 in the Cross Tab Wizard now display how they are summarized.

* More built-in field formats, especially for DateTime and TimeSpan fields, are now available. Also, custom formats now appear as "{0: format }".

* The Is Yes and Is No filter operators now appear as Is True and Is False to match the values displayed in a report.

* The scroll bar used for several controls, such as the field lists in step 2 of the report wizards, is now a standard scroll bar rather than the "slim" style used in the previous version.

* Ask-at-runtime is now supported for filter conditions on True/False fields.

* Adding a field or function to the expression of a formula now puts the field or function at the cursor position rather than at the end of the expression.

* The Advanced Properties dialog no longer has AfterData and AfterRun scripts.

* Online activation now supports unlimited license files.

* Dialogs, such as the report preview window and the ask-at-runtime condition dialog, are now cleaner and more consistent. Focus is now automatically set to the first control in dialogs and wizards.

* Processes that take some time now display a progress indicator. For example, when running a report, such an indicator appears on the Preview button.

* Notifications displayed to the user, such as when a problem with running a report occurs, now appear in a special notification window.

* The Import Report dialog now has a button to start the import.

## Bug Fixes

* Users are now sorted alphabetically in the Security dialog.

* Dialog close buttons are now completely visible in Internet Explorer.

* The Formula Editor now appears correctly when using different themes.

* Step 1 of the report wizards now sets the data group for a report properly when the Show All Data Groups setting is turned on.

* You can now enter values earlier than 1970-01-01 for filter conditions on date fields.

* Adding a formula to a table now assigns it the correct order so it appears at the end rather than the beginning of the list of fields when fields are displayed in database order.

* A bug that caused a "this isn't the first condition and Connection is blank" error when running a report that has a formula field in the first filter condition was fixed.

* Stonefield Query no longer gives an error if a report's SFX file is manually removed.

* Grouping on a date/time field formatted as date now properly groups the values for the report.

* Changing the name of a user in the Security dialog now works correctly.

* A bug that caused an error if a report the current user can see has a tag they cannot was fixed.

* Several issues with running Stonefield Query in Microsoft Internet Explorer were fixed.

* A bug that allowed a user to edit a report they don't have rights to was fixed.

* The report preview window no longer displays the results of the previous report run while the report is being rendered.

* You can no longer edit the All Reports tag in the Tag Editor.

* The Compare To control no longer appears in step 4 of the report wizards for the Is Blank, In Not Blank, Is One Of, Is Not One Of operators.

* Cancelling changes to a user or role in the Security dialog no longer changes the selected user or role.

* The Advanced Report Properties button in step 5 of the report wizards is now disabled when there are no fields in the report.

* An issue where some icons didn't appear correctly when using the Chrome browser on a Windows 8 machine was fixed.

* A bug that caused an error when an invalid extension code is entered in the Setup dialog was fixed.