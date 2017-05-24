---
lang: en
layout: article_with_sidebar
updated_at: '2017-05-24 11:42 +0400'
identifier: ref_rOT8GezP
title: Free shipping
categories:
  - User manual
published: true
order: 140
---
To enable free shipping, use the module **Free shipping and Shipping freights** by X-Cart team (available in X-Cart Business, Multivendor, Ultimate editions).
    ![xc5_shipping_free_ship_ship_freights.png]({{site.baseurl}}/attachments/ref_rOT8GezP/xc5_shipping_free_ship_ship_freights.png)

With this module, X-Cart allows you to configure:

*   [Free shipping on specific products](#free-shipping-on-specific-products-or-all-products) (or all products);
*   [Free shipping on orders that meet certain conditions](#free-shipping-on-orders-that-meet-certain-conditions) (for example, orders delivered to addresses in the immediate vicinity of your store, or orders with a subtotal over a certain amount).

## Free shipping on specific products (or all products)

If you want to provide free shipping on a specific product, use the following method:

1.  In your store's back end, locate the product for which you want to configure free shipping.
2.  Click through to edit the details of this product . On the **Info** tab of the product details, enable the option **Free shipping**:
    ![]({{site.baseurl}}/attachments/6389844/9437240.png)
     (This option is available only for tangible goods; i.e. the property **Requires shipping** / **Shippable** must be set to "Yes" for the setting **Free shipping** to be visible).

3.  Use the **Update product** button at the bottom of the screen to save the changes. 

Now X-Cart will know that the cost of shipping for this product should be "0" (zero).

If necessary, you can use this method to enable free shipping on multiple products (and even on all the products in your store). It is also the method to use if you want to provide a "free in-store pickup" option for your products.

Note, however, that for the case when a customer's shopping cart contains only products with free shipping your store will need a free shipping method selectable at checkout. We provide a special shipping method for this purpose - "Free shipping". If you are going to provide free shipping on any products at your store, make sure this method is active:

![]({{site.baseurl}}/attachments/6389844/9437241.png)

 If necessary, you can edit the name and description of this method. For example, you may wish to change the name from "Free shipping" to "Free in-store pickup". To do so, click on the method name and adjust the information you require.

![]({{site.baseurl}}/attachments/6389844/9437242.png)

## Free shipping on orders that meet certain conditions

The method described in this section allows you to provide free shipping on orders that meet certain conditions.

For example, your store is in the United States, and you want to provide free delivery on orders over $50 that will be shipped to the contiguous United States. Here's the way to do it:

1.  In your store's Admin area, configure a destination zone for the contiguous United States (for example, name it "United States").
2.  Go to the Shipping methods section (**Store setup** > **Shipping**) and configure a new table-based shipping method for the free delivery of orders based on the conditions stated above:
    1.  Click the **Add shipping method** button.
    2.  In the popup window that appears, select the **Custom table rates** tab.
    3.  Provide general information about the shipping method and configure how shipping rates should be calculated for it:
        *   Enter a name for this shipping method (for example, "Free shipping" or "Free shipping on orders over $50").
        *   Set the **Address zone** property to whatever you named your zone for the contiguous U.S. (in our case, "United States").
        *   Specify that the table is based on "Subtotal" and set the **Subtotal range** to "$50.00 - $  ∞". Make sure that the fields **flat rate**, **per item**, **% and per weight unit** have zero values.![]({{site.baseurl}}/attachments/6389844/9437243.png)
    4.  Save your changes and make sure the method you configured is active.
3.  Make sure that all the products that will be shipped using this shipping method have the option **Requires shipping** (in older X-Cart versions - **Shippable**) enabled.

That is all. You should now have a free shipping method that will be displayed at checkout only when the customer's order amount is $50 or more, and the customer's address belongs to the "United States" address zone.

![]({{site.baseurl}}/attachments/6389844/9437251.png)

You can also set up your free method based on:

*   Weight range;
*   Items range;
*   Any combination of subtotal, weight and items ranges.
