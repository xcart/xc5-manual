---
identifier: ref_MKeFEB38
updated_at: 2015-09-29 00:00
layout: article_with_sidebar
lang: en
title: 'Setting up volume discounts for products'
categories:
  - User manual

---


X-Cart 5 allows you to configure volume discounts. A volume discount may be expressed as a fixed amount or a percentage off the order subtotal amount. Unlike {% link "coupon discounts" ref_EThAAs0G %}, volume discounts do not require your customers to enter any kind of secret code: a volume discount is applied automatically to any order that meets certain requirements. You define what these requirements should be. For example, you may create a discount that will be applied to orders with a subtotal amount equal to or greater than a certain amount, or will be applied to orders placed by users of a specific membership level.

When a volume discount is applied, the cart and checkout pages will show the discount amount on a separate line:

![]({{site.baseurl}}/attachments/6389792/8719445.png?effects=drop-shadow)

For purchases with a subtotal amount below the level needed to get a discount, a message like the following will be displayed:

![]({{site.baseurl}}/attachments/6389792/8719446.png?effects=drop-shadow)  

The volume discounts feature in X-Cart 5 is enabled by the module **Volume Discounts**:

![]({{site.baseurl}}/attachments/6389792/8719438.png?effects=drop-shadow)

To use the volume discounts feature, make sure the module is installed and enabled at your store. If the module is not installed, you can install it from the X-Cart Marketplace. For general module installation instructions, see [Installing modules from the Marketplace](http://kb.x-cart.com/display/XDD/Installing+modules+from+the+Marketplace).

To configure volume discounts:

1.  In your store's Admin area, go to the Volume discounts section (**Promotions** > **Volume discounts**).  
    ![]({{site.baseurl}}/attachments/6389792/8719439.png?effects=drop-shadow)
2.  Click the **Add discount** button.  
    ![]({{site.baseurl}}/attachments/6389792/8719440.png?effects=drop-shadow)  
    A section for adding a new discount will be displayed:  
    ![]({{site.baseurl}}/attachments/6389792/8719441.png?effects=drop-shadow)
3.  Specify the parameters of your discount in the fields of the section that has appeared.   
    For example, we want to create a discount to let **all our customers** (regardless of their membership level) to get a **10% discount** on orders wth a total amount **equal to or** **greater than $100**. In this case we need to configure the discount parameters as follows:  
    ![]({{site.baseurl}}/attachments/6389792/8719442.png?effects=drop-shadow)
4.  Once you are done, click the **Save changes **button.  
    ![]({{site.baseurl}}/attachments/6389792/8719443.png?effects=drop-shadow)

The discount will be added:

![]({{site.baseurl}}/attachments/6389792/8719450.png?effects=drop-shadow)

If necessary, you can add more than one discounts for the different subtotal ranges and membership levels. For example, with a setup like in the following screenshot all our customers will get a 10% discount off orders with a subtotal amount of $100 or more, and a 20% discount off orders with a subtotal amount of $200 or more; customers of the membership level "Wholesaler" will get 30% off any order of $200 or more.

![]({{site.baseurl}}/attachments/6389792/8719452.png?effects=drop-shadow)  

_Related pages:_

*   {% link "Configuring volume discounts and coupons in X-Cart 5" ref_rckpZ7SS %} (video)

## Attachments:

![](images/icons/bullet_blue.gif) [marketplace-volume-discounts.png]({{site.baseurl}}/attachments/6389792/6586420.png) (image/png)  
![](images/icons/bullet_blue.gif) [volume-discounts-menu.png]({{site.baseurl}}/attachments/6389792/6586422.png) (image/png)  
![](images/icons/bullet_blue.gif) [volume-discount-add-discount-button.png]({{site.baseurl}}/attachments/6389792/6586423.png) (image/png)  
![](images/icons/bullet_blue.gif) [volume-discounts.png]({{site.baseurl}}/attachments/6389792/6586424.png) (image/png)  
![](images/icons/bullet_blue.gif) [volume-discount-save-changes-button.png]({{site.baseurl}}/attachments/6389792/6586425.png) (image/png)  
![](images/icons/bullet_blue.gif) [frontend-checkout-no-volume-discount.png]({{site.baseurl}}/attachments/6389792/6586426.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_volume_discounts_module_installed_enabled.png]({{site.baseurl}}/attachments/6389792/8719438.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_volume_discounts_vd_section.png]({{site.baseurl}}/attachments/6389792/8719439.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_volume_discounts_add_discount0.png]({{site.baseurl}}/attachments/6389792/8719440.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_volume_discounts_add_discount1.png]({{site.baseurl}}/attachments/6389792/8719441.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_volume_discounts_add_discount2.png]({{site.baseurl}}/attachments/6389792/8719444.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_volume_discounts_add_discount3.png]({{site.baseurl}}/attachments/6389792/8719443.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_volume_discounts_add_discount2.png]({{site.baseurl}}/attachments/6389792/8719442.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_volume_discounts_checkout.png]({{site.baseurl}}/attachments/6389792/8719447.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_volume_discounts_get_discount.png]({{site.baseurl}}/attachments/6389792/8719448.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_volume_discounts_checkout.png]({{site.baseurl}}/attachments/6389792/8719449.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_volume_discounts_get_discount.png]({{site.baseurl}}/attachments/6389792/8719446.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_volume_discounts_checkout.png]({{site.baseurl}}/attachments/6389792/8719445.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_volume_discounts_from100.png]({{site.baseurl}}/attachments/6389792/8719451.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_volume_discounts_from100.png]({{site.baseurl}}/attachments/6389792/8719450.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_volume_discounts_list.png]({{site.baseurl}}/attachments/6389792/8719452.png) (image/png)