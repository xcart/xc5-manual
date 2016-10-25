---
lang: en
layout: article_with_sidebar
updated_at: '2016-09-27 23:59 +0400'
identifier: ref_qAZlJxZm
title: 'Configuring your store&#39;s General settings'
categories:
  - User manual
published: true
order: 140
---

The most general settings that determine your store's appearance and behavior can be found in the **Store setup > Cart & checkout** section, on the **General** tab:

![]({{site.baseurl}}/attachments/7505478/8716538.png?effects=drop-shadow)

Below you can find some of the settings explained.

## Customer Zone settings

*   **Display check number for eCheck payment method**: This setting is used for stores using the Check payment method. It defines whether the payment information form provided to the customer who has chosen to pay by check should include a field for check number, or not.

*   **Subcategory listings format**: This setting defines how subcategories should be displayed on category pages. 
    Setting the subcategory listings format to "_Icons_" allows you to have icons displayed for your subcategories:
    ![]({{site.baseurl}}/attachments/7505478/7602697.png?effects=drop-shadow)
    Setting the format to "_List_" produces a simple list of subcategory names, without icons:
    ![]({{site.baseurl}}/attachments/7505478/7602698.png?effects=drop-shadow)
    Note that this setting does not apply to root (top level) categories. The appearance of root categories on the store's Front page can be adjusted with the setting 'Root category listings format' in the **Catalog > Front page** section.

*   **Default order to sort products within a category**: This setting allows you to control the default display order for products within a category. 
    The following options are available:

*   *   Recommended - The product sort order defined by the store owner via the category settings:
        ![]({{site.baseurl}}/attachments/7505478/8716548.png?effects=drop-shadow)

    *   Newest first - The sort order based on the arrival dates of specific products (Products with the latest arrival date are displayed first).
    *   Price ![]({{site.baseurl}}/attachments/7505478/7602702.png) - The low to high price sort order (Products with the lowest price are displayed first).
    *   Price ![]({{site.baseurl}}/attachments/7505478/7602700.png) - The high to low price sort order (Products with the highest price are displayed first).

    *   Name ![]({{site.baseurl}}/attachments/7505478/7602702.png) - The sort order in which products are sorted by their names, A to Z direction.
    *   Name ![]({{site.baseurl}}/attachments/7505478/7602700.png) - The sort order in which products are sorted by their names, Z to A direction.

*   **Products per category listing page**: This setting allows you to limit the number of products displayed on a category page. For example, if we set this to "2", only two products will be displayed per page. For the rest of the product list pagination will be provided:
    ![]({{site.baseurl}}/attachments/7505478/7602705.png?effects=drop-shadow)
*   **Maximum product image width (px)** and **Maximum product image height (px)**: These are the maximum dimensions with which product images will be displayed on the product details page.
    ![]({{site.baseurl}}/attachments/7505478/7602706.png?effects=drop-shadow)
     Images uploaded in a size larger than specified here will be resized; for such images the Magic Zoom feature will be available:
    ![]({{site.baseurl}}/attachments/7505478/7602707.png?effects=drop-shadow)
    X-Cart does not provide a limitation on the size of product images, and you can set any values you require for your store's maximum image width and height; however, you should make sure the result of your settings looks good on the store's pages. If your desired image dimensions break the surrounding page design, you may need to tweak it using custom CSS.

*   **Minimum allowed order subtotal**: This setting allows you to set the minimum order amount a shopper must reach before being allowed to check out.
    ![]({{site.baseurl}}/attachments/7505478/7602713.png?effects=drop-shadow)

*   **Maximum allowed order subtotal**: This setting allows you to set the maximum order amount. A shopper will be allowed to check out only if their order subtotal amount is less than this value.
    ![]({{site.baseurl}}/attachments/7505478/7602714.png?effects=drop-shadow)
*   **Maximum order quantity (per product) **(used to be "Default purchase limit" in earlier X-Cart 5 versions): This setting allows you to limit the number of product units that a buyer can order at a time. If a buyer attempts to add to cart more product units than specified here, only the allowed quantity will be added; the buyer will be notified of the quantity adjustment with an appropriate message (For example, "Sorry, there's a limit of 1 per order for the product `<Product name>`. 1 unit(s) already in cart.")

*   **Force customer to choose product options before adding a product to cart**: This setting affects the add to cart behavior of products with modifier options and products with product variants. When the option "Force customer to choose product options before adding a product to cart" is disabled, a shopper can drag and drop such products to cart without having to select any product options manually; the products are added to cart with default options:
    ![]({{site.baseurl}}/attachments/7505478/7602715.png?effects=drop-shadow)
    When this option is enabled, the "Drag and drop me to the cart" hint is not displayed for products with modifiers/variants, and the drag-and-drop to cart feature for such products is disabled. Instead, a shopper hovering their mouse over a product with modifiers/variants will see a note "Choose the product options first":
    ![]({{site.baseurl}}/attachments/7505478/7602716.png?effects=drop-shadow)
    The shopper will need to click on the product to access its details and make a selection of product options with which they want to add the product to cart.

*   **Redirect customer to the cart page after a product is added to cart**: When this option is enabled, after adding a product to cart a shopper is redirected to the cart page where they can see the item they just added. When the option is disabled, the shopper remains on the same page. Please note that this setting is not compatible with X-Cart's Add to Cart module: when the module Add to Cart popup is enabled, adding a product to cart results in a popup being displayed.

*   **Display "Add to cart" buttons for products in grid view**: This setting defines whether "Add to cart" buttons should be displayed for products in grid view, or not. The snapshot below demonstrates products in grid view with "Add to cart" buttons enabled: 
    ![]({{site.baseurl}}/attachments/7505478/7602709.png?effects=drop-shadow)
    Note that this setting affects only grid view (does not affect list view and table view; in list view and table view "Add to cart" buttons are displayed at all times - regardless of the value of this setting).

*   **Ask anonymous users to create an account or sign in before checkout**: When this option is enabled, a shopper who was not signed in when they clicked the Checkout button is provided with a page where they can sign in to their account or create a new account:
    ![]({{site.baseurl}}/attachments/7505478/7602723.png?effects=drop-shadow)
    When this option is disabled, such a page is not provided, and the shopper goes straight to the store's checkout page. 
    Regardless of whether this option is enabled or disabled, on the checkout page, the shopper will still be able to sign in if they choose to do so: 
    ![]({{site.baseurl}}/attachments/7505478/7602724.png?effects=drop-shadow)
    And even if the "Sign in" link at the top of the page goes unnoticed, an existing user will be recognized by the system based on their email address and prompted to sign in:
    ![]({{site.baseurl}}/attachments/7505478/7602725.png?effects=drop-shadow)

*   **Terms and conditions relative URL**: You can create a static page for Terms and conditions using Simple CMS module and specify its relative url here. if field is empty (for example, Simple CMS is not installed, but you still need T&c), then lang var from ?target=terms (Terms and conditions text) is used (text will be displayed in a popup for Terms and conditions on checkout).  (Core, Simple CMS module not necessary)

*   **Next order #**: This field allows you to increase the order number starting from which orders in your store will be numbered. For example, if your store has just went into production and does not yet have many orders, your first customers may be scared off by the order numbers they get. For new customers, a business with order numbers like #1 or #2 may not seem trustworthy enough. To generate more trust, you can set this field, for example, to 103 (In practice, this value can be set to any number - the only requirement is that this number must be greater than the number of the latest order in your database). Your next order will then be #103, and after that you will get the order numbers #104, #105, etc.

*   **Cart TTL (days)**: When a new visitor comes to an X-Cart based store for the first time, a "cart" is created for them in the store's database. Since a lot of visitors will leave the store without creating an account, it's no use storing their carts forever (For visitors who become registered customers, the "cart" is stored for the lifetime of the respective user account). The setting "Cart TTL (days)" allows you to limit the time period for which anonymous shopping carts (carts of visitors who do not have an account) should be stored in the database. Anonymous carts older than the number of days specified here will be considered old (expired) and will be scheduled for deletion by the internal cron service (See the setting below).

*   **Enable internal cron service**: This setting allows you to enable/disable the use of your store's internal cron service. This service schedules the run of certain maintenance tasks required to keep your store running smoothly and problem-free (like removing the expired shopping carts of visitors who do not have an account with your store or performing other tasks implemented via X-Cart modules) at the periodicity of once per 100 user sessions (i.e. every time after your store gets 100 unique visitors). Your store's internal cron service is not related to {% link "console.php" ref_lLqNzAaq %} and does not require any external setup of the crontab on your system. If using the internal cron service causes performance problems for your store, we recommend disabling this option and using an external cron setup to run console.php. 

## Administrator Zone settings

*   **Products per page**: This setting allows you to specify the maximum number of products that can be displayed on a search results page in the store's back end.
*   **Users per page**:  This setting allows you to specify the maximum number of users that can be displayed on a search results page in the store's back end.
*   **Orders per page**:  This setting allows you to specify the maximum number of orders that can be displayed on a search results page in the store's back end.
*   **The number of orders in the recent order list**: This setting allows you to specify the maximum number of orders that can be displayed in the "Recent orders" list in the store's back end.
*   **Number of days to store the last login data**: This setting defines the lifespan of a "recent_login" cookie that is set by the store on a customer's computer when they log in. While being stored, the cookie allows the customer to return to the store without having to re-enter their user authentication details (username and password).
