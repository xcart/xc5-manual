---
lang: en
layout: article_with_sidebar
updated_at: '2017-08-30 14:11 +0400'
identifier: ref_T9GhEfev
title: Free shipping on orders that meet certain conditions
order: 100
published: false
---
You can easily configure your X-Cart store to provide free shipping on orders that meet certain conditions; for example:

   * orders with a subtotal over a certain amount ("free shipping on orders over $50");
   * orders delivered to addresses in a specific shipping zone ("free shipping on all orders within the contiguous United States", "free shipping within Germany", etc.);
   * orders containing a certain number of items ("buy 3 or more items, get free shipping");
   * orders weighing within a certain weight range ("orders up to 200 g ship free").

If necessary, it is possible to set up complex conditions based on a combination of any of the above (for example, "free shipping on orders over $50 shipped within Germany").

Let's take a closer look at how to configure free shipping for various types of conditions.

## Example 1. Free shipping on orders over $50
## Example 2. Free shipping within Germany
## Example 3. Free shipping on orders of 3 or more items
## Example 4. Free shipping on orders of up to 200 g weight
## Example 5. Free shipping on orders over $50 shipped within Germany

1.  In your store's Admin area, go to **Store setup** > **Countries, states and zones** and configure a destination zone including all the states and territories of the contiguous United States (for example, name it "United States").
2.  Go to the Shipping methods section (**Store setup** > **Shipping**) and create a new shipping method - the one to be used for orders that meet the above stated conditions (subtotal over $50 AND shipping to the contiguous U.S.):
    1.  Click the **Add shipping method** button.
    2.  In the popup window that appears, select the **Custom table rates** tab.
    3.  Provide general information about the shipping method and configure how shipping rates should be calculated for it:
        *   Enter a name for this shipping method (for example, "Free shipping" or "Free shipping on orders over $50").
        *   Set the **Address zone** property to whatever you named your zone for the contiguous U.S. (in our case, "United States").
        *   Specify that the table is based on "Subtotal" and set the **Subtotal range** to "$50.00 - $  ∞". Make sure that the fields **flat rate**, **per item**, **% and per weight unit** have zero values.
        ![]({{site.baseurl}}/attachments/6389844/9437243.png)
    4.  Save your changes and make sure the method you configured is active.
3.  Make sure that all the products that will be shipped using this shipping method have the option **Requires shipping** (in older X-Cart versions - **Shippable**) enabled.

That is all. You should now have a free shipping method that will be displayed at checkout only if the customer's order amount is $50 or more, and the customer's address belongs to the address zone you have configured for the contiguous United States.

![]({{site.baseurl}}/attachments/6389844/9437251.png)

You can also set up your free method based on:

*   Weight range;
*   Items range;
*   Any combination of subtotal, weight and items ranges.
