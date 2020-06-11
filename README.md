# OpenACS Calendar 
This package is part of ]project-open[, an open-source enterprise project management system.

For more information about ]project-open[ please see:
* [Documentation Wiki](http://www.project-open.com/en/)
* [V5.0 Download](https://sourceforge.net/projects/project-open/files/project-open/V5.0/)
* [Installation Instructions](http://www.project-open.com/en/list-installers)

About OpenACS Calendar :

<p>The OpenACS calendar package is a web-based calendar package. In its current form it provides a UI for storing events that have a time or that last a day, and it offers a list view, a day, week, and month view. <p><img src="http://www.project-open.com/images/manual_screenshots/calender_view.png" /><h3>Permissions </h3><p> Calendar uses a lot of custom permissions. Most of them are unused and will be removed eventually. It will then use a Unix-like set of read, write, create, admin permissions. <h3>Calendars </h3><p> A calendar has a name and an owner and belongs to a package, it also is an acs_object. This goes into the table calendars. A calendar is created via the usual constructor - a &quot;new&quot; function&quot; - and destroyed via the usual destructor - a &quot;delete&quot; function. <p> The calendar package currently uses its own little category system: calendar item types can be created per package, they are stored in the table cal_item_types <p> The table cal_party_prefs allows storing customization information per calendar and per user. It is completely unused and I couldn&#39;t find any traces of it ever having been used. A similar table will be used in a future version of calendar to store user options though. 

# Online Reference Documentation

## The Data Model



## Procedure Files

<table cellpadding="0" cellspacing="0"><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/procs-file-view?version_id=100649&amp;path=packages/calendar/tcl/apm-callback-procs.tcl">tcl/apm-callback-procs.tcl</a></b></td><td></td><td>Calendar Package APM callbacks library Procedures that deal with installing, instantiating, mounting. </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/procs-file-view?version_id=100649&amp;path=packages/calendar/tcl/cal-item-procs.tcl">tcl/cal-item-procs.tcl</a></b></td><td></td><td>Utility functions for Calendar Applications </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/procs-file-view?version_id=100649&amp;path=packages/calendar/tcl/calendar-callback-procs.tcl">tcl/calendar-callback-procs.tcl</a></b></td><td></td><td>Callbacks for the search package. </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/procs-file-view?version_id=100649&amp;path=packages/calendar/tcl/calendar-compatibility-procs.tcl">tcl/calendar-compatibility-procs.tcl</a></b></td><td></td><td>These procs are there to ensure backwards compatibility for possible API breakages. </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/procs-file-view?version_id=100649&amp;path=packages/calendar/tcl/calendar-install-procs.tcl">tcl/calendar-install-procs.tcl</a></b></td><td></td><td>Calendar install callbacks </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/procs-file-view?version_id=100649&amp;path=packages/calendar/tcl/calendar-outlook-procs.tcl">tcl/calendar-outlook-procs.tcl</a></b></td><td></td><td>Utility functions for syncing Calendar with Outlook taken from SloanSpace v1, hacked for OpenACS by Ben. </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/procs-file-view?version_id=100649&amp;path=packages/calendar/tcl/calendar-procs.tcl">tcl/calendar-procs.tcl</a></b></td><td></td><td>Utility functions for Calendar Applications </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/procs-file-view?version_id=100649&amp;path=packages/calendar/tcl/calendar-sc-procs.tcl">tcl/calendar-sc-procs.tcl</a></b></td><td></td><td>Calendar service contract bindings </td></tr></table>

## Procedures

<table cellpadding="0" cellspacing="0"><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::adjust_date">calendar::adjust_date</a></b></td><td></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::apm::package_after_upgrade">calendar::apm::package_after_upgrade</a></b></td><td></td><td>Upgrade script for the calendar package </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::assign_permissions">calendar::assign_permissions</a></b></td><td></td><td>given a calendar_id, party_id and a permission this proc will assign the permission to the party the legal permissions are public, private, calendar_read, calendar_write, calendar_delete if the revoke is set, then the given permission will be removed for the party </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::attachments_enabled_p">calendar::attachments_enabled_p</a></b></td><td></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::calendar_list">calendar::calendar_list</a></b></td><td></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::create">calendar::create</a></b></td><td></td><td>create a new calendar private_p is default to true since the default calendar is a private calendar </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::delete">calendar::delete</a></b></td><td></td><td>Delete a calendar </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::do_notifications">calendar::do_notifications</a></b></td><td></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::from_sql_datetime">calendar::from_sql_datetime</a></b></td><td></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::get">calendar::get</a></b></td><td></td><td>Get calendar info </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::get_item_types">calendar::get_item_types</a></b></td><td></td><td>return the item types </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::get_month_multirow_information">calendar::get_month_multirow_information</a></b></td><td></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::have_private_p">calendar::have_private_p</a></b></td><td></td><td>check to see if ther user have a private calendar if -return_id is 1, then proc will return the calendar_id </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::item::add_recurrence">calendar::item::add_recurrence</a></b></td><td></td><td>Adds a recurrence for a calendar item </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::item::assign_permission">calendar::item::assign_permission</a></b></td><td></td><td>update the permission of the specific cal_item if revoke is set to revoke, then we revoke all permissions </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::item::delete">calendar::item::delete</a></b></td><td></td><td>Delete the calendar item </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::item::delete_recurrence">calendar::item::delete_recurrence</a></b></td><td></td><td>delete a recurrence </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::item::edit">calendar::item::edit</a></b></td><td></td><td>Edit the item </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::item::edit_recurrence">calendar::item::edit_recurrence</a></b></td><td></td><td>edit a recurrence </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::item::get">calendar::item::get</a></b></td><td></td><td>Get the data for a calendar item </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::item::new">calendar::item::new</a></b></td><td></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::item_type_delete">calendar::item_type_delete</a></b></td><td></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::item_type_new">calendar::item_type_new</a></b></td><td></td><td>creates a new item type </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::make_datetime">calendar::make_datetime</a></b></td><td></td><td>given a date, and a time, construct the proper date string to be imported into oracle. </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::name">calendar::name</a></b></td><td></td><td>Return a calendar&#39;s name </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::new">calendar::new</a></b></td><td></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::notification::get_url">calendar::notification::get_url</a></b></td><td></td><td>Returns a full URL to the object_id </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::outlook::cal_outlook_gmt_sql">calendar::outlook::cal_outlook_gmt_sql</a></b></td><td></td><td>formats the hours to substract or add to make the date_time be in gmt </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::outlook::format_item">calendar::outlook::format_item</a></b></td><td></td><td>the cal_item_id is obvious. </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::outlook::ics_timestamp_format">calendar::outlook::ics_timestamp_format</a></b></td><td></td><td>the timestamp must be in the format YYYY-MM-DD HH24:MI:SS </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::personal_p">calendar::personal_p</a></b></td><td></td><td>Returns true (1) if this is the user&#39;s personal calendar, false (0) otherwise. </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::rename">calendar::rename</a></b></td><td></td><td>rename a calendar </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar::to_sql_datetime">calendar::to_sql_datetime</a></b></td><td></td><td>This takes two date chunks, one for date one for time, and combines them correctly. </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar_assign_permissions">calendar_assign_permissions</a></b></td><td></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar_create">calendar_create</a></b></td><td></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar_have_private_p">calendar_have_private_p</a></b></td><td></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar_item_add_recurrence">calendar_item_add_recurrence</a></b></td><td></td><td>Adds a recurrence for a calendar item </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=calendar_make_datetime">calendar_make_datetime</a></b></td><td></td><td>given a date, and a time, construct the proper date string to be imported into oracle. </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=callback::merge::MergePackageUser::impl::calendar">callback::merge::MergePackageUser::impl::calendar</a></b></td><td></td><td>Merge the calendars of two users. </td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/proc-view?version_id=100649&amp;proc=callback::merge::MergeShowUserInfo::impl::calendar">callback::merge::MergeShowUserInfo::impl::calendar</a></b></td><td></td><td>Shows the calendar tables user info </td></tr></table>

## SQL Files

<table cellpadding="0" cellspacing="0"><tr valign="top"><td><b><a href="http://www.project-open.net/api-doc/display-sql?package_key=calendar&amp;url=postgresql/cal-item-create.sql&amp;version_id=100649">sql/postgresql/cal-item-create.sql</a></b></td><td></td><td></td></tr><tr valign="top"><td><b><a href="http://www.project-open.net/api-doc/display-sql?package_key=calendar&amp;url=postgresql/cal-item-drop.sql&amp;version_id=100649">sql/postgresql/cal-item-drop.sql</a></b></td><td></td><td></td></tr><tr valign="top"><td><b><a href="http://www.project-open.net/api-doc/display-sql?package_key=calendar&amp;url=postgresql/cal-table-create.sql&amp;version_id=100649">sql/postgresql/cal-table-create.sql</a></b></td><td></td><td></td></tr><tr valign="top"><td><b><a href="http://www.project-open.net/api-doc/display-sql?package_key=calendar&amp;url=postgresql/cal-table-drop.sql&amp;version_id=100649">sql/postgresql/cal-table-drop.sql</a></b></td><td></td><td></td></tr><tr valign="top"><td><b><a href="http://www.project-open.net/api-doc/display-sql?package_key=calendar&amp;url=postgresql/calendar-create.sql&amp;version_id=100649">sql/postgresql/calendar-create.sql</a></b></td><td></td><td></td></tr><tr valign="top"><td><b><a href="http://www.project-open.net/api-doc/display-sql?package_key=calendar&amp;url=postgresql/calendar-drop.sql&amp;version_id=100649">sql/postgresql/calendar-drop.sql</a></b></td><td></td><td></td></tr><tr valign="top"><td><b><a href="http://www.project-open.net/api-doc/display-sql?package_key=calendar&amp;url=postgresql/calendar-notifications-init.sql&amp;version_id=100649">sql/postgresql/calendar-notifications-init.sql</a></b></td><td></td><td></td></tr><tr valign="top"><td><b><a href="http://www.project-open.net/api-doc/display-sql?package_key=calendar&amp;url=postgresql/upgrade/upgrade-2.0d1-2.0b2.sql&amp;version_id=100649">sql/postgresql/upgrade/upgrade-2.0d1-2.0b2.sql</a></b></td><td></td><td></td></tr><tr valign="top"><td><b><a href="http://www.project-open.net/api-doc/display-sql?package_key=calendar&amp;url=postgresql/upgrade/upgrade-2.1.0b4-2.1.0b5.sql&amp;version_id=100649">sql/postgresql/upgrade/upgrade-2.1.0b4-2.1.0b5.sql</a></b></td><td></td><td></td></tr><tr valign="top"><td><b><a href="http://www.project-open.net/api-doc/display-sql?package_key=calendar&amp;url=postgresql/upgrade/upgrade-2.6.1d2-2.6.1d3.sql&amp;version_id=100649">sql/postgresql/upgrade/upgrade-2.6.1d2-2.6.1d3.sql</a></b></td><td></td><td></td></tr></table>

## Content Pages

<table cellpadding="0" cellspacing="0"><tr valign="top"><td><b>www/</b></td></tr><tr valign="top"><td><b>admin/</b></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/admin/calendar-create.tcl">calendar-create.tcl</a></b></td><td>generation of new group calendar when a party_wide calendar is generated the default permission is that this calendar is</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/admin/calendar-delete.tcl">calendar-delete.tcl</a></b></td><td>Delete calendar</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/admin/calendar-edit.adp">calendar-edit.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/admin/calendar-edit.tcl">calendar-edit.tcl</a></b></td><td>Add/Edit calendar</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/admin/index.adp">index.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/admin/index.tcl">index.tcl</a></b></td><td>Main Calendar Admin Page.</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/admin/permissions-user-add.adp">permissions-user-add.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/admin/permissions-user-add.tcl">permissions-user-add.tcl</a></b></td><td>Redirect page for adding users to the permissions list.</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/admin/permissions.adp">permissions.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/admin/permissions.tcl">permissions.tcl</a></b></td><td>Permissions for the subsite itself.</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/cal-item-create-recurrence.adp">cal-item-create-recurrence.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/cal-item-create-recurrence.tcl">cal-item-create-recurrence.tcl</a></b></td><td>Creation of new recurrence for cal item</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/cal-item-delete-all-occurrences.tcl">cal-item-delete-all-occurrences.tcl</a></b></td><td>delete all occurences of a recurring item</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/cal-item-delete-confirm.adp">cal-item-delete-confirm.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/cal-item-delete-confirm.tcl">cal-item-delete-confirm.tcl</a></b></td><td>Confirm Deletion</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/cal-item-delete.tcl">cal-item-delete.tcl</a></b></td><td>Delete a calendar item</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/cal-item-new.adp">cal-item-new.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/cal-item-new.tcl">cal-item-new.tcl</a></b></td><td>Creating a new Calendar Item</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/cal-item-outlook.tcl">cal-item-outlook.tcl</a></b></td><td>Output an item as ics for Outlook</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/cal-item-view.adp">cal-item-view.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/cal-item-view.tcl">cal-item-view.tcl</a></b></td><td>View one event</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/cal-nav.adp">cal-nav.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/cal-nav.tcl">cal-nav.tcl</a></b></td><td>Nav page</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/cal-options.adp">cal-options.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/cal-options.tcl">cal-options.tcl</a></b></td><td>List all the calendars for which the user has the read privilege.</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/calendar-item-types.adp">calendar-item-types.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/calendar-item-types.tcl">calendar-item-types.tcl</a></b></td><td>Manage the calendar item types</td></tr><tr valign="top"><td><b>ics/</b></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/ics/index.vuh">index.vuh</a></b></td><td>Output an item as ics for Outlook The expected URL is &lt;cal_item_id&gt;.ics</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/index.tcl">index.tcl</a></b></td><td>Main Calendar Page totally redone by Ben</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/item-type-delete.tcl">item-type-delete.tcl</a></b></td><td>Delete an item type</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/item-type-new.tcl">item-type-new.tcl</a></b></td><td>Add an item type</td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/mini-calendar.adp">mini-calendar.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/mini-calendar.tcl">mini-calendar.tcl</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/navbar.adp">navbar.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/navbar.tcl">navbar.tcl</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/view-list-display.adp">view-list-display.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/view-list-display.tcl">view-list-display.tcl</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/view-month-display.adp">view-month-display.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/view-month-display.tcl">view-month-display.tcl</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/view-one-day-display.adp">view-one-day-display.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/view-one-day-display.tcl">view-one-day-display.tcl</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/view-print-display.adp">view-print-display.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/view-week-display.adp">view-week-display.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/view-week-display.tcl">view-week-display.tcl</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/view.adp">view.adp</a></b></td><td></td></tr><tr valign="top"><td style="width:35%"><b><a href="http://www.project-open.net/api-doc/content-page-view?version_id=100649&amp;path=packages/calendar/www/view.tcl">view.tcl</a></b></td><td>Viewing Calendar Information.</td></tr></table>
