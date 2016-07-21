---
identifier: ref_II05AOGF
updated_at: 2014-04-09 00:00
layout: article_with_sidebar
lang: en
title: 'Pay with Amazon customer experience'
categories:
  - User manual

---


In the Customer area of your X-Cart store, in all the locations from which buyers can initiate checkout, the Pay with Amazon module adds a **Pay with Amazon** button:

Here's what it looks like on the "Your shopping bag" page:

![]({{site.baseurl}}/attachments/7504625/7602347.png?effects=drop-shadow)

in the "Minicart" widget:

![]({{site.baseurl}}/attachments/7504625/7602348.png?effects=drop-shadow)

and in the "Add to cart" popup:

![]({{site.baseurl}}/attachments/7504625/7602349.png?effects=drop-shadow)

Once the **Pay with Amazon** button is clicked, a pop-up window titled "Amazon Payments: Sign In" is displayed where the buyer is asked for their Amazon Payments account email address and password:

![]({{site.baseurl}}/attachments/7504625/7602350.png?effects=drop-shadow)

(As you can see in the screenshot above, you can add your company logo in the buyer authentication pop-up window. This can be done by uploading your own banner image on the "Settings" -> "Integration Settings" page in Seller Central).

After the buyer successfully authenticates, they find themselves on a special checkout page in X-Cart which has two Amazon widgets embedded in it: the AddressBook widget (the "Address Book" section) where the buyer can select a shipping address from their Amazon Payments account or add a new one and the Wallet widget (the "Payment Method" section) where the buyer can select a payment method from their Amazon Payments account:

![]({{site.baseurl}}/attachments/7504625/7602351.png?effects=drop-shadow)

Note that the buyer stays on your store's site throughout the checkout process, without ever being redirected to Amazon.

After selecting a shipping address and a payment method from their account, the buyer selects a shipping method. X-Cart uses the information provided by the customer to calculate the shipping cost and taxes. Then the buyer places the order using the **Place order** button. This sends a payment request to Amazon.

After submitting the order, the buyer sees X-Cart's standard order confirmation page ("Congratulations! Your order has been placed. You will receive your order confirmation shortly") displaying the order invoice with all the required information (The payment method is shown as "Pay with Amazon").  

The way in which the order status is handled after order placement depends on the Pay with Amazon module settings:

*   If the _Synchronous_ type of authorization request is used, the order status almost instantly becomes one of the following:
    *   "Authorized" (= successful authorization, possible in "Authorization then capture" capture mode);
    *   "Processed" (= successful authorisation and capture, possible in "Immediate Charge" capture mode);
    *   "Declined" (= transaction declined).
*   If the _Asynchronous_ type of authorization request is used, the order initially gets the status "Queued", and, a few minutes later, when the store receives the payment request processing status from Amazon through the Instant Payment Notification (IPN) service,  this order status is updated to either "Authorized"/"Processed" (dependes on the Capture mode) or "Declined".

When the order is created, appropriate order notifications are sent to the email addresses of the buyer and the store's orders department in accordance with your store's "General settings :: Email notifications options" configuration. When the payment's status in Amazon Payments transitions as a part of the payment process (for example, when you capture a previously authorized amount or issue a refund), appropriate notifications are sent as well.

_Related pages:_

*   {% link "Configuring the Pay with Amazon module" ref_T3zMut4t %}
*   {% link "Pay with Amazon admin experience" ref_iDgFCnRt %}

## Attachments:

![](images/icons/bullet_blue.gif) [PwA_button_cart.png]({{site.baseurl}}/attachments/7504625/7602347.png) (image/png)  
![](images/icons/bullet_blue.gif) [PwA_button_minicart.png]({{site.baseurl}}/attachments/7504625/7602348.png) (image/png)  
![](images/icons/bullet_blue.gif) [PwA_button_add2cart.png]({{site.baseurl}}/attachments/7504625/7602349.png) (image/png)  
![](images/icons/bullet_blue.gif) [PwA_amazon_signin_popup.png]({{site.baseurl}}/attachments/7504625/7602350.png) (image/png)  
![](images/icons/bullet_blue.gif) [PwA_widgets.png]({{site.baseurl}}/attachments/7504625/7602351.png) (image/png)