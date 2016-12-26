---
lang: en
layout: article_with_sidebar
updated_at: '2016-12-22 13:54 +0400'
identifier: ref_9raTXZPN
title: ''
order: 100
published: false
---
## Introduction

This article gives general information on X-Cart 5 upgrades and provides hints about what to do if an upgrade fails in the middle of the process.

## Table of Contents

*   [Introduction](#introduction)
*   [Table of Contents](#table-of-contents)
*   [General information](#general-information)
*   [Process of store upgrade](#process-of-store-upgrade)
*   [Manual upgrade](#manual-upgrade)

## Upgrade types

Since the adoption by X-Cart of the [four-sequence versioning scheme](http://devs.x-cart.com/en/misc/x-cart_versions.html#x-cart-53x-versioning), in which the first two sequences of digits in the version identifier represent the major version, the third sequence - the minor version, and the fourth sequence - the build version (bugfix release), we had to change X-Cart's upgrade system a little bit to accomodate the changes. As a result, X-Cart now uses two types of upgrades:

* **major upgrade** - an upgrade resulting in the increase of the first three sequences of digits in the version number (for example, an upgrade from 5.0.13 to 5.1.3, or from 5.2.16 to 5.2.20, or from 5.3.1.6 to 5.3.2.0);

* **minor update** - an update resulting in the increase of the build version number (for example, an update involving the change of the version number from 5.3.1.3 to 5.3.1.6).

The type of upgrade reflects the significance of changes that the upgrade implements. A major upgrade provides both new features and bugfixes. A minor update provide only bugfixes. The new features implemented by a major upgrade rely on major changes of the core, which means that the interfaces of classes and the signatures of methods change. It does not happen during a minor update. Consequently, a minor update does not require any change in the modules, whereas a major upgrade does require module compatibility changes.

<table class="ui celled padded compact small table">
  <thead>
  	<tr>
      <th><strong>4th digit increases<br/>5.3.0.3 to 5.3.0.5</strong></th>
      <th><strong>3d digit increases<br/>5.3.0.3 to 5.3.1.0</strong></th>
      <th><strong>2nd digit increases<br/>5.3.0.3 to 5.4.0.0</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Bugfixes only</td>
      <td>Bugfixes<br/>New features<br/>Minor API changes</td>
      <td>Bugfixes<br/>New features<br/>Minor API changes</td>
    </tr>
    <tr>
      <td>Free anytime</td>
      <td>Free with active<br/>upgrade subscription</td>
      <td>Free with active<br/>upgrade subscription</td>
    </tr>
  </tbody>
</table>

If a major upgrade and a minor update are available to a store at the same time, the store administrator can choose which one they want to apply. A minor update will mean an update to get all the fixes of the latest available bugfix release within the store's version branch. A major upgrade will mean an upgrade to the latest version with all the new features and bugfixes available with the store's license.  

## Upgrade waves
Every X-Cart version undergoes thorough testing before it is released. To 

## Availability of upgrades for different versions
A major upgrade involving the change of the second sequence in the version number can be done only from the latest version of the branch. In other words, if the 5.0.x branch consists of the versions 5.0.10, 5.0.11, 5.0.12, 5.0.13, 5.0.14, then the only version number from which you can upgrade to 5.1 is 5.0.14. Major upgrades involving the change of the third sequence in the version number do not follow this requirement, which means you can upgrade a 5.0.10 store to 5.0.14 in one run. To upgrade a store from 5.0.10 to 5.1.0, a two-step upgrade will be required: first, an upgrade from 5.0.10 to 5.0.14, and then an upgrade from 5.0.14 to 5.1.0.

## Upgrade hooks
The general idea of any upgrade/update is to overwrite the existing files of the core/module. That simple. However, sometimes X-Cart needs to synchronize data or do some utility work. Such work is done by **upgrade hooks**. There are three types of upgrade hooks:

*   **pre-upgrade hooks** are run before the files have been overwritten. These hooks work using the code of the old core.
*   **post-upgrade hooks** are run after the files have been overwritten, but before the cache rebuild process has started. They are used for the preparation of the store for the cache rebuild process. They work using the code of the old core.
*   **post-rebuild hooks** are run after the very first cache rebuild process has finished. They work using the code of the new core.

Upgrade hooks of the core are located in the `<X-Cart 5>/upgrade/` folder. If you want to find upgrade hooks for version 5.1.3, then you should go to the `<X-Cart 5>/upgrade/5.1/3/` directory. There you can find three types of files:

*   **pre_upgrade.php** contains pre-upgrade hooks;
*   **post_upgrade.php **contains post-upgrade hooks;
*   **post_rebuild.php** contains post-rebuild hooks.

Upgrade hooks may exist in the modules as well, if the module needs to synchronize data between its own versions. Module upgrade hooks can be found in the `<X-Cart 5>/classes/Module/<DEV-ID>/<MODULE-ID>/upgrade/` folders; for example `<X-Cart 5>/classes/XLite/Module/XC/ProductComparison/upgrade/`.

## Store upgrade process
Once per day, each store checks the marketplace for updates. The response from marketplace is cached for a day. If you need to delete this cache, you should open the `admin.php?target=addons_list_marketplace&action=clear_cache` link.

If there is any kind of update available, the merchant will see the **Updates are available** link in the header of admin area.
![]({{site.baseurl}}/attachments/7505469/7602688.png)

Click this link and proceed to upgrade. You can see possible warnings before upgrade.

*   If your store does not have any license (free or paid), you will be prompted to buy one

![]({{site.baseurl}}/attachments/7505469/7602689.png)

*   If your store has modules that do not exist in the marketplace (e.g. you uploaded them via **Upload add-on** button) and you are doing a **minor upgrade, **you will be advised to disable them, although it is not necessary![]({{site.baseurl}}/attachments/7505469/7602690.png)
*   If your store has modules that do not exist in the marketplace (e.g. you uploaded them via **Upload add-on** button) and you are doing a **major upgrade,** you will be told that **they ****will be disabled automatically**![]({{site.baseurl}}/attachments/7505469/7602691.png)

After clicking **Continue **button, X-Cart will start downloading upgrade packs for core and modules.

NOTE: if this step times out because of bad connection, you can try to adjust the REQUEST_LONG_TTL constant in the `<X-Cart 5>/var/run/classes/XLite/Core/Marketplace.php` script, so that X-Cart would be able to download all the files in time.

Once all the upgrade packs have been downloaded, you will be prompted to create a backup, and there will be the **Install updates** button. Clicking it will run the upgrade process (which cannot be interrupted).

![]({{site.baseurl}}/attachments/7505469/7602771.png)

At this last step, you can also receive several types of warnings:

*   If your store has any modified files, you will get a warning like this

![]({{site.baseurl}}/attachments/7505469/7602770.png)

*   If your store has any modules that have upgrade hooks and these modules are disabled (not active), you will be prompted to either activate such modules or completely remove them. A module must be active in order to correctly run the upgrade hooks, and this is the reason why the module must be either enabled or deleted
    ![]({{site.baseurl}}/attachments/7505469/7602769.png)

After the **Install updates** button has been clicked, the process will continue as follows:

1.  Pre-upgrade hooks are run. If there is upgrade from 5.0.14 to 5.1.3, then all the upgrade hooks - 5.1.0, 5.1.1, 5.1.2, 5.1.3 - will be run during this step. In addition to that, all the modules' upgrade hooks will be run at this stage;
2.  Overwriting of files happens: new files are added, existing ones are overwritten, non-existent ones in new version are deleted;
3.  Post-upgrade hooks are run. The same process as with pre-upgrade hooks;
4.  Cache rebuild process;
5.  Post-rebuild hooks are run. The same process as with pre-upgrade and post-upgrade hooks;
6.  Update of language variables happens. Script will take all install.yaml files of modules + yaml file with language variables of the core (`<X-Cart 5>/sql/install.yaml`) and put the language variables from these files to the database;
7.  Upgrade is finished.

## Manual upgrade

We do our best to provide smooth minor and major upgrade capabilities, but sometimes something goes wrong and you need to deal with it. If an upgrade was interrupted, you can continue it manually.

First thing to do is to find out what step your upgrade stopped at. Look at the bottom of the `<X-Cart 5>/var/log/upgrade.log` file. It will show you what upgrade hooks were run and what files were overwritten. If not all the post-rebuild hooks were run, it means that the upgrade process broke during the 5th step. If not all the files were overwritten, then the process stopped at the 2nd step. You need to locate the problem step, re-do this step manually, and then run all the following steps manually.

Below we have provided a description of a full manual upgrade:

1.  How to get new files? First of all, check the folder `<X-Cart 5>/var/tmp`, and all the new files should be there. If this folder is empty, you should install the X-Cart 5 version you are upgrading to on the same server (you can freely get it on [http://www.x-cart.com)](http://www.x-cart.com)) and activate all the paid add-ons using your license keys. After that, this installation will have all the needed files.
2.  You need to run all the pre-upgrade hooks (core's and modules'). The code example of how to run one hook is below: 

    ```php
    <?php
    require_once (dirname(__FILE__) . DIRECTORY_SEPARATOR . 'top.inc.php');

    $func = include 'upgrade/5.1/0/pre_upgrade.php';
    $func();

    ?>
    ```

3.  Overwrite all the files manually. You can put the files from the new version distribution pack to your store's folder.

4.  Run all the post-upgrade hooks. The code should be the same as the code you used at step 2, but it should point to the post-upgrade hooks file.

5.  Rebuild cache.

6.  Run all the post-rebuild hooks using the same code mentioned for steps 2 and 4.

7.  Run the hooks for updating language variables. The code example for one hook is below: 

    ```php
    <?php
        require_once (dirname(__FILE__) . DIRECTORY_SEPARATOR . 'top.inc.php');

    	// core yaml file
        $yamlFile = dirname(__FILE__) . DIRECTORY_SEPARATOR . 'sql' . DIRECTORY_SEPARATOR . 'xlite_data.yaml';
        \XLite\Core\Translation::getInstance()->loadLabelsFromYaml($yamlFile);

    	// module yaml file (example of one yaml file, you need to run all of them)
    	$yamlFile = dirname(__FILE__) . DIRECTORY_SEPARATOR . 'classes' . DIRECTORY_SEPARATOR . 'XLite' . DIRECTORY_SEPARATOR . 'Module' . DIRECTORY_SEPARATOR . 'XC' . DIRECTORY_SEPARATOR . 'ProductComparison' . DIRECTORY_SEPARATOR . 'install.yaml';
        \XLite\Core\Translation::getInstance()->loadLabelsFromYaml($yamlFile);

        \XLite\Core\Translation::getInstance()->reset();
    ?>
    ```

This completes the upgrade process.


_Related pages:_

*   [X-Cart Upgrade General Steps](http://devs.x-cart.com/en/misc/x-cart_upgrade_general_steps.html)
*   [Upgrade hooks](http://devs.x-cart.com/en/misc/upgrade_hooks.html)
