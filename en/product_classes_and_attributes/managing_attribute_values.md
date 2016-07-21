---
identifier: ref_uKVHuBU6
updated_at: 2015-08-28 00:00
layout: article_with_sidebar
lang: en
title: 'Managing attribute values'
categories:
  - User manual

---


This page covers the following topics:

*   {% link "attribute value field types" ref_uKVHuBU6 %} supported by X-Cart 5;
*   how to specify product options through the use of {% link "multi-value attributes" Managing-attribute-values_7504859.html %};
*   how to allow {% link "personalization options" Managing-attribute-values_7504859.html %} for products (i.e. provide an editable text area on the product page on the storefront so buyers can use it to enter their own custom text; for example, a monogram);
*   how to set up product options as {% link "price and weight modifiers" Managing-attribute-values_7504859.html %} so that the price and/or weight of the product will change depending on the product options selected by the buyer;
*   how to {% link "set one of the defined attribute values as default" Managing-attribute-values_7504859.html %}.

# Attribute value field types

X-Cart supports three field types for attribute values:

*   {% link "Plain field" Managing-attribute-values_7504859.html %}
*   {% link "Textarea" Managing-attribute-values_7504859.html %}
*   {% link "Yes/No" Managing-attribute-values_7504859.html %}

When configuring an attribute, select the field type that best suits your needs. Below we provide detailed explanation of each type.

### Plain field

Choose this field type if you need the attribute value to be a word/phrase of your choice. You can use _Plain field_ to specify such properties of a product as color, size, ISBN (for books), etc.: it is good foor almost anything, provided you can describe it in a couple of words. For example, we used it to specify the dimensions of a bag:

![]({{site.baseurl}}/attachments/7504859/8719327.png?effects=drop-shadow)

On the storefront, it shows as follows:

![]({{site.baseurl}}/attachments/7504859/7602527.png?effects=drop-shadow)

Note that this field type can be used to specify multiple values for one attribute. For details, see {% link "Multi-value attributes (product options)" Managing-attribute-values_7504859.html %}.

### Textarea

This field type allows for a longer text length than _Plain field_ and can be used to provide lengthier descriptions. For example, we used it to add detailed information about the fabric and cut of a women's top:

![]({{site.baseurl}}/attachments/7504859/8719328.png?effects=drop-shadow)

On the storefront, it shows as follows:

![]({{site.baseurl}}/attachments/7504859/7602525.png?effects=drop-shadow)

Starting with X-Cart 5.1, the _Textarea_ attribute value field type can be used to add personalization options for products (i.e. provide an editable text area on the product page on the storefront so buyers can use it to enter their own custom text). For details, see {% link "Personalization options" Managing-attribute-values_7504859.html %}.

### **Yes/No**

This field type is intended for attribute values that emphasize the presence or absence of some property or feature. For example, we used it to emphasize the wirelessness of the headphones:

![]({{site.baseurl}}/attachments/7504859/8719329.png?effects=drop-shadow)

On the storefront, it looks like this:

![]({{site.baseurl}}/attachments/7504859/7602541.png?effects=drop-shadow)

Note that the _Yes/No_ field type can also be used to specify "Yes or No" options for products. For details, see {% link "Multi-value attributes (product options)" Managing-attribute-values_7504859.html %}.

# Multi-value attributes (product options)

The _Plain text_ and _Yes/No_ attribute value field types allow you to use the **_multi-value_** feature, i.e. to specify multiple values for one attribute. In X-Cart 5 this feature is used to specify the product options that customers will be able to choose. For example, you can use _Plain field_ attribute values to provide information about the available sizes of a garment. Specific sizes like XS, S, M and L can be made into product options if you add them as values for the attribute "Size" like so:

![]({{site.baseurl}}/attachments/7504859/8719330.png?effects=drop-shadow)

On the storefront, it shows as follows:

![]({{site.baseurl}}/attachments/7504859/7602532.png?effects=drop-shadow)

Note how the attribute values XS, S, M and L have become product options that buyers can choose from a drop-down list before adding the product to their cart.

To achieve this setup:

1.  Use the **Attribute option** field next to the attribute name to enter the attribute value that should go first in your list of values for the attribute (In our example, we simply typed in "XS").
2.  Hover your cursor over the blank area to the right of the** Attribute option** field. This reveals a check box that says **_multi value_**:  
    ![]({{site.baseurl}}/attachments/7504859/8719331.png?effects=drop-shadow)
3.  Select this check box to enable multiple values for the attribute you are editing. A new empty line is added to the attribute values list:  
    ![]({{site.baseurl}}/attachments/7504859/8719332.png?effects=drop-shadow)
4.  Use the **Attribute option** field on the new line to type in the next attribute value name. As soon as you start typing, another empty line will be added to the list:  
    ![]({{site.baseurl}}/attachments/7504859/8719333.png?effects=drop-shadow)
5.  Continue until you have added all the attribute values you require.
6.  Choose whether you want to apply the changes locally or globally.
7.  Click **Save changes**.

With the _Yes/No_ field type, it is quite similar; the only difference is that there are just two options, _Yes_ and _No_, and you do not have to type them manually, but can select them from a list.

![]({{site.baseurl}}/attachments/7504859/8719334.png?effects=drop-shadow)

On the storefront, customers can choose the option they require by adjusting the respective check box:

![]({{site.baseurl}}/attachments/7504859/7602537.png?effects=drop-shadow)

It should be noted that the method for specifying product options described above does not provide a way to track how many product units with a specific option you have sold and how many you still have on hand. Also, if the product has more than one multi-valued attribute, there is no way to specify, which option combinations (product variants) are actually available. If you need these features, consider installing X-Cart's [Product Variants](http://www.x-cart.com/extensions/addons/product-variants.html) module. This module allows you to create product variants from options and make them have their own prices, SKUs and stock levels.

# Personilization options (editable Textarea)

Starting with X-Cart 5.1, it is possible to add _**editable**_ _Textarea_ attribute values. Adding an editable attribute value  for some product attribute creates an empty editable text area field on the product page where buyers can enter their own custom text before adding the product to their shopping cart. This feature may be used if you are going to provide personalization options for products, like monogramming, embroidery, etc.

To add a _Textarea_ attribute value as editable, you need to leave the **Attribute option** field empty and select the **_editable_** check box next to it before saving the changes (The check box is hidden and is revealed only when you hover your cursor over the blank area to the right of the **Attribute option** field).

The snapshot below provides an example of how an editable text area attribute value can be used to allow customers to enter custom monogram text for a bath towel:

![]({{site.baseurl}}/attachments/7504859/8719335.png?effects=drop-shadow)

On the storefront, it looks like this:

![]({{site.baseurl}}/attachments/7504859/7602536.png?effects=drop-shadow)

# Price and weight modifiers

Attribute values for multi-value product attributes can be configured as _price and/or weight modifier_ options that will increase or decrease the price and/or weight of the product (the product's weight affects the shipping cost). 

Here's an example of a price modifier option that allows customers purchasing a towel to add a monogram for an additional $10 per unit:

![]({{site.baseurl}}/attachments/7504859/8719336.png?effects=drop-shadow)

Here's what it looks like on the storefront:

![]({{site.baseurl}}/attachments/7504859/7602577.png?effects=drop-shadow)

Notice how the price of the product changes when the check box "Monogram this item? (+ $10.00)" is selected:

![]({{site.baseurl}}/attachments/7504859/7602579.png?effects=drop-shadow)

To configure attribute values as price/weight modifiers:

1.  Hover your cursor over the field displaying the attribute value that you want to make a price modifier. For example, we want the option "Monogram this item?.....Yes" to have the price of $10, so we hover over the attriibute value "Yes". A link titled **<u>Modifiers</u>** is revealed:  
    ![]({{site.baseurl}}/attachments/7504859/8719337.png?effects=drop-shadow)
2.  Click on the <u>**Modifiers**</u> link. This displays a popup panel allowing you to specify the price and/or weight by which this option will alter the product's price and/or weight:  
    ![]({{site.baseurl}}/attachments/7504859/8719338.png?effects=drop-shadow)
3.  Use the **Price** and/or **Weight** field(s) on the popup panel to specify the modifier values you require. These can be In our case, we need to specify the price modifier:  
    ![]({{site.baseurl}}/attachments/7504859/8719339.png?effects=drop-shadow)
4.  Choose whether you want to apply the changes locally or globally.
5.  Click **Save changes**:  
    ![]({{site.baseurl}}/attachments/7504859/8719340.png?effects=drop-shadow)  
    The settings will be saved.

# Setting the default attribute value

When configuring multi-value attributes, you can control which of the attribute values should be shown to customers by default.

To set the default attribute value:

1.  Hover your cursor over the field displaying the attribute value that you want to make the default one. For example, we want the option "Monogram this item?.....No" to be available to users by default, so we hover over the attriibute value "No". A link titled **<u>Modifiers</u>** is revealed:  
    ![]({{site.baseurl}}/attachments/7504859/8719341.png?effects=drop-shadow)
2.  Click on the <u>**Modifiers**</u> link. This displays a popup panel:  
    ![]({{site.baseurl}}/attachments/7504859/8719342.png?effects=drop-shadow)
3.  Select the _Default option_ check box:  
    ![]({{site.baseurl}}/attachments/7504859/8719343.png?effects=drop-shadow)
4.  Choose whether you want to apply the changes locally or globally. We want to make the value "Monogram this item?.....No" default for the entire product class "Towels", so we selected the option "Apply value changes globally":  
    ![]({{site.baseurl}}/attachments/7504859/8719345.png?effects=drop-shadow)
5.  Click **Save changes**.  
    The settings will be saved.

_Related pages:_

*   {% link "Product classes and attributes" ref_F1TNi0gL %}
*   {% link "Types of product attributes - by scope" ref_UdUa8HcM %}

## Attachments:

![](images/icons/bullet_blue.gif) [textarea_admin.png]({{site.baseurl}}/attachments/7504859/7602524.png) (image/png)  
![](images/icons/bullet_blue.gif) [textarea_storefront.png]({{site.baseurl}}/attachments/7504859/7602525.png) (image/png)  
![](images/icons/bullet_blue.gif) [plain_field_admin.png]({{site.baseurl}}/attachments/7504859/7602526.png) (image/png)  
![](images/icons/bullet_blue.gif) [plain_field_storefront.png]({{site.baseurl}}/attachments/7504859/7602527.png) (image/png)  
![](images/icons/bullet_blue.gif) [plain_field_multi_value1.png]({{site.baseurl}}/attachments/7504859/7602528.png) (image/png)  
![](images/icons/bullet_blue.gif) [plain_field_multi_value2.png]({{site.baseurl}}/attachments/7504859/7602529.png) (image/png)  
![](images/icons/bullet_blue.gif) [plain_field_multi_value.png]({{site.baseurl}}/attachments/7504859/7602531.png) (image/png)  
![](images/icons/bullet_blue.gif) [plain_field_multi_value.png]({{site.baseurl}}/attachments/7504859/7602530.png) (image/png)  
![](images/icons/bullet_blue.gif) [plain_field_multi_value_storefront.png]({{site.baseurl}}/attachments/7504859/7602533.png) (image/png)  
![](images/icons/bullet_blue.gif) [plain_field_multi_value_storefront.png]({{site.baseurl}}/attachments/7504859/7602532.png) (image/png)  
![](images/icons/bullet_blue.gif) [plain_field_multi_value3.png]({{site.baseurl}}/attachments/7504859/7602534.png) (image/png)  
![](images/icons/bullet_blue.gif) [editable_textarea_admin.png]({{site.baseurl}}/attachments/7504859/7602535.png) (image/png)  
![](images/icons/bullet_blue.gif) [editable_textarea_storefront.png]({{site.baseurl}}/attachments/7504859/7602536.png) (image/png)  
![](images/icons/bullet_blue.gif) [yes_no_multi_storefront.png]({{site.baseurl}}/attachments/7504859/7602538.png) (image/png)  
![](images/icons/bullet_blue.gif) [yes_no_multi_storefront.png]({{site.baseurl}}/attachments/7504859/7602576.png) (image/png)  
![](images/icons/bullet_blue.gif) [yes_no_multi_admin.png]({{site.baseurl}}/attachments/7504859/7602539.png) (image/png)  
![](images/icons/bullet_blue.gif) [yes_no_single_admin.png]({{site.baseurl}}/attachments/7504859/7602542.png) (image/png)  
![](images/icons/bullet_blue.gif) [yes_no_single_storefront.png]({{site.baseurl}}/attachments/7504859/7602541.png) (image/png)  
![](images/icons/bullet_blue.gif) [yes_no_single_admin.png]({{site.baseurl}}/attachments/7504859/7602540.png) (image/png)  
![](images/icons/bullet_blue.gif) [price_modifier.png]({{site.baseurl}}/attachments/7504859/7602575.png) (image/png)  
![](images/icons/bullet_blue.gif) [yes_no_multi_storefront.png]({{site.baseurl}}/attachments/7504859/7602537.png) (image/png)  
![](images/icons/bullet_blue.gif) [price_modifier_storefront.png]({{site.baseurl}}/attachments/7504859/7602578.png) (image/png)  
![](images/icons/bullet_blue.gif) [price_modifier_storefront.png]({{site.baseurl}}/attachments/7504859/7602580.png) (image/png)  
![](images/icons/bullet_blue.gif) [price_modifier_storefront1.png]({{site.baseurl}}/attachments/7504859/7602579.png) (image/png)  
![](images/icons/bullet_blue.gif) [price_modifier_storefront.png]({{site.baseurl}}/attachments/7504859/7602577.png) (image/png)  
![](images/icons/bullet_blue.gif) [price_modifier1.png]({{site.baseurl}}/attachments/7504859/7602581.png) (image/png)  
![](images/icons/bullet_blue.gif) [price_modifier2.png]({{site.baseurl}}/attachments/7504859/7602582.png) (image/png)  
![](images/icons/bullet_blue.gif) [price_modifier3.png]({{site.baseurl}}/attachments/7504859/7602583.png) (image/png)  
![](images/icons/bullet_blue.gif) [price_modifier4.png]({{site.baseurl}}/attachments/7504859/7602584.png) (image/png)  
![](images/icons/bullet_blue.gif) [default_attr_value.png]({{site.baseurl}}/attachments/7504859/7602585.png) (image/png)  
![](images/icons/bullet_blue.gif) [default_attr_value1.png]({{site.baseurl}}/attachments/7504859/7602586.png) (image/png)  
![](images/icons/bullet_blue.gif) [default_attr_value2.png]({{site.baseurl}}/attachments/7504859/7602587.png) (image/png)  
![](images/icons/bullet_blue.gif) [default_attr_value3.png]({{site.baseurl}}/attachments/7504859/7602588.png) (image/png)  
![](images/icons/bullet_blue.gif) [default_attr_value4.png]({{site.baseurl}}/attachments/7504859/7602590.png) (image/png)  
![](images/icons/bullet_blue.gif) [default_attr_value4.png]({{site.baseurl}}/attachments/7504859/7602589.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_bag_dimensions.png]({{site.baseurl}}/attachments/7504859/8719327.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_boho_top.png]({{site.baseurl}}/attachments/7504859/8719328.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_headphones_wireless_yes.png]({{site.baseurl}}/attachments/7504859/8719329.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_apparel_sizes.png]({{site.baseurl}}/attachments/7504859/8719330.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_multi_value.png]({{site.baseurl}}/attachments/7504859/8719331.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_new_blank_multi_value_line.png]({{site.baseurl}}/attachments/7504859/8719332.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_another_blank_multi_value_line.png]({{site.baseurl}}/attachments/7504859/8719333.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_monogram_multi_value.png]({{site.baseurl}}/attachments/7504859/8719334.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_editable_textarea.png]({{site.baseurl}}/attachments/7504859/8719335.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_price_modifier_10.png]({{site.baseurl}}/attachments/7504859/8719336.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_modifier_link.png]({{site.baseurl}}/attachments/7504859/8719337.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_modifiers_setup.png]({{site.baseurl}}/attachments/7504859/8719338.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_modifiers_setup1.png]({{site.baseurl}}/attachments/7504859/8719339.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_towel_save.png]({{site.baseurl}}/attachments/7504859/8719340.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_modifier_link1.png]({{site.baseurl}}/attachments/7504859/8719341.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_modifiers_setup2.png]({{site.baseurl}}/attachments/7504859/8719344.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_modifiers_setup3.png]({{site.baseurl}}/attachments/7504859/8719343.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_modifiers_setup2.png]({{site.baseurl}}/attachments/7504859/8719342.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_modifier_globally.png]({{site.baseurl}}/attachments/7504859/8719345.png) (image/png)