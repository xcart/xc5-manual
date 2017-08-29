---
lang: en
layout: article_with_sidebar
updated_at: '2017-08-29 17:08 +0400'
identifier: ref_T9GhEfev
title: Free shipping on orders that meet certain conditions
order: 100
published: false
---
Core

(for example, orders delivered to addresses in the immediate vicinity of your store, or orders with a subtotal over a certain amount).

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
