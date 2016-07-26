---
identifier: ref_nFq48dhr
updated_at: 2015-11-13 00:00
layout: article_with_sidebar
lang: en
title: 'Configuring the Multi-vendor module'
categories:
  - User manual

---


After the Multi-vendor module has been installed and enabled, it needs to be configured.

To configure the module:

1.  In the Installed Modules section of your X-Cart store’s Admin area, locate the entry for "Multi-vendor" and click the **Settings **link below it:![]({{site.baseurl}}/attachments/8749139/8716518.png?effects=drop-shadow)
    This opens the '"Multi-vendor" module settings' page:
    ![]({{site.baseurl}}/attachments/8749139/8719612.png?effects=drop-shadow)
2.  Adjust the module settings:

    *   **Multivendor mode**: Select the operation mode for your multi-vendor store_ (Warehouse / Vendors as separate shops)_. 

        | Warehouse |  Vendors as separate shops |
        | 

        *   When a customer's cart contains items from more than one vendor, a single order is formed.
        *   Processing of the order is done by admin. Vendors cannot edit the order.
        *   The order is delivered as a single shipment from a single warehouse location. The cost of shipping is calculated for delivery from the Company address as specified by the store admin.

         | 

        *   When a customer's cart contains items from more than one vendor, a separate order is formed for every vendor.
        *   Vendors can fully edit their orders.
        *   Every order is delivered from the warehouse of the respective vendor. The cost of shipping is calculated for delivery from the address specified by the vendor.

         |

    *   **Order DST based commission rate** and **Order shipping cost based commission rate**: If you wish to charge your vendors a commission on every sale of their products through your store, use these fields to specify your commission rates. The "Order DST based commission rate" setting allows you to set a commission rate as a percentage of the order discounted subtotal (DST), the "Order shipping cost based commission rate" setting - as a percentage of the order shipping cost. As of X-Cart version 5.2.9, the rates specified here are applied to the sales of all the vendors in the store - there is no way to set different commission rates for different vendors. 
        The commission will be charged automatically when a buyer pays for an order containing products supplied by a vendor. You will be able to see the commission you earned on any vendor order in the Orders list section.
        Please note that the setting  "Order shipping cost based commission rate" applies only to the "Vendors as separate shops" multivendor mode (In the "Warehouse" mode, no shipping cost based commission is calculated, since the products of all the vendors are considered to be shipped from the same warehouse).

    *   **Vendor access to global attributes**: Specify whether your vendors should be allowed to add their own attribute values if they decide to use attributes added at product class and global levels by the store admin and/or other vendors.
        The available options here are "Use existing values only" and "Use existing and add new values".

    *   **Show vendor list in product filter**: This option applies only for stores using the "Product Filter" module. Enable this option if you want your store's visitors to be able to filter products by vendor. With this option enabled, your store's product filter will allow users to select the vendor whose products they wish to view. Note that filtering by vendor will be available only in categories that list products of more than one vendor. If you do not want to allow filtering by vendor, make sure this option is disabled.

3.  Click **Submit** to save the changes.

_Related pages:_

*   {% link "Multi-vendor module: system requirements and installation" ref_MRQEvicQ %}
*   {% link "Multi-vendor: Admin experience" ref_6kbIUy5R %}
*   {% link "Vendor registration" ref_SkW62BgH %}

## Attachments:

* [mv_module_config.png]({{site.baseurl}}/attachments/8749139/8716519.png) (image/png)
* [mv_module_config.png]({{site.baseurl}}/attachments/8749139/8716518.png) (image/png)
* [mv_module_config1.png]({{site.baseurl}}/attachments/8749139/8716520.png) (image/png)
* [xc5_multi_module_settings.png]({{site.baseurl}}/attachments/8749139/8719612.png) (image/png)