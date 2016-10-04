---
lang: en
layout: article_with_sidebar
updated_at: '2016-10-04 11:47 +0400'
identifier: ref_Ah935naM
title: Using the module "XC4 to XC5 Migration wizard"
order: 130
published: true
version: X-Cart 5.3.1 and later
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

3.  At the second step of the wizard ("2. Connect"), specify your X-Cart 4 store database connection details. 

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

    That will take you to the next step of the wizard - "3. Check".

4.  Using the connection details provided at the previous step, your X-Cart 5 store tries to connect to the specified X-Cart 4 database. Provided that the connection details have been specified correctly, at the third step of the wizard ("3. Check") you should be able to see a summary of information that X-Cart 5 could obtain regarding your X-Cart 4 store:
     ![xc5_migration_wizard_check1.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_check1.png?effects=drop-shadow)

    Click **Continue** to proceed.
    ![xc5_migration_wizard_check2.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_check2.png?effects=drop-shadow)

    
5.  At the fourth step of the wizard ("4. Select"), you will see a list of data types that can be migrated from your X-Cart 4 store to X-Cart 5, with check boxes:
    ![xc5_migration_wizard_select1.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_select1.png?effects=drop-shadow)

    Use the check boxes to select the data types that you want to be moved to X-Cart 5, then click **Save and continue**:
    ![xc5_migration_wizard_select2.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_select2.png?effects=drop-shadow)

6.  If the module detects that your X-Cart 4 installation has features that are lacking in X-Cart 5 default distribution pack, but can be implemented by enabling certain X-Cart 5 add-on modules, at the next step of the wizard ("5. Enable"), it will provide you with a list of X-Cart 5 modules that you should enable so you can have the same features as in your X-Cart 4 store:
    ![xc5_migration_wizard_enable1.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_enable1.png?effects=drop-shadow)

    Click **Enable and continue**:
    ![xc5_migration_wizard_enable2.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_enable2.png?effects=drop-shadow)

    The process of module activation will be started:
    ![xc5_migration_wizard_enable3.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_enable3.png?effects=drop-shadow)

    Note that not all of the activated modules may be free. If any paid modules are installed and activated at this step, you will get a license warning like the following:
    ![xc5_migration_wizard_enable4.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_enable4.png?effects=drop-shadow)

    The warning means that you have two options available to you:
    *   Purchase licenses for the installed paid modules and activate your license keys;
    *   Remove the installed modules from your store.

    On our demo, we chose to activate a license key for X-Cart Ultimate. After activating the key, we got a message at the top of the screen showing that the key has been activated successfully:
    ![xc5_migration_wizard_enable5.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_enable5.png?effects=drop-shadow)
    
    This means the problem with our module licenses has been resolved, and we can go back to our migration wizard:
    ![xc5_migration_wizard_enable6.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_enable6.png?effects=drop-shadow)
   
7.  By the next step ("5. Transfer"), the wizard has collected all the information it requires and is ready to start the data migration process. You can see a list of X-Cart entities that will be transfered from your X-Cart 4 store to the X-Cart 5 platform:
    ![xc5_migration_wizard_transfer1.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_transfer1.png?effects=drop-shadow)
    
    Click **Start migration**.
    ![xc5_migration_wizard_transfer2.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_transfer2.png?effects=drop-shadow)
    
    The migration process begins:
    ![xc5_migration_wizard_transfer3.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_transfer3.png?effects=drop-shadow)

    Note that the migration process, which may take a while to complete, only continues while the page is open. 
    ![xc5_migration_wizard_transfer4.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_transfer4.png?effects=drop-shadow)

    So be sure to keep the page open or, if you have to close it for a while, be sure to re-open it to allow the migration module to finish its work.
    
    While your data is being migrated from your X-Cart 4 store to X-Cart 5, you will be able to see the progress on the screen. Here are the stages that will have to be completed:
    
    *   Processing products: 
    ![xc5_migration_wizard_transfer5.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_transfer5.png?effects=drop-shadow)
    
    *   Removing duplicate images:    
    ![xc5_migration_wizard_transfer6.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_transfer6.png?effects=drop-shadow)

    *   Resizing images:    
    ![xc5_migration_wizard_transfer7.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_transfer7.png?effects=drop-shadow)

8. Once the transfer has completed, the final step of the wizard will be displayed - "6. Complete":
    ![xc5_migration_wizard_congrats.png]({{site.baseurl}}/attachments/ref_Ah935naM/xc5_migration_wizard_congrats.png?effects=drop-shadow)

That is all; your data has been successfully migrated.



    
