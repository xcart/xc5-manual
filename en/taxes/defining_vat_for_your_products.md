---
identifier: ref_HkDXZBRO
updated_at: 2015-03-11 00:00
layout: article_with_sidebar
lang: en
title: 'Defining VAT for your products'
categories:
  - User manual

---


[VAT (Value added tax)](http://en.wikipedia.org/wiki/Value_added_tax#With_a_value_added_tax) is a type of tax that is already included into the product price shown to the customer. Even though the tax value is already added to the price, you may want to set up VAT in your store for correct picture of your sales/revenue and for correct work with ERP systems such as Quickbooks.

This article describes the process of setting up VAT taxes in your X-Cart 5 and consists of three parts:

1.  Understanding what is product class, whether you need it and how to create it
2.  Defining VAT settings
3.  Creating VAT rates

Before you get started, make sure that you have the **VAT** module installed and activated. If not, you should install it according to {% link "instruction in our Knowledge base" ref_FBqE6f5B %}.

![]({{site.baseurl}}/attachments/6389863/6586573.png)

Finally, the process of creating VAT system relies on understanding what is {% link "destination zones" ref_BR33Qe4e %} and what is user memberships. Check the manual if you are not sure about these terms.

# Video tutorial

<iframe class="youtube-player" type="text/html" style="width: 800px; height: 450px" src="http://www.youtube.com/embed/kCS54G0QvvU" frameborder="0"></iframe>

# Understanding what is product class, whether you need it and how to create it

The description of what is tax class and how to define them if you need custom ones is explained in the {% link "Setting up tax classes" ref_5Mr9DJPu %} article. Check it for more information.

# Defining VAT settings

Before you set up VAT rates, you need to decide how you want to display VATs to customers.

1.  Go to **Store setup > Taxes > VAT** section in your admin area  
    ![]({{site.baseurl}}/attachments/6389863/6586574.png)
2.  Define VAT title and enable VAT system itself  

    ![]({{site.baseurl}}/attachments/6389863/6586575.png)
3.  Decide whether you want to display product prices including VAT on catalog pages (categories, search, etc). If you do, tick the corresponding option on.  
    ![]({{site.baseurl}}/attachments/6389863/6586576.png)
4.  Decide whether you want to display **including VAT **labels near the prices. You can choose to never show these labels (**Never**), to show them on product details pages only (**On product details only**) or to show them on all relevant pages (**On all catalog pages**).  

    ![]({{site.baseurl}}/attachments/6389863/6586577.png)
5.  Your VAT is included into the product price and you must decide what type of customers this VAT is defined for. For instance, your prices are defined with the assumption that your products will be bought by UK customers with no membership. In this case you set up the following fields as  
    ![]({{site.baseurl}}/attachments/6389863/6586578.png)  
    Of course, if you define different VAT rates for non-UK customers and/or with another membership, then the module will take the product price, subtract VAT rate for no-membership/UK customer and add VAT rate for this customer type.
6.  Once you are done with VAT setting, click the **Save changes** button at the bottom.  
    ![]({{site.baseurl}}/attachments/6389863/6586579.png)

# Creating VAT rates

 Final step in creating VAT system is creating VAT rates. Creating VAT rates process is quite straight-forward. 

1.  In the **VAT** section click the **New rate** button.  
    ![]({{site.baseurl}}/attachments/6389863/6586580.png)
2.  Choose **Tax class**, **User membership** and **Destination zone** parameters for the VAT rate you are specifying and define the **VAT rate** itself in the result line.  
    ![]({{site.baseurl}}/attachments/6389863/6586581.png)
3.  Add some other VAT rates if needed and click the **Save changes** button.  
    ![]({{site.baseurl}}/attachments/6389863/6586582.png)

## Attachments:

![](images/icons/bullet_blue.gif) [vat-icon.png]({{site.baseurl}}/attachments/6389863/6586573.png) (image/png)  
![](images/icons/bullet_blue.gif) [vat-section-admin.png]({{site.baseurl}}/attachments/6389863/6586574.png) (image/png)  
![](images/icons/bullet_blue.gif) [vat-title-admin.png]({{site.baseurl}}/attachments/6389863/6586575.png) (image/png)  
![](images/icons/bullet_blue.gif) [display-vat-in-catalog.png]({{site.baseurl}}/attachments/6389863/6586576.png) (image/png)  
![](images/icons/bullet_blue.gif) [display-vat-prices-setting.png]({{site.baseurl}}/attachments/6389863/6586577.png) (image/png)  
![](images/icons/bullet_blue.gif) [product-prices-defined-based-on.png]({{site.baseurl}}/attachments/6389863/6586578.png) (image/png)  
![](images/icons/bullet_blue.gif) [save-vat-settings-changes.png]({{site.baseurl}}/attachments/6389863/6586579.png) (image/png)  
![](images/icons/bullet_blue.gif) [new-rate-button-admin.png]({{site.baseurl}}/attachments/6389863/6586580.png) (image/png)  
![](images/icons/bullet_blue.gif) [vat-rate-1.png]({{site.baseurl}}/attachments/6389863/6586581.png) (image/png)  
![](images/icons/bullet_blue.gif) [var-rates-admin.png]({{site.baseurl}}/attachments/6389863/6586582.png) (image/png)