---
identifier: ref_87Vtn3Al
updated_at: 2016-06-21 00:00
layout: article_with_sidebar
lang: en
title: 'Understanding X-Cart order statuses'
categories:
  - User manual

---


# System order statuses

Every order in your X-Cart store has a payment status and a shipping status. These two statuses provide information as to the current state of the order in the {% link "order processing workflow" ref_87Vtn3Al %}. 

By default, X-Cart uses the following order statuses:

**Payment statuses**

<table class="confluenceTable">

<tbody style="margin-left: 30.0px;">

<tr style="margin-left: 30.0px;">

<td class="confluenceTd">Q</td>

<td class="confluenceTd">Awaiting payment</td>

<td class="confluenceTd">

The order has been created, but has not been paid yet. It is used as the initial status of all orders for which an offline payment method was selected (like Phone ordering, Wire Transfer, etc.) It may also be assigned as a temporary initial status to orders for which an online payment method was selected. In this case the "Awaiting payment" status indicates that the buyer has submitted their payment information, but the result of the transaction is not known yet: the order payment is neither successfully processed nor declined yet.

</td>

</tr>

<tr style="margin-left: 30.0px;">

<td class="confluenceTd">P</td>

<td class="confluenceTd">Paid</td>

<td class="confluenceTd">The buyer has been fully charged for their purchase. With online payment methods, this usually means that the money for the purchase has been transferred to the merchant's account.</td>

</tr>

<tr style="margin-left: 30.0px;">

<td class="confluenceTd">PP</td>

<td class="confluenceTd">Partially paid</td>

<td class="confluenceTd">The order has been partially paid (or there has been a partial refund).</td>

</tr>

<tr style="margin-left: 30.0px;">

<td class="confluenceTd">A</td>

<td class="confluenceTd">Authorized</td>

<td class="confluenceTd">

This status can only be set by a payment processor (cannot be set manually). It indicates that an authorization has been placed on the buyer's card to ensure the buyer has sufficient credit or balance to pay for the purchase. The bank has put a hold on the requested amount, but the money has not been transferred to the merchant yet.The merchant has yet to place a charge to capture it.

</td>

</tr>

<tr style="margin-left: 30.0px;">

<td colspan="1" class="confluenceTd">D</td>

<td colspan="1" class="confluenceTd">Declined</td>

<td colspan="1" class="confluenceTd">This status can only be set by a payment processor (cannot be set manually). It indicates that an attempt to authorize or charge the buyer's card has failed and the order has been cancelled.</td>

</tr>

<tr style="margin-left: 30.0px;">

<td colspan="1" class="confluenceTd">C</td>

<td colspan="1" class="confluenceTd">Cancelled</td>

<td colspan="1" class="confluenceTd">The order has been cancelled by the merchant.</td>

</tr>

<tr style="margin-left: 30.0px;">

<td colspan="1" class="confluenceTd">R</td>

<td colspan="1" class="confluenceTd">Refunded</td>

<td colspan="1" class="confluenceTd">The money for the purchase has been refunded in full.</td>

</tr>

</tbody>

</table>

The statuses Awaiting payment, Paid and Authorized cause the inventory levels of the ordered items to be decreased according to the quantities ordered. The statuses Refunded, Cancelled and Declined cause the items to be restocked. The status Partially Paid does not affect the inventory.

**Shipping statuses**

<table class="confluenceTable">

<tbody style="margin-left: 60.0px;">

<tr style="margin-left: 60.0px;">

<td class="confluenceTd">N</td>

<td class="confluenceTd">New</td>

<td class="confluenceTd">The initial status assigned by default to any new order once it has been created.</td>

</tr>

<tr style="margin-left: 60.0px;">

<td class="confluenceTd">P</td>

<td class="confluenceTd">Processing</td>

<td class="confluenceTd">The merchant is working on the order.</td>

</tr>

<tr style="margin-left: 60.0px;">

<td class="confluenceTd">S</td>

<td class="confluenceTd">Shipped</td>

<td class="confluenceTd">The merchant has shipped the order.</td>

</tr>

<tr style="margin-left: 60.0px;">

<td class="confluenceTd">D</td>

<td class="confluenceTd">Delivered</td>

<td class="confluenceTd">The buyer has received the package.</td>

</tr>

<tr style="margin-left: 60.0px;">

<td colspan="1" class="confluenceTd">WND</td>

<td colspan="1" class="confluenceTd">Will not deliver</td>

<td colspan="1" class="confluenceTd">The order will not be shipped to the buyer for some reason.</td>

</tr>

<tr style="margin-left: 60.0px;">

<td colspan="1" class="confluenceTd">R</td>

<td colspan="1" class="confluenceTd">Returned</td>

<td colspan="1" class="confluenceTd">The buyer is returning the ordered items; the items have been sent back to the merchant.</td>

</tr>

<tr style="margin-left: 60.0px;">

<td colspan="1" class="confluenceTd">NF</td>

<td colspan="1" class="confluenceTd">Not Finished</td>

<td colspan="1" class="confluenceTd">(Enabled by the module Not Finished Orders). After the buyer's attempt to pay for the order, the payment system has returned the "cancelled" or "failed" callback, so the order payment status has been set to "Declined".</td>

</tr>

</tbody>

</table>

Note

Icon

What you see in the first columns of the above tables is letter codes by which X-Cart's system order statuses are represented in the software code; these codes are used only internally.

For information on _custom order statuses_, see the {% link "Managing X-Cart order statuses (X-Cart 5.2.7 and later)" ref_VLNBHNDw %} section of this manual.

# Order workflow

For orders paid using offline payment methods, the order processing workflow is as follows:

*   A new order is created with the status Awaiting payment.
*   As the order progresses through the various stages of the order processing and fulfillment process, the store administrator manually updates the order status. The current status of the order can be changed manually to any other status at any time. Typically, after the order payment has been received, the status Awaiting payment will be changed to Paid; if the order is cancelled - to Cancelled. After a refund, the status Paid will have to be changed to Refunded. The status Partially Paid is possible in case of a partial payment for the order or a partial refund.

For orders paid using online payment processors, the regular order processing workflow looks as follows:

*   A new order is created with the status Awaiting payment, Paid or Authorized - depending on the payment method settings and the type of response received from the payment gateway.
*   If the initial order status is Awaiting Payment or Authorized, it may be changed automatically to Paid, Partialy Paid or Declined (The resulting status depends on the callback received from the payment gateway).
*   If the order status is Paid, the order may be refunded. This is only possible if the payment gateway supports refunds. After a full refund, the order status is automatically changed to Refunded. After a partial refund, the order status becomes Partialy Paid.
*   If necessary, the store administrator can intervene at any stage of the order processing flow and manually change the current status of the order to any status they require.

_Related pages:_

*   {% link "Managing X-Cart order statuses (X-Cart 5.2.7 and later)" 8750763.html %}