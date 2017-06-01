---
lang: en
layout: article_with_sidebar
updated_at: '2017-05-31 18:24 +0400'
identifier: ref_C3AVd3Zp
title: ''
order: 100
published: false
---
[Kissmetrics](https://www.kissmetrics.com/) is a popular behavioral analytics and engagement platform. By connecting your X-Cart store to Kissmetrics, you get a mighty tool to analyze your online store and your customers’ behaviour in it.

An X-Cart 5 store can be connected to Kissmetrics using one of the following methods:
   
   * [Method 1: Paste some Kissmetrics-provided JS code into your store using X-Cart's custom JS feature](#method-1-paste-some-kissmetrics-provided-js-code-into-your-store-using-x-carts-custom-js-feature) (supported by X-Cart versions 5.1 and later). 
   * [Method 2: Connect X-Cart to Kissmetrics by means of the free Segment Integration module](method-2-connect-x-cart-to-kissmetrics-by-means-of-the-free-segment-integration-module) (available for all X-Cart 5 versions).

## Method 1: Paste some Kissmetrics-provided JS code into your store using X-Cart's custom JS feature

To connect your X-Cart store to Kissmetrics using this method, follow the steps below:

   1.  In the Admin area of your X-Cart store, go to Look and Feel > Custom JavaScript. A page like the following will be opened:
       <img>
    
   2.  Make sure the "Use Custom JS" selector above the text area is set to "ON". 
    
   3. In a new browser tab or window, go to the [Settings page](https://app.kissmetrics.com/settings) in your Kissmetrics account and copy the tracking snippet for pasting onto your site. Go back to the tab/window with the Admin area of your X-Cart store and paste the JS code you have copied into the text area for custom JS code. Be sure to remove the script tags (<script type="text/javascript"> and </script>) wrapping this JS code, as X-Cart adds such tags automatically in the background. 
    
   4. Save the changes by clicking the **Save changes** button.
   
   5. To make sure the tracking snippet you have just pasted works fine, verify that it is capable of logging your own activity in the store in Kissmetrics [Live](https://app.kissmetrics.com/live) mode. Use the field on the "My Activity" tab on the left hand side menu to paste the URL of your X-Cart store and click **Show my activity**; your site will open in a new browser window allowing you to track your own activity. Do a few things your store visitors typically do on your site: try to find a product, add it to the shopping cart, place an order, rate a product, and so on. If you can see all your actions tracked in Kissmetrics, you’re all set! 
      <img>
      
## Method 2: Connect X-Cart to Kissmetrics by means of the free Segment Integration module

Another method to connect your X-Cart 5 based store to Kissmetrics is by means of the free [Segment Intergation](https://market.x-cart.com/addons/segment-integration.html) module by Qualiteam. [Segment](http://support.kissmetrics.com/article/show/implementing-kissmetrics-with-segment) is a powerful data aggregation tool which automatically collects information about your store's visitors, tracks e-commerce events and can send the gathered data to over a hundred of apps for analytics, marketing, data processing and storing. Kissmetrics is among them. 

To use this method, you will need to have an account with both Kissmetrics and Segment. The latter is available for free for 1 source, so it may be sufficient for you. 

To connect your store to Kissmetrics via the Segment Integration module, follow the steps below:

   1. In your X-Cart store's Admin area, go to the Modules section and install the module Segment Integration from the X-Cart marketplace. 
   2. After installing the module, open its Settings page.
   3. Keeping the Segment Integration module settings page open in your web browser, open a new tab or window to go to Kissmetrics. 
      * If you already have a Kissmetrics account, simply login to Kissmetrics. 
      * If you don't yet have a Kissmetrics account, choose to [sign up](https://signin.kissmetrics.com/signup). Then, at the first step of the wizard, select the option "Enable with Segment", and you will be redirected to Segment to sign in/sign up. 


   


