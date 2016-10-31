---
lang: en
layout: article_with_sidebar
updated_at: '2016-10-31 17:15 +0400'
identifier: ref_hxmof6xX
title: Setting up Canadian taxes
order: 400
published: false
version: X-Cart 5.3.2 and later
---
If your business is based in Canada and you need to configure taxes like Canadian VAT, PST (QST) or HST, we recommend using the module **Canadian Taxes** for tax setup. 
    ![xc5_taxes_canada_canadian_taxes_module.png]({{site.baseurl}}/attachments/ref_hxmof6xX/xc5_taxes_canada_canadian_taxes_module.png?effects=drop-shadow)
    
To start using the module "Canadian Taxes", ensure that it is installed and enabled in your store's Installed Modules section.

This article explains how to set up and enable the calculation of Canadian taxes using the module "Canadian Taxes" for X-Cart 5. 

## Configuring Canadian taxes

Before you configure your taxes:

1.  Ensure that each of the products in your store to which a tax needs to be applied has a tax class assigned to it. You can create your custom tax classes or use the "Default tax class" that is assigned to all your products by default. 

    See:
    
    *   {% link "Creating tax classes" ref_pAWOdG8N#creating-tax-classes %};
    
    *   {% link "Assigning tax classes to products" ref_pAWOdG8N#assigning-tax-classes-to-products %}.

2.  Ensure that your store has all the necessary address zones configured. You will need these zones to use different tax rates based on the customer address.
    
    See:
    
    *   {% link "Setting up destination (address) zones" ref_r68iO5Rm %}
    
3.  If you are going to need different tax rates for different customer membership levels, ensure that the necessary user membership levels have been set up. 
    
    See:
    
    *   {% link "Adding user membership levels" ref_9ITFspcC %}

To configure Canadian taxes, complete the following steps:

1.  In your store's Admin area, go to the Taxes section (**Store setup** > **Taxes**).
    ![xc5_taxes_vat_taxes_section.png]({{site.baseurl}}/attachments/ref_hxmof6xX/xc5_taxes_vat_taxes_section.png?effects=drop-shadow)
    
2.  Make sure you are viewing the **Canadian taxes** tab.
    ![xc5_taxes_canada_canadian_taxes_tab.png]({{site.baseurl}}/attachments/ref_hxmof6xX/xc5_taxes_canada_canadian_taxes_tab.png?effects=drop-shadow)

3.  Configure the tax options in the **Common tax settings** section:
    ![xc5_taxes_canada_common_settings.png]({{site.baseurl}}/attachments/ref_hxmof6xX/xc5_taxes_canada_common_settings.png)

    *   Specify whether tax calculation rules (we'll come to configuring these rules a bit later) should be the same for all your store's users, irrespective of their membership, or should be different depending on the users' membership. If the rules need to be the same for all your buyers, enable the option **Use the same tax rates for all user membership levels** by selecting the respective check box. If different membership levels need the taxes to be calculated differently, leave this check box unselected.
    
    *   Use the selectbox titled **Address for Canadian taxes calculation** to specify the address type based on which your taxes need to be calculated. The available options here are _Shipping address_ and _Billing address._ The address type you select here will be used to determine the customer's zone, which in its turn will be used to determine the tax rate that needs to be applied. For example, to charge tax based on where the product is being shipped to (not where it was purchased), you would need to choose the _Shipping address_ option in this field.
    
    *   **Taxable base**
    
    *   **GST rate (%)**
    
    *   X-Cart can display product prices with the label 'inc VAT' or 'ex VAT' displayed next to them - depending on whether VAT / GST is included into the price or not. Use the setting **Display 'inc/ex VAT' labels next to prices** to specify, whether you want to use such labels, and if so, on which pages the labels should be shown. 




_Related pages:_

*   {% link "Setting up tax classes" ref_pAWOdG8N %}
*   {% link "Assigning tax classes to products" ref_pAWOdG8N#assigning-tax-classes-to-products %}
*   {% link "Setting up destination (address) zones" ref_r68iO5Rm %}
*   {% link "Adding user membership levels" ref_9ITFspcC %}
*   {% link "Setting up sales tax" ref_aJPK4DHN %}
*   {% link "Setting up VAT with the module "EU and UK VAT / GST"" ref_wcorpZyz %}
  