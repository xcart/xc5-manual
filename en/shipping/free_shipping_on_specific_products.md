---
lang: en
layout: article_with_sidebar
updated_at: '2017-08-31 23:39 +0400'
identifier: ref_IU9J0uuT
title: 'Free shipping on specific products '
order: 100
published: false
---
With the module **Free shipping and Shipping freights** by X-Cart team (available in X-Cart Business, Multivendor, Ultimate editions), it is possible to configure free shipping on specific products. 
    ![xc5_shipping_free_ship_ship_freights.png]({{site.baseurl}}/attachments/ref_rOT8GezP/xc5_shipping_free_ship_ship_freights.png)

The module enables you to mark the products that should be shipped for free. The free shipping is unconditional, which means that so far you cannot configure any special offers like "these products, if purchased together, are shipped for free" or "buy 10+ items and get free shipping". If free shipping is enabled for a particular product using this module, this product is always shipped for free.

To provide free shipping on a specific product, use the following method:

   1.  In your store's back end, locate the product for which you want to set free shipping.
   
   2.  Click through to edit the details of this product . On the **Info** tab of the product details, enable the option **Free shipping**:
    ![]({{site.baseurl}}/attachments/6389844/9437240.png)
     (This option is available only for tangible goods; i.e. the property **Requires shipping** / **Shippable** must be set to "Yes" for the setting **Free shipping** to be visible).

   3.  Use the **Update product** button at the bottom of the screen to save the changes. 

Now X-Cart will know that the cost of shipping for this product should be "0" (zero).

You can use this method to enable free shipping on more than one product.

If you use real-time shipping rate calculation, any products with the "free shipping" option enabled will be excluded from shipping cost calculation completely.
If you use manually defined shipping rates, the products with the "free shipping" option enabled will be taken into account when selecting the shipping methods and rates available for the order (iteration 1), but they will not take part in the calculation of the order shipping cost itself (iteration 2).

Note, however, that for the case when a customer's shopping cart contains only products with free shipping your store will need a free shipping method selectable at checkout. We provide a special shipping method for this purpose - "Free shipping". If you are going to provide free shipping on any products at your store, make sure this method is active:

![]({{site.baseurl}}/attachments/6389844/9437241.png)

 If necessary, you can edit the name and description of this method. To do so, click on the method name and adjust the information you require.


