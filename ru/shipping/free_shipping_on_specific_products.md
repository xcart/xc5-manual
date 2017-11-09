---
lang: ru
layout: article_with_sidebar
updated_at: '2017-11-09 11:01 +0400'
identifier: ref_JQBTMTq5
title: Бесплатная доставка определенных продуктов
order: 40
published: false
---
С помощью модуля **Free shipping and Shipping freights**, которыe входят в X-Cart Business, X-Cart Multivendor и X-Cart Ultimate, можно настроить бесплатную доставку для некоторых продуктов. 
    ![xc5_freeshipping_module.png]({{site.baseurl}}/attachments/ref_IU9J0uuT/xc5_freeshipping_module.png)

Модуль позволяет исключить продукт, который доставляется бесплатно, из расчета стоимости доставки заказа, если в заказе есть такой продукт. Бесплатная доставка предоставляется без каких-либо дополнительных условий. Т.е. нельзя настроить такие специальные предложения, как, например, _эти продукты доставляются бесплатно, если куплены в одном заказе_ или _купи более 10 штук и получи доставку в подарок_.  Если для какого-то продукта настроена бесплатная доставка с помощью этого модуля, продукт всегда доставляется бесплатно.

Как настроить бесплатную доставку для продукта::

   1.  In your store's back end, locate the product for which you want to set free shipping.
   
   2.  Click through to edit the details of this product . On the **Info** tab of the product details, enable the option **Free shipping**.
     (This option is available only for tangible goods; i.e. the property **Requires shipping** / **Shippable** must be set to "Yes" for the setting **Free shipping** to be visible).

   3.  Use the **Update product** button at the bottom of the screen to save the changes. 

Now X-Cart will know that the cost of shipping for this product should be "0" (zero).

You can use this method to enable free shipping on more than one product.

If using real-time shipping rate calculation, any products with the "free shipping" option enabled will be excluded from shipping cost calculation completely.
If using manually defined shipping rates, the products with the "free shipping" option enabled will be taken into account when selecting the shipping methods and rates available for the order (iteration 1), but they will not take part in the calculation of the order shipping cost itself (iteration 2).

The second use case may require some clarification.

## Example 1

You have 2 items:
   * Item One - 0.5 lb, free shipping = yes.
   * Item Two - 0.5 lb, free shipping = no.

You have 2 rates:
   * Rate One: 0-0.99lb, flat rate - $5.00
   * Rate Two: 1-1.99lb, flat rate - $10.00

In this case, depending on the combination of the products in the shopping cart, the shipping rates will be as follows:
Item One only - $0.00 (as the product is to be shipped for free);
Item Two only - $5.00 (Rate One is applied)
Item One and Item Two together - $10.00 (Rate Two is applied: As a result of the 1st iteration, Rate One is excluded, since Product One and Product Two together have a weight equal to 1lb. As a result of the 2nd iteration, the cost of shipping is found to be $10.00 - because the flat rate for Rate Two is $10.00, regardless of the number of items.)

## Example 2

You have 2 items:
   * Item One - 0.5 lb, free shipping = yes, item cost- 100$
   * Item Two - 0.5 lb, free shipping = no, item cost- 50$

You have 2 rates:
   * Rate One: 0-0.99lb, rate - 10% 
   * Rate Two: 1-1.99lb, rate - 15%

In this case, depending on the combination of products in the shopping cart, the shipping rates will be as follows:
Item One only - $0.00 (as the product is to be shipped for free).
Item Two only - $5.00 (Rate One is applied,`50$*10%=$5` )
Item One and Item Two together - $7.50 (Rate Two is applied: As a result of the 1st iteration, Rate One is excluded, since Product One and Product Two together have a weight equal to 1lb. As a result of the 2nd iteration, the cost of shipping is calculated using the percent-based Rate Two, but the rate is applied to Item Two only, `50$*15% -$7.5`)

## "Free shipping" method
For the case when a customer's shopping cart contains only products with free shipping, and, for some reason, the store does not have any other shipping methods that can be used for them, the module provides a method "Free shipping". 
![xc5_freeshipping_specialfreeshipmethod.png]({{site.baseurl}}/attachments/ref_IU9J0uuT/xc5_freeshipping_specialfreeshipmethod.png)

If necessary, you can edit the name and description of this method. To do so, click on the method name and adjust the information you require.

_Related pages:_

   * {% link "Free shipping on orders that meet certain conditions" ref_T9GhEfev %}
