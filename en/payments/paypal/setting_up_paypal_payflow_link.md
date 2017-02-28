---
lang: en
layout: article_with_sidebar
updated_at: '2017-02-28 15:37 +0400'
identifier: ref_mTCkpViN
title: Setting up Paypal Payflow Link
categories:
  - User manual
published: false
order: 160
---
To set up Paypal PayPal Payflow Link in X-Cart:

1.  In your X-Cart store's Admin area, go to the Payment methods page (**Store setup > Payment methods**). In the section for Online methods, click **Add payment method**:
![xc5_pp_add_payment_method.png]({{site.baseurl}}/attachments/ref_DT2EX6fz/xc5_pp_add_payment_method.png)

2.  In the popup box that appears, find the method **PayPal Payments Standard** and select to **Add** this method:
![xc5_pp_payflowlink_add.png]({{site.baseurl}}/attachments/ref_mTCkpViN/xc5_pp_payflowlink_add.png)

3.  Once the method has been added, configure the method settings:
![xc5_pp_payflow_link_settings.png]({{site.baseurl}}/attachments/ref_mTCkpViN/xc5_pp_payflow_link_settings.png)

'Your account settings' section:

    *   **Partner name**: Enter the ID of the partner that signed you up for the account. If you signed up directly through PayPal, this will be "PayPal".

    *   **Merchant login**: Specify the merchant login name that you chose when you signed up for PayPal Payflow Link.

    *   **User**: Enter the username that you set up for running transactions. If you have not specifically set up a username to run transactions, then this will be the same as the "Merchant login".

    *   **Password**: Enter the password that was created for the user account denoted in the "User" field.

'Additional settings' section:

    *   **Transaction type**: Specify the type of transaction that you want to be performed on order placement when a buyer pays you via PayPal Payflow link (_Auth_ or _Auth and capture_).

    *   **Test/Live mode**: Set the operating mode for PayPal Payflow Link ('Live' should be selected for live stores, 'Test' - for testing. Note that for testing purposes you will need to use test PayPal accounts).

    *   **Order id prefix**: Your trading name or any other prefix that will help you to identify a payment transaction as originating from this store. This field is required if using the same PayPal account for more than one online stores.

    *   **Display the "Buy Now with PayPal" button**: This setting determines whether or not the "Buy Now with PayPal" button should be displayed on product list pages (in list view) and product details pages.