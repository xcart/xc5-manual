---
identifier: ref_WO2CMR6d
updated_at: 2015-06-28 00:00
layout: article_with_sidebar
lang: en
title: 'Setting up a simple bookable product'
categories:
  - User manual

---


To create a simple bookable product (without product variants), follow these steps:

1.  Start creating a new product the normal way: specify a product name, choose a category, add images, etc.   
    ![]({{site.baseurl}}/attachments/8749984/8718722.png?effects=drop-shadow)
2.  Use the **Price** field to specify the price of reservation of the product for one day (or night).   
    If the price needs to vary, use this field to specify the base price - you will be able to add product options modifying this price after general information about the product has been saved. For information on setting up product options as price modifiers, see {% link "Managing attribute values" ref_uKVHuBU6 %}  
    Use the **Quantity in stock** field  to specify the maximum bookable quantity for the product. This quantity will be the maximum number of reservations of the product that can be made at the same time. For example, if you have only 8 units of an item that you can rent , your customers should not be able to reserve more than 8 units on any date; so, for such an item, you should specify the Quantity in stock as "8".  
    You probably won't need X-Cart to calculate shipping cost for your bookable product. To disable shipping calculation for the product, set the **Shippable** setting to "No".  
    ![]({{site.baseurl}}/attachments/8749984/8718720.png?effects=drop-shadow)  

3.  Provide the rest of general information about the product as needed and click **Add product** to save it. The product will be created.
4.  Continue configuring the product you have created: Switch to the **Booking** tab of the product details and set the **Product booking **option to "Enabled" to specify that this product is bookable:  
    ![]({{site.baseurl}}/attachments/8749984/8718724.png?effects=drop-shadow)  
    Be sure to click **Update** to save the changes.  

5.  If needed, configure product attributes to provide more details about the product and the available options.   
    For example, we can configure an option allowing customers to include some add-on items for an additional price:  
    ![]({{site.baseurl}}/attachments/8749984/8718725.png?effects=drop-shadow)

That is all; we have created a simple bookable product. Now you can check the result on the storefront. It should look something like this:

![]({{site.baseurl}}/attachments/8749984/8718726.png?effects=drop-shadow)

By clicking on the arrow icon next to the product name in the booking table, your customers can view the available options:

![]({{site.baseurl}}/attachments/8749984/8718727.png?effects=drop-shadow)

Note that the default wording used by the module "Booking" may not work well for your type of bookable products. For example, our demo wedding rentals website, on which the screenshot above was taken, would really benefit from replacing the phrases  "Room type" and  "Check dates (N-night stay)" with something like "Item" and  "Rental period (N day rental)". Not to worry - the wording can be fixed by editing the "Booking" module text labels. For details see {% link "Editing "Booking" module text labels to your needs" ref_k4DWqNTo %}.

_Related pages:_

*   {% link "Setting up a bookable product with variants" ref_o0sHduTv %}
*   {% link "Editing "Booking" module text labels to your needs" 8750032.html %}

## Attachments:

![](images/icons/bullet_blue.gif) [add_bookable_product.png]({{site.baseurl}}/attachments/8749984/8718719.png) (image/png)  
![](images/icons/bullet_blue.gif) [price_quantity_shippable.png]({{site.baseurl}}/attachments/8749984/8718723.png) (image/png)  
![](images/icons/bullet_blue.gif) [add_tree.png]({{site.baseurl}}/attachments/8749984/8718722.png) (image/png)  
![](images/icons/bullet_blue.gif) [price_quantity_shippable.png]({{site.baseurl}}/attachments/8749984/8718720.png) (image/png)  
![](images/icons/bullet_blue.gif) [product_booking_enabled.png]({{site.baseurl}}/attachments/8749984/8718724.png) (image/png)  
![](images/icons/bullet_blue.gif) [tree_attributes.png]({{site.baseurl}}/attachments/8749984/8718725.png) (image/png)  
![](images/icons/bullet_blue.gif) [tree_storefront1.png]({{site.baseurl}}/attachments/8749984/8718726.png) (image/png)  
![](images/icons/bullet_blue.gif) [tree_storefront2.png]({{site.baseurl}}/attachments/8749984/8718727.png) (image/png)