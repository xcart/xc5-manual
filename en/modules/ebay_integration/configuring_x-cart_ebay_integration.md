---
lang: en
layout: article_with_sidebar
updated_at: '2017-10-13 16:27 +0400'
identifier: ref_SCbAqGqX
title: Configuring X-Cart eBay Integration
categories:
  - User manual
published: true
order: 120
---

To connect your X-Cart store to eBay, you need to set up one or more eBay configurations via the eBay configurations section in your X-Cart store's Admin area. You can access this section one of the following methods:
   
   * by clicking the **eBay configurations** menu item under **Sales channels** in the Admin menu:
     ![xc5_ebay_ebay_confs_link.png]({{site.baseurl}}/attachments/ref_SCbAqGqX/xc5_ebay_ebay_confs_link.png)
     
   * by going to the eBay Integration addon setting from the **Installed Addons** section:
     ![xc5_ebay_settings_link.png]({{site.baseurl}}/attachments/ref_SCbAqGqX/xc5_ebay_settings_link.png)


You will need to add and set up a separate eBay configuration for each eBay marketplace site to which you would like to connect. This includes the following steps:

1.  [Add the eBay configuration you require](#add_the_eBay_configuration_you_require);
2.  [Obtain your eBay user token](#obtaining-your-ebay-user-token);
3.  [Set your business policies](#setting-your-business-policies);
4.  [Choose your default eBay categories](#choosing-your-default-ebay-categories);
5.  [Configure the General settings for the X-Cart eBay Integration addon](#configuring-the-general-settings-for-the-x-cart-ebay-integration-addon);
6.  (Optional) [Configure eBay options for products and categories](#configuring-ebay-options-for-products-and-categories).

Let's look at each of the steps more closely.

## Add the eBay configuration you require

To connect your X-Cart store to a specific eBay marketplace site, you will need to add a new eBay configuration:

1. In your X-Cart store's Admin area, go to the eBay configurations section (**Sales channels**>**eBay configurations**).
   ![xc5_ebay_configurations_tab.png]({{site.baseurl}}/attachments/ref_ZnP9TFJx/xc5_ebay_configurations_tab.png)

2. From the **eBay Site** box, select the eBay marketplace site to which you need to connect. The products and orders in your X-Cart store will be synchronized with this eBay site. 
   
3. Click the **Create configuration** button.
   ![xc5_ebay_create_configuration.png]({{site.baseurl}}/attachments/ref_ZnP9TFJx/xc5_ebay_create_configuration.png)

The eBay configuration will be created. On the page that opens, the configuration name and a link to the respective eBay marketplace site will be displayed. You will also be provided with some tools to set the operation mode (Test/Live) and to get the Auth Token for this eBay configuration:
   ![xc5_ebay_configurations_tab1.png]({{site.baseurl}}/attachments/ref_ZnP9TFJx/xc5_ebay_configurations_tab1.png)


## Obtaining an eBay user token

Once a new eBay configuration has been added via the eBay configurations section of your X-Cart store's Admin area, you need to is create a new user [token](http://developer.ebay.com/devzone/guides/ebayfeatures/Basics/Tokens-About.html) for it (also known as "Auth Token). The token is needed so the eBay Integration in your X-Cart store can connect to your eBay account. To create a new user token for an eBay configuration:

1.  If you haven't yet done so, add a new eBay configuration via the eBay configurations section of your X-Cart store's Admin area (**Sales channels**>**eBay configurations**) as described above (See [Add the eBay configuration you require](#add_the_eBay_configuration_you_require)): 
    ![xc5_ebay_configurations_tab1.png]({{site.baseurl}}/attachments/ref_ZnP9TFJx/xc5_ebay_configurations_tab1.png)
    or open the details of a previously added eBay configuration for which you need to set a new token at the **Get User Token** tab:
    ![xc5_ebay_get_token_tab.png]({{site.baseurl}}/attachments/ref_ZnP9TFJx/xc5_ebay_get_token_tab.png)

2.  Adjust the following settings:
    *   **eBay Site**: Select the eBay site where you will be selling your products. The products and orders in your X-Cart store will be synchronized with this eBay site. 
    *   **Select mode**: Specify the mode in which your store will be interacting with eBay: select _Test_ to use the eBay Sandbox or _Live_ to use the production environment.

3.  Click the **Create new token** button:
    ![]({{site.baseurl}}/attachments/9306381/9438473.png)
    This launches the user sign-in and consent process: you will be redirected to the eBay site where you will need to log in to the eBay account for which you need the token and grant the application the permission to access your account on your behalf:
    ![]({{site.baseurl}}/attachments/9306381/9438474.png)

    After signing in, provide your consent to share your eBay data by clicking "**I agree**":
    ![]({{site.baseurl}}/attachments/9306381/9438475.png)
    **Important**: If you are creating a Sandbox user token, enter the credentials for a [Sandbox User](https://developer.ebay.com/DevZone/sandboxuser/default.aspx). If it is a token for Production, use the credentials for a user created on the [Production eBay site](http://www.ebay.com/) (the one you will use to sell items on eBay). Remember that User IDs for Sandbox users begin with "`TESTUSER_`".
    Once application access has been granted, eBay will generate a new token, and you will be automatically redirected back to X-Cart. On the **Get User Token** screen, you should now be able to see the **User Token** field populated with your token value. Below this field you should be able to see information about the current status of your token (**Token Status**) and token expiration date (**Token Expiration**):
    ![]({{site.baseurl}}/attachments/9306381/9438476.png)
    When your token is about to expire, you will be notified and provided with a button to create a new one.
4.  Now that your token has been generated, click **Next** to save your changes and head over to the next step of configuring your eBay Integration: [Setting your business policies](#setting-your-business-policies).
    ![]({{site.baseurl}}/attachments/9306381/9438477.png)

## Setting your business policies

Once you have created an eBay user token to connect your X-Cart store to your eBay seller account, you can set business policies for your eBay listings. Business policies typically include information on how buyers can pay you; the shipping services you offer, and shipping costs; whether you accept returns, any return conditions, etc. All eBay listings must include this information. To provide information on your business policies for the listings that will be created from the products you sell via your X-Cart store, follow the steps below:

1.  If you haven't yet done so, configure your business policies in your eBay account (More information is available [here](http://pages.ebay.com/help/sell/business-policies.html)). 
2.  In X-Cart Admin, after creating your eBay token in the **Get User Token** section of the eBay Configuration page (**Settings** > **eBay Configuration**), click **Next** to go to the **Business policies** section:
    ![]({{site.baseurl}}/attachments/9306381/9438477.png)
    If you have configured your business policies earlier, it is possible to simply click the **Business policies** tab:
    ![]({{site.baseurl}}/attachments/9306381/9438479.png)
3.  Use the drop-down policy selectors to set the business policies you would like to use for your eBay listings:
    *   **Return Policy**;
    *   **Payment Policy**; 
    *   **Shipping Policy**. ![]({{site.baseurl}}/attachments/9306381/9438481.png)
    The names of business policies displayed to you on this page are pulled from your eBay account to which you have linked your application at the [previous step](#obtaining-your-ebay-user-token). If you do not see the policy you require in any of the selectors, it may be due to the fact that the policy was added after the information on the policies had been pulled into X-Cart. To resolve the problem, click the **Refresh Business Policies** button - the list of policies will be updated.
    ![]({{site.baseurl}}/attachments/9306381/9438482.png)
4.  Use the **PayPal email address** field to enter your valid PayPal email address. eBay will use this address to identify the correct PayPal account when the buyer pays you via PayPal.
5.  Click **Next** to save your changes and head over to the next step of configuring your eBay Integration: [Choose your default eBay categories](#choosing-your-default-ebay-categories).
    ![]({{site.baseurl}}/attachments/9306381/9438484.png)

## Choosing your default eBay categories

Every product you export to eBay has to be placed in at least one of eBay categories. When using eBay Integration, the eBay categories to which your products will be exported need to be set before the export actually takes place. The **Categories** section of the eBay Configuration page in X-Cart allows you to set the default eBay categories for your listings: one main and one additional category. The main category is required, the additional one is optional. The categories you specify here will be your store's default eBay categories - the ones that will be used for any products for which eBay categories are not set at the product or category level. 

To set your store's default eBay categories:

1.  In X-Cart Admin, in the **Business Policies **section of the eBay Configuration page (**Settings** > **eBay Configuration**), click **Next** to go to the **Categories** section:
    ![]({{site.baseurl}}/attachments/9306381/9438484.png)
    If you have configured your default eBay categories previously, you can simply click the **Categories** tab:
    ![]({{site.baseurl}}/attachments/9306381/9438485.png)

2.  Set the default _main_ category for your products:
    Use the **Main eBay Category** selector to select the eBay category that best describes the products you are going to sell on eBay. If not all your products are going to be in the same category, just select the category you intend to use for the majority of your eBay listings; for the products that do not fit well into the eBay category selected here, you will be able to choose an eBay category [at the product or category level](#configuring-ebay-options-for-products-and-categories).
    ![]({{site.baseurl}}/attachments/9306381/9438486.png)
    Note that category selection is likely to be a multi-step process: at first, the selector will show only top level eBay categories; once you select one of them, another selector will be displayed right below the first one so you can continue to select a nested category. You must continue selecting categories until you reach the lowest level of the eBay category hierarchy where you will be able to select the category that provides the most precise description of your products. At this point you should see a note "Allowed to select", which means the category selection process has been completed.
    ![]({{site.baseurl}}/attachments/9306381/9438487.png)
3.  (Optional step) In a similar way, use the **Additional eBay Category** selector to set a default _additional_ category for your products.
    ![]({{site.baseurl}}/attachments/9306381/9438488.png)
4.  Once you are happy with your default category settings, click **Next** to save your changes and head over to the next step of configuring your eBay Integration: [Configure the General settings for the X-Cart eBay Integration addon](#configuring-the-general-settings-for-the-x-cart-ebay-integration-addon).
    ![]({{site.baseurl}}/attachments/9306381/9438489.png)

## Configuring the General settings for the X-Cart eBay Integration addon

Before you start exporting products to eBay, you need to adjust the addon General settings.

To adjust the General settings for the X-Cart eBay Integration addon:

1.  In X-Cart Admin, in the **Categories** section of the eBay Configuration page (**Settings** > **eBay Configuration**), click **Next** to go to the **General Settings** section:
    ![]({{site.baseurl}}/attachments/9306381/9438489.png)
    If you have already configured your eBay General Settings previously, you can simply click the **General Settings** tab:
    ![]({{site.baseurl}}/attachments/9306381/9438491.png)

2.  Adjust the settings in the **Product options** section:
    ![]({{site.baseurl}}/attachments/9306381/9438492.png)
    The settings in this section will apply to all the products in your X-Cart store, for which similar settings have not been set [at the level of categories or individual products](#configuring-ebay-options-for-products-and-categories).

    *   **Listing duration**: Select a duration for your store's eBay listings. Ebay help on listing duration is available [here](http://pages.ebay.com/help/sell/duration.html).
    *   **Product condition**: Select the condition of the products you are going to export to eBay. Click the _Condition help_ link for help on item condition for your category.
    *   **Product price modifier**: If necessary, the price of items sold via eBay can be made higher or lower than the price of these items in your X-Cart store. The price difference can be implemented by setting a product price modifier. 
        For example, to add a $1 per item processing fee for eBay orders, you should set the price modifier as "[1.00] + [ $ ]":

        Image is missing

        This way all your items sold on eBay will be $1 more expensive than the items in your X-Cart store.
        To reduce the price of items sold on eBay by 10% of their price in your X-Cart store, you should set the price modifier as "[-10.00] + [ % ]":

        Image is missing

        (Note the minus sign before "10.00"; it shows that the price of items on eBay will be _lower_ than the original item price in the X-Cart store).
        The price modifier defined in the eBay Integration General Settings applies to your entire X-Cart store (i.e. all the products that will be exported to eBay). If you need a price modifier only for _some_ of the products, you should set the modifier [at the level of specific categories or individual products](#configuring-ebay-options-for-products-and-categories).
    *   **Exchange rate**: If the type of currency you use in your X-Cart store is different from the currency that will be used for your eBay listings (for example, if the prices at your X-Cart store are in Australian dollars, and the prices on eBay need to be specified in US dollars), use this field to set the exchange rate. The exchange rate will be used both when exporting your products from your X-Cart store to eBay and when importing orders from eBay back to your X-Cart store.
    *   **Export product description**: In X-Cart, a product can have two types of description: a short description and a detailed description. EBay listings can have just one description. So, before you export any products to eBay, you need to specify which of the two product descriptions should be used for eBay. Here you set the type of product description that should be exported to eBay by default. If any of your products need to use a different type of description on eBay, you can adjust this setting individually for these products in their [eBay product options](#configuring-ebay-options-for-products-and-categories). 
    *   **End a Listing when the stock of product hits zero**: Enable this option if you want your eBay listings to be ended automatically as soon as the stock quantity of the respective products in your X-Cart store reaches zero.

3.  Adjust the settings in the **System options** section:
    ![]({{site.baseurl}}/attachments/9306381/9438493.png)

    *   **Show eBay warning messages in admin area**: When exporting products to eBay or importing orders from eBay, you may get eBay warnings. Unlike errors, warnings are conditions that are not fatal to the addon operation, but they alert you to some minor problems that you may want to fix. Any warnings your store gets from eBay are written to log files in your X-Cart store. If, in addition to that, you also wish to have eBay warning messages displayed in your store's Admin area, enable this option. 
    *   **Save eBay API requests/responses in the log file**: If you need eBay API requests/responses to be written to log file (for example, if you need this information for debugging purposes), enable this option.
4.  Click **Save** to save your changes.

    ![]({{site.baseurl}}/attachments/9306381/9438494.png)
    You should see a success message like the following:
    ![]({{site.baseurl}}/attachments/9306381/9438495.png)

That is all;you have completed the basic configuration of your eBay Integration and can now start selling on eBay. However, if you require a more nuanced approach to publishing your products on eBay (for example, if you need to map your products to eBay categories more accurately than simply by setting one common default category for all your products), we recommend you take a couple more steps to complete your store's eBay related configuration. For more info, see the sections on configuring [eBay options for categories and products](#configuring-ebay-options-for-products-and-categories).

## Configuring eBay options for products and categories

The sections **Categories** and **General Settings** of the eBay Configuration page allow you to set the most basic rules for how your product information should be exported to eBay. This includes which eBay category your products should be exported to, whether a price modifier should be used to increase or decrease the product price on eBay, and so on.

By default, these rules will apply to all your products. However, if you want different products in your store to be treated differently (for example, if you want to publish different products in different eBay categories, or use a price modifier just for a couple of products), you will need to fine-tune your eBay export by adding more rules at the level of specific products and/or categories.

The rules in question can be set by configuring the eBay options for these products/categories. The eBay options set at the level of a specific product will apply to that product only. The eBay options set at the level of a category will apply to the products in that category and the products in all the subcategories of that category.

 To set eBay options for a category: 

1.  In the Manage categories section of your X-Cart store's Admin area (**Catalog** > **Categories**), find the category for which you need to set eBay options and click on its name to go to the category details page:
    ![]({{site.baseurl}}/attachments/9306381/9439148.png)
2.  On the category details page, select the **eBay category options** tab:
    ![]({{site.baseurl}}/attachments/9306381/9439149.png)
    The eBay category options page opens:
    ![]({{site.baseurl}}/attachments/9306381/9439150.png)

3.  Adjust the eBay options for the selected category:
    *   **Allow export to eBay**: Specify whether the products from this category and the subcategories of this category should be exported to eBay. If you do not intend to sell products from this category and its subcategories on eBay, you can forbid the export of this category to eBay by deactivating this option.
    *   **Main eBay Category**: Set the main eBay category for the products from the selected X-Cart category and the subcategories of this category.
    *   **Additional eBay Category**: Set the additional eBay category for the products from the selected X-Cart category and the subcategories of this category.
    *   **Product price modifier**: If the price of the products in the selected X-Cart category and its subcategories needs to be different from the price of these products on eBay, set a price modifier.
4.  Once you are done configuring the eBay options for the selected category, click **Save options** to save your changes.
    ![]({{site.baseurl}}/attachments/9306381/9439151.png)
    The eBay options for the category will be saved.

To set eBay options for a product:

1.  In your X-Cart store's Admin area, find the product for which you need to set eBay options. For example, you can find it via the Products section (**Catalog** > **Products**). Click on the product name to access the details of the product that has been found:
    ![]({{site.baseurl}}/attachments/9306381/9439152.png)
2.  On the product details page that opens, select the **eBay product options **tab:
    ![]({{site.baseurl}}/attachments/9306381/9439153.png)
    The eBay product options section of the product details opens:
    ![]({{site.baseurl}}/attachments/9306381/9439154.png)

3.  Adjust the eBay options for the selected product:

    *   **Allow export to eBay**: Specify whether the product should be exported to eBay. If you do not intend to sell this product on eBay, you can forbid the export of this product to eBay by deactivating this option.
    *   **Main eBay Category**: Set the main eBay category for the product.
    *   **Additional eBay Category**: Set the additional eBay category for the product.
    *   **Product price modifier**: If the price of the product on eBay needs to be different from the price of this product in your X-Cart store, set a price modifier.
    *   **Export product description**: In X-Cart, a product can have two types of description: a short description and a detailed description. EBay listings can have just one description. So, before you export any products to eBay, you need to specify what type of description should be used for the eBay listing that will be based on the selected product. The available options are _SShort description_ and _Full description_. These correspond to X-Cart's short and detailed product descriptions, respectively. 
    *   **eBay item ID**: Leave this field be; it will be populated with an item ID value automatically after the product is exported to eBay.
4.  Once you are done configuring the eBay options for the selected product, click **Save options** to save your changes. 
    ![]({{site.baseurl}}/attachments/9306381/9439155.png)
    The eBay options for the product will be saved.

_Related pages:_

*   {% link "X-Cart eBay Integration system requirements and installation" ref_RgzAH0hf %}
*   {% link "Exporting products to eBay" ref_40Al0Nky %}
*   {% link "Automated export of products to eBay and automated import of orders from eBay" ref_qPIZcwNs %}
