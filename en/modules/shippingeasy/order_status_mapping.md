---
identifier: ref_o506IWMl
updated_at: 2014-11-13 00:00
layout: article_with_sidebar
lang: en
title: 'Order status mapping'
categories:
  - User manual

---


Order statuses used by ShippingEasy are not the same as those used by X-Cart, so, before orders from your X-Cart store can be exported to ShippingEasy, you will need to map order statuses in X-Cart to order statuses in ShippingEasy. To complete the task you will need to specify all the X-Cart statuses with which orders will need to be sent to ShippingEasy and - for each of these statuses - to specify the respective matching ShippingEasy statuses.

Here's how you can do it:

1.  In your X-Cart store's Admin area, go to the **ShippingEasy statuses** page (**Store setup **> **ShippingEasy statuses**):
    ![]({{site.baseurl}}/attachments/8224919/8355912.png)
    Initially, the **ShippingEasy statuses** page does not contain any items and looks as follows:
    ![]({{site.baseurl}}/attachments/8224919/8355913.png)
2.  Select **New item**: 
    ![]({{site.baseurl}}/attachments/8224919/8355914.png)

    This expands a section with two drop-down boxes:
    ![]({{site.baseurl}}/attachments/8224919/8355916.png)

3.  Use this section to specify a pair of matching statuses. For example, if you want order info to be sent to ShippingEasy when an order gets the payment status "Paid" in X-Cart, and you want this order to be marked as "Awaiting shipment" in ShippingEasy, you should select "Paid" from the drop-down box in the **X-Cart **payment **status** column and "Awaiting shipment" from the drop-down box in the **ShippingEasy status** column:
    ![]({{site.baseurl}}/attachments/8224919/8355917.png)

4.  Click **Save changes**:
    ![]({{site.baseurl}}/attachments/8224919/8355918.png)
    The pair of matching statuses will be saved:
    ![]({{site.baseurl}}/attachments/8224919/8355919.png)
5.  Repeat steps 1-4 if you need to specify more matching pairs of statuses. As a result, you should have all the X-Cart payment statuses for which order info needs to be sent automatically to ShippingEasy listed in the **X-Cart payment status** column, and their respective matching ShippingEasy statuses listed on the opposite side in the **ShippingEasy status** column:![]({{site.baseurl}}/attachments/8224919/8355920.png)

Note that your store will send order information to ShippingEasy no more than once per order. This means that when an order in X-Cart receives any of the statuses for which you have specified a matching status in ShippingEasy, information about this order will be automatically exported to ShippingEasy; if afterwards the status of this order in X-Cart changes to another status listed in the table, its information will _not_ be sent to ShippingEasy again. For example, according to the order statuses configuration demonstrated in the snapshot above (Partially Paid -> Awaiting shipment, Paid -> Awaiting payment), an order that gets the status "Partially Paid" in X-Cart will be sent to ShippingEasy; when this order is marked as "Paid", it won't be sent to ShippingEasy a second time. 

_Related pages:_

*   {% link "Manual export of orders to ShippingEasy" ref_t2NVGwT2 %}

## Attachments:

* [shippingeasy_xc5_statuses.png]({{site.baseurl}}/attachments/8224919/8355912.png) (image/png)
* [shippingeasy_xc5_statuses1.png]({{site.baseurl}}/attachments/8224919/8355913.png) (image/png)
* [shippingeasy_xc5_statuses_new_item.png]({{site.baseurl}}/attachments/8224919/8355915.png) (image/png)
* [shippingeasy_xc5_statuses_new_item.png]({{site.baseurl}}/attachments/8224919/8355914.png) (image/png)
* [shippingeasy_xc5_statuses2.png]({{site.baseurl}}/attachments/8224919/8355916.png) (image/png)
* [shippingeasy_xc5_statuses3.png]({{site.baseurl}}/attachments/8224919/8355917.png) (image/png)
* [shippingeasy_xc5_statuses4.png]({{site.baseurl}}/attachments/8224919/8355918.png) (image/png)
* [shippingeasy_xc5_statuses5.png]({{site.baseurl}}/attachments/8224919/8355919.png) (image/png)
* [shippingeasy_xc5_statuses_multiple.png]({{site.baseurl}}/attachments/8224919/8355920.png) (image/png)