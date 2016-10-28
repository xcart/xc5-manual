---
lang: en
layout: article_with_sidebar
updated_at: '2016-10-28 13:57 +0400'
identifier: ref_Rzp45QlN
title: Setting up  VAT / GST (for EU and UK)
order: 100
published: false
---
If you are required to charge buyers a value added tax (VAT) or a goods and services tax (GST), we recommend using the module **Value Added Tax / Goods and Services Tax** for tax setup. This module is specifically designed for businesses in the UK, EU, Australia and other countries where you need to be able to charge VAT / GST. The module allows you to use different tax rates based on the membership level and address of the customer. It also supports tax exemption based on customer's VAT ID.

To start using the module "Value Added Tax / Goods and Services Tax", ensure that it is installed and enabled in your store's Installed Modules section.

This article explains how to set up and enable VAT / GST calculation using the module "Value Added Tax / Goods and Services Tax" for X-Cart 5. 

## Configuring VAT / GST

Before you configure your VAT / GST tax:

1.  Ensure that each of the products in your store to which VAT / GST needs to be applied has a tax class assigned to it. You can create your custom tax classes or use the "Default tax class" that is assigned to all your products by default. 
    See:

    *   {% link "Creating tax classes" ref_pAWOdG8N#creating-tax-classes %};

    *   {% link "Assigning tax classes to products" ref_pAWOdG8N#assigning-tax-classes-to-products %}.

2.  Ensure that your store has all the necessary address zones configured. You will need these zones to use different tax rates based on the customer address.
    See:

    *   {% link "Setting up destination (address) zones" ref_r68iO5Rm %}
    
3.  If you are going to need different tax rates for different customer membership levels, ensure that the necessary user membership levels have been set up. 
    See:

    *   {% link "Adding user membership levels" ref_9ITFspcC %}

To configure your VAT / GST tax, complete the following steps:
1.  In your store's Admin area, go to the Taxes section (**Store setup** > **Taxes**).
    ![]({{site.baseurl}}/attachments/8225533/8716413.png?effects=drop-shadow)
2.  Make sure you are viewing the **VAT / GST** tab.
    ![]({{site.baseurl}}/attachments/8225533/8716416.png?effects=drop-shadow)
3.  Configure the tax options in the **Common tax settings** section:
    ![]({{site.baseurl}}/attachments/8225533/8716417.png?effects=drop-shadow)

    *   Use the **Tax title** field to enter a general name describing the type of tax applied to orders in your store. This name will show on your store's checkout and on your customers' invoices. By default, _VAT_ is used as the tax title, but you can change it to _GST_ or any other name you require.
    *   Specify whether tax calculation rules for the tax you are configuring (we'll come to configuring these rules a bit later) should be the same for all your store's users, irrespective of their membership, or should be different depending on the users' membership. If the rules need to be the same for all your buyers, enable the option **Use the same tax rates for all user membership levels** by selecting the respective check box. If different membership levels need the tax to be calculated differently, leave this check box unselected.
    *   Use the selectbox titled **Address for VAT / GST calculation** to specify the address type based on which your VAT / GST tax needs to be calculated. The available options here are _Shipping address_ and _Billing address._ The address type you select here will be used to determine the customer's zone, which in its turn will be used to determine the tax rate that needs to be applied. For example, to charge sales tax based on where the product is being shipped to (not where it was purchased), you would need to choose the _Shipping address_ option in this field.
    *   Use

