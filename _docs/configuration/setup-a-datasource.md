---
layout: default
title: Setup Data Source
nav_order: 6
parent: Configuration
---
{% if site.manage_conn_string %}
{{ site.app_name }} needs to know how to connect to your database. The first time you run it, no data sources have been set up, so you are prompted to go to the Setup Wizard.

![](/assets/images/connstrings.png)

Click ![](/assets/images/addround.png) to add a data source. Enter a friendly name (the name you want displayed in {{ site.app_name }}) and choose the provider type from the drop-down list. The choices are:

* *System.Data.Odbc*: use this for an ODBC connection.
* *System.Data.OleDb*: use this for an OLE DB connection.
* *System.Data.SqlClient*: use this if you are connecting to Microsoft SQL Server.
* *MySql.Data.MySqlClient*: use this if you are connecting to MySQL.

Enter the connection string to connect to the database:

* For System.Data.Odbc, the connection string is typically something like "driver=*ODBC driver name*;server=*server name*;database=*database name*;uid=*user name*;pwd=*password*."

* For System.Data.OleDb, the connection string is typically something like "provider=*OLE DB provider name*;Data Source=*server name*;Initial Catalog=*database name*;User ID=*user name*;Password=*password*."

* For System.Data.SqlClient, the connection string is typically something like "Server=*server name*;Database=*database name*;User ID=*user name*;Password=*password*."

See <a href="http://www.connectionstrings.com" target="top">www.connectionstrings.com</a> for connection strings for different ODBC drivers and OLE DB providers.

> @icon-info-circle The connection string is encrypted when it's stored in {{ site.app_name }}'s system files, so you don't have to worry about compromising your settings.
{% else %}
{{ site.app_name }} connects to your database using an ODBC data source name (DSN). ODBC, or Open DataBase Connectivity, is a database access technology built into Windows that provides a consistent way of accessing data from different database engines. Using ODBC means {{ site.app_name }} doesn't have to know details such as where the server is located, which database to access, etc.; this information is defined in an ODBC data source your system administrator sets up. The first time you run it, no DSNs have been set up in {{ site.app_name }}, so you are prompted to go to the Setup Wizard.

![](/assets/images/datasources.png)

Click ![](/assets/images/addround.png) to add a data source. Enter a friendly name (the name you want displayed in {{ site.app_name }}) and choose the desired DSN from the drop-down list. {{ site.app_name }} needs the user name and password to access this database (this is the database user name and password, not your Windows or other application user name and password), so enter those in the text boxes provided.

> @icon-info-circle The password is encrypted when it's stored in {{ site.app_name }}'s system files, so you don't have to worry about compromising your password.

> @icon-info-circle If you are accessing the IBM iSeries Db2 ODBC driver, be sure to configure your DSN to convert binary data to text on the Translation page of the ODBC setup dialog.
{% endif %}

Click the Test button to make sure the settings are correct; you will see a message that the test succeeded or failed. Once it succeeds, click ![](/assets/images/savestyles.png) to save the data source. Click ![](/assets/images/deleteicon.png) to remove the data source. You can add as many data sources as you wish. Click Finish to exit the Setup Wizard.

You can add additional data sources by choosing Setup Wizard from the Tools menu. Note that this is only available to users in the Administrator role.