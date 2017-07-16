---
lang: en
layout: article_with_sidebar
updated_at: '2017-07-16 16:41 +0400'
identifier: ref_w5MRyybe
title: Getting started with MailChimp Integration with E-commerce support
order: 100
published: false
---
If the module "MailChimp Integration with Ecommerce support" is not installed in your store, you can find and install it via the **My addons** section of your store's Admin area.

To use the module, you will need a MailChimp account. If you do not yet have a MailChimp account, you can [sign up here](https://login.mailchimp.com/signup/?source=website&pid=xcart). If you expect to have 2,000 or fewer subscribers and to send up to 12,000 emails per month, you can use MailChimp for free. For higher sending volumes, MailChimp also offers a few [pricing plans](https://mailchimp.com/pricing/).

Once the module "MailChimp Integration with Ecommerce support" has been enabled in your X-Cart store, you will need to connect to your MailChimp account. The connection is done using an API key. Instructions for how to find or generate your API key are available in the MailChimp knowledge base article [About API keys](http://kb.mailchimp.com/integrations/api-integrations/about-api-keys).

Once an API key has been set up for your X-Cart store in your MailChimp account, you can go to the module settings page in your store's Admin area and use one of the following methods to connect to MailChimp:

*   Click on the link "Connect with your MailChimp account". On the MailChimp authorization page, enter your MailChimp login and password. Provided that the authorization goes successfully, your account will be connected to X-Cart automatically.
    OR:
*   Copy the API key you have set up in your MailChimp account for your X-Cart store and paste it into the field that says "Enter your MailChimp API key manually". Save the changes.

Once your X-Cart store has been connected to your MailChimp account, the module settings page in your X-Cart store's Admin area will show your MailChimp API key and provide some settings that you will be able to use to adjust your module preferences. For example, you will be able to toggle the E-commerce analytics and Abandoned carts features, choose how your customers should be able to subscribe to your MailChimp lists (whether a customer should be able to choose more than one list when subscribing, whether an additional confirmation should be required after a customer opts in to subscribe, etc.) For more info, see {% link "Configuring the MailChimp Integration with E-commerce support module" ref_ST1QnErC %}

If you've already had some lists and list groups configured in your MailChimp account before connecting your X-Cart store to MailChimp, you should expect to find these lists and groups imported into your X-Cart store as soon as the connection between the store and your MailChimp account has been established. To view and manage the lists imported from your account, go to the **Sales channels** > **MailChimp lists** page. At the least, you will need to visit this page and make sure that the lists to which you would like your store users to be able to subscribe are active for your store. For more info on managing lists in X-Cart, see {% link "Managing your MailChimp lists" %}. If you haven't yet created any lists on the MailChimp end and need more information on this topic, see the MailChimp Knowledge Base [article on Lists](http://kb.mailchimp.com/lists). 

As soon as your lists/groups are ready, your store's users will be able to subscribe to them via the subscription form on the checkout and registration pages. Registered customers will be able to change their subscriptions (add more lists/groups or unsubscribe completely) via the Account details page. You as the store administrator will also be able to edit the subscription preferences of your store users by editing the profiles of these users via your X-Cart store's Admin area. 

After setting up your lists in MailChimp, you will be able to create and send [Campaigns](http://kb.mailchimp.com/campaigns).

To make the most of MailChimp's e-commerce features, be sure to enable e-commerce link tracking when configuring your campaigns or automations to track purchases. 
To turn on e-commerce link tracking for a campaign, follow these steps:

   1.  Navigate to the Setup step of the Campaign Builder.
   2.  In the Tracking section, check the box next to E-commerce link tracking. 
   
This way you will be able to track individual visitors of your website attracted by your MailChimp campaigns, capture customers purchasing activity, and pass it all back to MailChimp. You will be able to view purchase details, conversions, and total sales on the Reports page in your MailChimp account. 

Note that MailChimp mailing lists support segmentation based on your subscribers' purchase activity: Orders amount (Biggest Spenders/Tiny spenders), Frequency of ordering (Frequent Buyers/We Miss You), Series of purchasing (after a specific product purchase). Based on your customers' purchasing activity, MailChimp will recommend products to your newsletter recipients. Every recipient will see a set of products that are more likely to be interesting particularly to them.

With the advanced Email Automation capabilities of MailChimp, you will be able to set emails or series of emails to be sent to your customers right away as soon as they take particular actions in your store, i.e. just subscribed, abandoned cart, made a first purchase, bought any/specific product, bought product from some category.



