---
identifier: ref_quEqZzq1
updated_at: 2015-05-26 00:00
layout: article_with_sidebar
lang: en
title: 'How AvaTax Sales Tax Automation works'
categories:
  - User manual

---


 The two main functions provided by the AvaTax Sales Tax Automation module are address validation and sales tax calculation.

## Address validation

Address validation is provided both in the Customer and Admin areas of the online store. 

In the Customer area, address validation is performed:

*   in the Address book of a customer user profile - when an address is saved or updated:

![]({{site.baseurl}}/attachments/8749288/8717984.png?effects=drop-shadow)

*   on the checkout page - when a customer clicks the **Check address** button:

![]({{site.baseurl}}/attachments/8749288/8717983.png?effects=drop-shadow)

(If the customer chooses to place their order without clicking the** Check address** button first, their address is not validated.)

In the Admin area, address validation is performed only when the store administrator saves or updates an address in a customer's Address book:

![]({{site.baseurl}}/attachments/8749288/8717987.png?effects=drop-shadow)

For address validation, an address validation call is made to AvaTax. AvaTax performs validation of the address and returns results to the X-Cart store.

If the input address data can be resolved successfully, a normilized address is returned:

*   The original address is automatically corrected for spelling errors and inaccurate street names.
*   The postal code may be updated to provide more accuracy (For example, for addresses in the United States, a five-digit zip code may be replaced with a nine-digit code in the "Zip+4" format). 

If the address submitted to AvaTax for validation contains ambiguous data that cannot be resolved, an error is returned, and a message indicating the problem is displayed at the top of the page in X-Cart. For example, the screenshot below demonstrates a message resulting from an attempt to validate an erroneous street address:

![]({{site.baseurl}}/attachments/8749288/8717556.png?effects=drop-shadow)

## Sales tax calculation

Sales tax automation for orders at your X-Cart store falls back on Avalara's extensive database of taxability data for different taxing jurisdictions. X-Cart's AvaTax Sales Tax Automation module allows your store to connect to Avalara's AvaTax engine to determine the taxing jurisdiction to which the sale transaction pertains based on the address data provided and have the appropriate product taxability rules applied to the products being purchased. 

The product taxability rules in AvaTax system are associated with specific products in your X-Cart store via tax codes. Depending on your AvaTax subscription plan, you may be able to use hundreds of thousands of pre-defined AvaTax system tax codes or define your own custom tax codes. 

When sales tax calculation needs to be performed, the module passes on to AvaTax all the information it requires to do the calculation. AvaTax uses this information to determine the necessary taxing jurisdiction and select the taxing rules that need to be applied. The results of sales tax calculation for an order are provided directly on the checkout page before the order is placed:

![]({{site.baseurl}}/attachments/8749288/8717988.png?effects=drop-shadow)  

_Related pages:_

*   {% link "AvaTax Sales Tax Automation module: system requirements and installation" ref_7sCnJ9Fn %}
*   {% link "Getting started with AvaTax Sales Tax Automation" ref_hqOqXrfu %}
*   {% link "Configuring the AvaTax Sales Tax Automation module" ref_e7Bik73T %}
*   {% link "Mapping products to AvaTax tax codes" ref_OxmufIdA %}
*   {% link "Managing sales tax exemption for customers (AvaTax settings)" ref_Zt2I0fgM %}

## Attachments:

![](images/icons/bullet_blue.gif) [avatax_wrong_address.png]({{site.baseurl}}/attachments/8749288/8717982.png) (image/png)  
![](images/icons/bullet_blue.gif) [avatax_wrong_address1.png]({{site.baseurl}}/attachments/8749288/8717557.png) (image/png)  
![](images/icons/bullet_blue.gif) [avatax_wrong_address.png]({{site.baseurl}}/attachments/8749288/8717556.png) (image/png)  
![](images/icons/bullet_blue.gif) [avatax_check_address_button.png]({{site.baseurl}}/attachments/8749288/8717983.png) (image/png)  
![](images/icons/bullet_blue.gif) [avatax_address_validation_address_book0.png]({{site.baseurl}}/attachments/8749288/8717984.png) (image/png)  
![](images/icons/bullet_blue.gif) [avatax_address_validation_address_book.png]({{site.baseurl}}/attachments/8749288/8717985.png) (image/png)  
![](images/icons/bullet_blue.gif) [avatax_address_validation_address_book_a.png]({{site.baseurl}}/attachments/8749288/8717986.png) (image/png)  
![](images/icons/bullet_blue.gif) [avatax_address_validation_address_book_a0.png]({{site.baseurl}}/attachments/8749288/8717987.png) (image/png)  
![](images/icons/bullet_blue.gif) [avatax_tax_calculation.png]({{site.baseurl}}/attachments/8749288/8717988.png) (image/png)  
![](images/icons/bullet_blue.gif) [avatax_code_field.png]({{site.baseurl}}/attachments/8749288/8717989.png) (image/png)