---
lang: en
layout: article_with_sidebar
updated_at: '2017-03-07 09:17 +0400'
identifier: ref_DT2EX6fz
title: Setting up Paypal Payments Standard
categories:
  - User manual
published: false
order: 120
---

To enable PayPal Payments Standard as a payment method in your X-Cart store:

1.  If you haven't yet done so, [sign up](https://www.paypal.com/webapps/mpp/referral/paypal-payments-standard?partner_id=XCART5_Cart "Sign up for PayPal Payments Standard") for PayPal Payments Standard. Note that to complete the signup process for PayPal Payments Standard you will need a verified PayPal Business account. This means that you will need to either create a new Business account or to log in to your existing account and upgrade it to Business.

2.  In X-Cart, add PayPal Payments Standard to the list of your store's active payment methods and configure it.

    1.  In your X-Cart store's Admin area, go to the Payment methods page (**Store setup > Payment methods**). In the section for Online methods, click **Add payment method**:
    ![xc5_pp_add_payment_method.png]({{site.baseurl}}/attachments/ref_DT2EX6fz/xc5_pp_add_payment_method.png)

    2.  In the popup box that appears, find the method **PayPal Payments Standard** and select to **Add** this method:
![xc5_pp_standard_add.png]({{site.baseurl}}/attachments/ref_DT2EX6fz/xc5_pp_standard_add.png)
    
    3.  Once the method has been added, you will be redirected to the settings page for PayPal Payments Standard. Сonfigure PayPal Payments Standard settings:
![xc5_pp_standard_settings.png]({{site.baseurl}}/attachments/ref_DT2EX6fz/xc5_pp_standard_settings.png)

        'Your account settings' section:

         *   **PayPal ID / Email**: Enter the email address associated with your PayPal account.

        'Additional settings' section:

         *   **Purchase description**: Enter a generic description of a typical purchase at your store. This description is intended for the PayPal payment page; the purpose of this description is to let the customer know what exactly they are paying for. Note that in most cases, when redirected to PayPal to pay for their purchase, your customers will see the actual product names (and thus will know what they are paying for). The generic description is needed only for backup: your customers will see it only if the actual list of items being purchased may not be displayed by PayPal for some reason. This may happen, for example, if the order total amount in X-Cart does not exactly match the order total amount on the PayPal end (This is typically caused by the rounding of decimals: in X-Cart, we round long decimals to the fourth digit after the decimal point, whereas decimal values passed on to PayPal need to be rounded to the second digit after the decimal point; when the totals in X-Cart and in PayPal do not match, PayPal cannot display the actual product names and prices, so that's when the generic description is used).

         *   **Test/Live mode**: Set the operating mode for PayPal Payments Standard ('Live' should be selected for live stores, 'Test' - for testing. Note that for testing purposes you will need to use test PayPal accounts in place of all the live accounts used while processing a live transaction; i.e. you will need at least one test seller account and one test buyer account. Test accounts for PayPal Payments Standard can be set up in the [PayPal Sandbox](https://developer.paypal.com/docs/classic/lifecycle/ug_sandbox/ "Setting up Paypal Payments Standard") - a self-contained testing environment for PayPal applications. The Sandbox mirrors the features found on the PayPal production servers and allows you to run test checkouts without any money changing hands or accounts being debited).

         *   **Order id prefix**: Specify your trading name or any other prefix that will help you to identify a payment transaction as originating from this store. This field is required if using the same PayPal account for more than one online stores.

    4.   Click **Save changes**:
         ![xc5_pp_standard_settings_save.png]({{site.baseurl}}/attachments/ref_DT2EX6fz/xc5_pp_standard_settings_save.png)

         The method settings will be saved.
         
    5.   Make sure the method is active:
         ![xc5_pp_standard_activate.png]({{site.baseurl}}/attachments/ref_DT2EX6fz/xc5_pp_standard_activate.png)

         
