---
lang: en
layout: article_with_sidebar
updated_at: '2017-11-08 13:31 +0400'
identifier: ref_DkbTi1qJ
title: Understanding X-Cart order statuses
categories:
  - User manual
published: true
order: 100
---


## System order statuses

Every order in your X-Cart store has a payment status and a fulfilment status. These two statuses provide information as to the current state of the order in the {% link "order processing workflow" ref_DkbTi1qJ %}. 

By default, X-Cart uses the following order statuses:

**Payment statuses**

{:.ui.compact.celled.small.padded.table}
| Q | Awaiting payment | The order has been created, but has not been paid yet. It is used as the initial status of all orders for which an offline payment method was selected (like Phone ordering, Wire Transfer, etc.) It may also be assigned as a temporary initial status to orders for which an online payment method was selected. In this case the "Awaiting payment" status indicates that the buyer has submitted their payment information, but the result of the transaction is not known yet: the order payment is neither successfully processed nor declined yet. |
| P | Paid | The buyer has been fully charged for their purchase. With online payment methods, this usually means that the money for the purchase has been transferred to the merchant's account. |
| PP | Partially paid | The order has been partially paid (or there has been a partial refund). |
| A | Authorized | This status can only be set by a payment processor (cannot be set manually). It indicates that an authorization has been placed on the buyer's card to ensure the buyer has sufficient credit or balance to pay for the purchase. The bank has put a hold on the requested amount, but the money has not been transferred to the merchant yet.The merchant has yet to place a charge to capture it. |
| D | Declined | This status can only be set by a payment processor (cannot be set manually). It indicates that an attempt to authorize or charge the buyer's card has failed and the order has been cancelled. |
| C | Cancelled | The order has been cancelled by the merchant. Typically, an order has to be in the Authorized or Awaiting payment state before it becomes Cancelled. |
| R | Refunded | The money for the purchase has been refunded in full. This status can be set automatically by payment processors whose X-Cart integration supports refunds, or it can be set manually by administrator. Typically, an order has to be in the Paid state before it becomes Refunded. |

The statuses Awaiting payment, Paid and Authorized cause the inventory levels of the ordered items to be decreased according to the quantities ordered. The statuses Refunded, Cancelled and Declined cause the items to be restocked. The status Partially Paid does not affect the inventory.

**Fulfilment statuses**

{:.ui.compact.celled.small.padded.table}
| N | New | The initial status assigned by default to any new order once it has been created. |
| P | Processing | The merchant is working on the order. |
| S | Shipped | The merchant has shipped the order. |
| D | Delivered | The buyer has received the package. |
| WND | Will not deliver | The order will not be shipped to the buyer for some reason. |
| R | Returned | The buyer is returning the ordered items; the items have been sent back to the merchant. |
| NF | Not Finished | (Enabled by the module Not Finished Orders). After the buyer's attempt to pay for the order, the payment system has returned the "cancelled" or "failed" callback, so the order payment status has been set to "Declined". |

{% note info %}
What you see in the first columns of the above tables is letter codes by which X-Cart's system order statuses are represented in the software code; these codes are used only internally.
{% endnote %}

For information on _custom order statuses_, see the {% link "Managing X-Cart order statuses (X-Cart 5.2.7 and later)" ref_7FIU2sxJ %} section of this manual.

## Order workflow

For orders paid using offline payment methods, the order processing workflow is as follows:

*   A new order is created with the status Awaiting payment.
*   As the order progresses through the various stages of the order processing and fulfillment process, the store administrator manually updates the order status. The current status of the order can be changed manually to any other status at any time. Typically, after the order payment has been received, the status Awaiting payment will be changed to Paid; if the order is cancelled - to Cancelled. After a refund, the status Paid will have to be changed to Refunded. The status Partially Paid is possible in case of a partial payment for the order or a partial refund.

We strongly recommend using the Refunded status (not Cancelled) when updating the order status from Paid, and Cancelled (not Refunded) when updating the order status from Authorized or Awaiting payment.


For orders paid using online payment processors, the regular order processing workflow looks as follows:

*   A new order is created with the status Awaiting payment, Paid or Authorized - depending on the payment method settings and the type of response received from the payment gateway.
*   If the initial order status is Awaiting Payment or Authorized, it may be changed automatically to Paid, Partialy Paid or Declined (The resulting status depends on the callback received from the payment gateway).
*   If the order status is Paid, the order may be refunded. This is only possible if the payment gateway supports refunds. After a full refund, the order status is automatically changed to Refunded. After a partial refund, the order status becomes Partialy Paid.
*   If necessary, the store administrator can intervene at any stage of the order processing flow and manually change the current status of the order to any status they require.

_Related pages:_

*   {% link "Managing X-Cart order statuses (X-Cart 5.2.7 and later)" ref_7FIU2sxJ %}
