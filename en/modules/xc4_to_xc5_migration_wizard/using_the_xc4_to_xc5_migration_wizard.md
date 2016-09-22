---
lang: en
layout: article_with_sidebar
updated_at: '2016-09-20 21:07 +0400'
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

2.  At the first step of the wizard ("1. Step-Start"), select the check box to confirm that you understand the consequences of using the wizard (namely, that any existing data in your X-Cart 5 store will be overwritten as a result of the migration process). Click **Start migration** to proceed:
![xc5_migration_wizard_start2.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_start2.png?effects=drop-shadow)

    As a result, the second step of the wizard will be loaded - "2. Connect":
![xc5_migration_wizard_connect1.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_connect1.png?effects=drop-shadow)

3.  At the second step of the wizard ("2. Step-Connect"), specify your X-Cart 4 store database connection details. 

    Start by completing the following fields:
    *   **Database name**: The name of your X-Cart 4 database.
    *   **Database username**: The username of your MySQL account.
    *   **Database password**: The password of your MySQL account.
    
    If this set of fields is not enough to provide all the necessary connection details, please use the **Advanced options** section (expands at the click of the respective button): 
![xc5_migration_wizard_connect2.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_connect2.png?effects=drop-shadow)

    In the **Advanced options** section, you can enter the following info:
    *   **Host name**: The name of the host where your MySQL server is running.
    *   **Port number**: The port number to use for the connection, for connections made using TCP/IP. The default port number is 3306.
    *   **Socket**: The MySQL Unix socket.
    *   **Table prefix**: The table prefix used in your X-Cart 4 database (as was specified during X-Cart 4 installation). If you do not remember the table prefix that was used for your X-Cart 4 store, you can look it up in the file init.php of your X-Cart 4.x installation (in X-Cart versions 4.5.3 and later, see the value of `XC_TBL_PREFIX`; in earlier versions - the value of `xcart_tbl_prefix`). The default table prefix for all X-Cart 4 versions is `xcart_`.
    ![xc5_migration_wizard_connect2_1.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_connect2_1.png?effects=drop-shadow)

    After specifying the above details, provide the following settings:
    * Encryption key: Your X-Cart 4 store Blowfish key (the secret key needed for access to certain types of data stored in X-Cart 4 in encrypted form, such as user passwords). For more info on X-Cart 4 Blowfish key, see [X-Cart 4 manual](http://help.x-cart.com/index.php?title=X-Cart:Blowfish#Blowfish_key_based_encryption_method "X-Cart 4 manual").
    * Site URL: The URL of your X-Cart 4 store.
    ![xc5_migration_wizard_connect3.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_connect3.png?effects=drop-shadow)
    
    Click **Save and continue**:
    ![xc5_migration_wizard_connect4.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_connect4.png?effects=drop-shadow)
    
    That will take you to the next step of the wizard - "3. Step-Check".

4.  Using the connection details provided at the previous step, your X-Cart 5 store tries to connect to the specified X-Cart 4 database. Provided that the connection details have been specified correctly, at the third step of the wizard ("3. Step-Check") you should be able to see a summary of information that X-Cart 5 could obtain regarding your X-Cart 4 store:
    ![xc5_migration_wizard_check1.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_check1.png?effects=drop-shadow)
    
    Click **Continue** to proceed.
    ![xc5_migration_wizard_check2.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_check2.png?effects=drop-shadow)

    
5.  At the fourth step of the wizard ("4. Step-Select"), you will see a list of data types that can be migrated from your X-Cart 4 store to X-Cart 5, with check boxes:
    ![xc5_migration_wizard_select1.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_select1.png?effects=drop-shadow)
    
    Use the check boxes to select the data types that you want to be moved to X-Cart 5, then click **Save and continue**:
    ![xc5_migration_wizard_select2.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_select2.png?effects=drop-shadow)
    
6.  If the module detects that your X-Cart 4 installation has features that are lacking in X-Cart 5 default distribution pack, but can be implemented by enabling certain X-Cart 5 add-on modules, at the next step of the wizard ("5. Step-Enable"), it will provide you with a list of X-Cart 5 modules that you should enable so you can have the same features as in your X-Cart 4 store:
    ![xc5_migration_wizard_enable1.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_enable1.png?effects=drop-shadow)
    
    Click **Enable and continue**:
    ![xc5_migration_wizard_enable2.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_enable2.png?effects=drop-shadow)

    The modules will be enabled:
    ![xc5_migration_wizard_enable3.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_enable3.png?effects=drop-shadow)

7.  At the next step ("6. Step-Transfer"),   

    ![xc5_migration_wizard_transfer1.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_transfer1.png?effects=drop-shadow)
    
    jk
    ![xc5_migration_wizard_transfer2.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_transfer2.png?effects=drop-shadow)
    
    jjjnn
    ![xc5_migration_wizard_transfer3.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_transfer3.png?effects=drop-shadow)






