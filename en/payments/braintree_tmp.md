---
lang: en
layout: article_with_sidebar
updated_at: '2017-10-10 11:16 +0400'
identifier: ref_3U96LOWn
title: ''
order: 100
published: false
---
X-Cart can be integrated with [Braintree, A PayPal Service](https://www.braintreepayments.com/). Currently, there are two Braintree integration modules available in the X-Cart Marketplace:
   
   * **[PayPal powered by Braintree](https://market.x-cart.com/addons/paypal-powered-by-braintree.html)** 
   * **[Braintree payment gateway](https://market.x-cart.com/addons/braintree-for-xcart5.html)**

The module "PayPal powered by Braintree" is the newer of the two. It is the most advanced payment solution from PayPal to date, and it is based on the latest Braintree API. 
The module "Braintree payment gateway" is an older version of the integration based on the previous version of Braintree API. 
Because the new API (the one used by "PayPal powered by Braintree") is currently available only to users in the USA, UK and France, we are keeping the module "Braintree payment gateway" available to X-Cart customers through the Marketplace as it uses an API available in many more countries.

Depending on the X-Cart version you are using, a Braintree integration module may already be installed on your X-Cart store:
![xc5_braintree_module_installed.png]({{site.baseurl}}/attachments/ref_3U96LOWn/xc5_braintree_module_installed.png)

If not, you can obtain it from the X-Cart Marketplace at any time:
![xc5_braintree_module.png]({{site.baseurl}}/attachments/ref_3U96LOWn/xc5_braintree_module.png)

To enable Braintree as a payment method in your X-Cart store:

1.  If you haven't yet done so, [sign up](https://... "Sign up for Braintree") for Braintree. 

2.  In X-Cart, add Braintree to the list of your store's active payment methods and configure it.

    1.  In your X-Cart store's Admin area, go to the Payment methods page (**Store setup > Payment methods**). In the section for Online methods, click **Add payment method**:
        
        ![xc5_braintree_add_payment_method.png]({{site.baseurl}}/attachments/ref_3U96LOWn/xc5_braintree_add_payment_method.png)

    2.  In the popup box that appears, find the Braintree method you require (in our case **PayPal Powered by Braintree**) and select to **Add** this method:

        ![xc5_braintree_payment_method_add.png]({{site.baseurl}}/attachments/ref_3U96LOWn/xc5_braintree_payment_method_add.png)
 
        The method will be added:
     
        ![xc5_braintree_payment_method_added_successfully.png]({{site.baseurl}}/attachments/ref_3U96LOWn/xc5_braintree_payment_method_added_successfully.png)

        Note that if the Braintree integration module is not installed at the time of adding the method, there will be an **Install** button instead of **Add**: 
        
        ![xc5_braintree_payment_method.png]({{site.baseurl}}/attachments/ref_3U96LOWn/xc5_braintree_payment_method.png)
        
        Use this button to install the module and add the method, after which you will be able to continue with configuring the Braintree method as provided below.
        
    3.  Once the method has been added, you will need to adjust the Braintree integration settings. You can access the settings page at any time by clicking the **Configure** button:
    
         ![xc5_braintree_configure_button.png]({{site.baseurl}}/attachments/ref_3U96LOWn/xc5_braintree_configure_button.png)
