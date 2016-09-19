---
lang: en
layout: article_with_sidebar
updated_at: '2016-09-16 13:20 +0400'
identifier: ref_Ah935naM
title: Using the module "XC4 to XC5 Migration wizard"
order: 130
published: false
version: X-Cart 5.3.0 and later
---
Once the module "XC4 to XC5 Migration wizard" has been installed on your X-Cart 5 store, you get a new item at the top of the Admin area menu - "Migration wizard":

![xc5_migration_wizard_menu_item.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_menu_item.png?effects=drop-shadow)

To use the wizard:

1.  Click on the "Migration wizard" item in the Admin area menu. The wizard will be launched. 
![xc5_migration_wizard_start1.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_start1.png?effects=drop-shadow)

2.  At the first step of the wizard ("1. Start"), select the check box to confirm that you understand the consequences of using the wizard (namely, that any existing data in your X-Cart 5 store will be overwritten as a result of the migration process). Click **Start migration** to proceed:
![xc5_migration_wizard_start2.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_start2.png?effects=drop-shadow)

As a result, the second step of the wizard will be loaded - "2. Connect":
![xc5_migration_wizard_connect1.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_connect1.png?effects=drop-shadow)

3.  At the second step of the wizard ("2. Connect"), specify your X-Cart 4 store database connection details. The standard set of fields to complete is as follows:
    * **Database name**: The name of your X-Cart 4 database.
    * **Database username**: The username of your MySQL account.
    * **Database password**: The password of your MySQL account.
    
    If the standard fields are not enough to provide all the necessary connection details, please use the **Advanced options** section (expands at the click of the respective button): 
![xc5_migration_wizard_connect2.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_connect2.png?effects=drop-shadow)

    The **Advanced options** section allows you to enter the following info:
    * **Host name**: The name of the host where your MySQL server is running.
    * **Port number**: The port number to use for the connection, for connections made using TCP/IP. The default port number is 3306.
    * **Socket**: The MySQL Unix socket.
    * **Table prefix**: The table prefix used in your X-Cart 4 database (as was specified during X-Cart 4 installation). If you do not remember the table prefix that was used for your X-Cart 4 store, you can look it up in the file init.php of your X-Cart 4.x installation (in X-Cart versions 4.5.3 and later, see the value of XC_TBL_PREFIX; in earlier versions - the value of xcart_tbl_prefix). The default table prefix for all X-Cart 4 versions is "xcart_".
    
![xc5_migration_wizard_connect2_1.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_connect2_1.png?effects=drop-shadow)

![xc5_migration_wizard_connect3.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_connect3.png?effects=drop-shadow)
,j
![xc5_migration_wizard_connect4.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_connect4.png?effects=drop-shadow)
kjk
![xc5_migration_wizard_connect5.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_connect5.png?effects=drop-shadow)
