---
identifier: ref_VL5PeU5w
updated_at: 2015-08-28 00:00
layout: article_with_sidebar
lang: en
title: 'Managing global attributes'
categories:
  - User manual

---


This page provides information on the following actions with global attributes:

*   {% link "Adding global attributes" ref_VL5PeU5w %};
*   {% link "Viewing your store's list of global attributes" Managing-global-attributes_7504857.html %};
*   {% link "Assigning global attributes to products" Managing-global-attributes_7504857.html %};
*   {% link "Viewing a product's global attributes" Managing-global-attributes_7504857.html %};
*   {% link "Editing global attributes" Managing-global-attributes_7504857.html %};
*   {% link "Deleting global attributes" Managing-global-attributes_7504857.html %}.

# Adding global attributes

X-Cart supports two methods of adding global attributes. Below, we will show how to add a global attribute "Color".

**Method 1:**

When using this method, you configure global attributes via the Classes & attributes section (**Catalog > Classes & attributes**) of the Admin area.

The process is as follows:

1.  In your store's Admin area, go to the Classes & attributes section (**Catalog > Classes & attributes**).
2.  Click on the <u>Edit attributes (N)</u> link opposite the **Global attributes** title:  
    ![]({{site.baseurl}}/attachments/7504857/8719294.png?effects=drop-shadow)  
    This opens a page where you will be able to manage global attributes:  
    ![]({{site.baseurl}}/attachments/7504857/8719295.png?effects=drop-shadow)
3.  On this page, click **New attribute**:  
    ![]({{site.baseurl}}/attachments/7504857/8719296.png?effects=drop-shadow)  
    A popup titled **New attribute** appears:  
    ![]({{site.baseurl}}/attachments/7504857/8719297.png?effects=drop-shadow)
4.  Use the fields of the **New attribute** popup to provide information about the new attribute. Specify the following information:  

    *   **Attribute**: Attribute name.
    *   **Attribute group**: (Specify this if you want to assign the new attribute to some attribute group) Name of the attribute group.
    *   **Type**: Attribute value type (_Plain field_, _Textarea_, _Yes/No_).![]({{site.baseurl}}/attachments/7504857/8719298.png?effects=drop-shadow)
5.  Click **Next**. The attribute should be saved. Now the popup is expanded so you can edit attribute values:  
    ![]({{site.baseurl}}/attachments/7504857/8719299.png?effects=drop-shadow)
6.  Configure the attribute values you require (See [Managing attribute values](http://kb.x-cart.com/display/XDD/Managing+attribute+values) for more info). In our example, we need to add values for the attribute "Color"; these will be "Orange", "Blue", etc - we simply need to name all the colors for all the products that will use this global attribute. The snapshot below demonstrates adding the value "Orange":   
    ![]({{site.baseurl}}/attachments/7504857/8719300.png?effects=drop-shadow)
7.  If you want some or all of the value(s) you added for this global attribute to be applied automatically to all the products that will be added to your store's catalog in future, click the Check mark icon(s) opposite the names of these attribute values (the Check mark icons should turn green):   
    ![]({{site.baseurl}}/attachments/7504857/8719301.png?effects=drop-shadow)
8.  Once you're done editing the attribute values, save the changes using the **Save changes** button:  
    ![]({{site.baseurl}}/attachments/7504857/8719302.png?effects=drop-shadow)  
    The attribute value(s) should be saved.   

    You have added a global attribute "Color". If at step 7 you chose to enable the Check mark icon for any attribute values, these values will be assigned automatically to all new products that will be created in your store. Any products that already existed before you saved the new attribute values will not get these values automatically; if you need the new attribute values to be assigned to existing products as well, you can visit the **Attributes** tab of such products and assign the attribute values you require manually (You can also use the "Apply value changes globally" feature to assign attribute values globally to all the existing products) .

**Method 2:**

When using this method, you edit the details of some product and add global attributes via the **Attributes** tab of its details page. 

The process is as follows:

1.  In your store's Admin area, open the deails of any product that needs to be assigned a new global attribute and click on the** Attributes** tab:  
    ![]({{site.baseurl}}/attachments/7504857/8719303.png?effects=drop-shadow)  
    This will open a page where you can manage attributes for this product. 
2.  Click on the <u style="font-size: 14.0px;line-height: 1.4285715;">Global</u> link at the top of the page to access the subsection where you can add and assign global and "product class"-level attributes to this product:  
    ![]({{site.baseurl}}/attachments/7504857/8719304.png?effects=drop-shadow)  
    On the page that opens there will be the **Global attributes** section where you will add new attributes on the global level:  
    ![]({{site.baseurl}}/attachments/7504857/8719305.png?effects=drop-shadow)  

3.  Use the **Global attributes** section to add information about the new attribute:
    1.  Create a new empty entry in the attributes list (This is where you will specify your attribute name and value(s)): click the "down arrow" part of the **Add attribute** button and select the type of attribute value you require (_Plain field_, _Textarea_ or _Yes/No_) from the drop-down button menu.   
        ![]({{site.baseurl}}/attachments/7504857/8719306.png?effects=drop-shadow)  
        (For an explanation of the different attribute value field types, see [Managing attribute values](http://kb.x-cart.com/display/XDD/Managing+attribute+values)).   
        As we are going to add the attribute  "Color" with values like "Orange", "Blue", etc., we should select the attribute value type "_Plain field_". "_Plain field_" is the default value, so we don't even need to use the drop-down menu: simply clicking **Add attribute** will create the empty fields we require:  
        ![]({{site.baseurl}}/attachments/7504857/8719307.png)  

    2.  Use the **Attribute name** and **Attribute option** fields to specify, respectively, the attribute name and value(s):  
        ![]({{site.baseurl}}/attachments/7504857/8719308.png?effects=drop-shadow)  

    3.  Choose whether you want to apply the changes you made locally or globally:  

        *   Apply value changes globally => Changes of attribute values will apply for all the products in your store.
        *   Apply value changes locally => Changes of attribute values will affect only this product. Changes of attribute names and of the attribute list (for example, changes of the order of attributes in the list, or removal of attributes) will affect all the products in your store.For example, choosing to apply globally the attribute value "Orange" that we added for the attribute "Color" (see the snapshot below) will result in that all the products in your store will have the attribute "Color..........Orange" in their Specification.   
        ![]({{site.baseurl}}/attachments/7504857/8719309.png?effects=drop-shadow)  
        Note that when you apply attribute values globally, they are applied only to products that exist in the store's catalog at the time you save the changes. Any products that will be created at a later time will _not_ get these values automatically.
    4.  Click the **Save changes** button at the bottom of the screen:  
        ![]({{site.baseurl}}/attachments/7504857/8719310.png?effects=drop-shadow)  

        The attribute will be added:  
        ![]({{site.baseurl}}/attachments/7504857/8719311.png?effects=drop-shadow)  
        Now if you view the product on the storefront,  the Specification tab on its details page will show the attribute "Color..........Orange". If at step 4c you chose to apply the attribute value "Orange" globally, all the products in your store will show the same attribute as well. If you kept the option "Apply value changes locally", the attribute value "Orange" will be applied only for the product you edited (However, you will be able to find "Orange" in the list of attribute values for the attribute "Color" and apply it to other products in your store manually).

# Viewing your store's list of global attributes

To view your store's global attributes:

1.  In your store's Admin area, go to the Classes & attributes section (**Catalog > Classes & attributes**).
2.  Click on the <u>Edit attributes (N)</u> link opposite the **Global attributes** title:  
    ![]({{site.baseurl}}/attachments/7504857/8719313.png?effects=drop-shadow)  
    This opens a page with your store's global attributes list:  
    ![]({{site.baseurl}}/attachments/7504857/8719314.png?effects=drop-shadow)

In the list of global attributes, for each attribute you can see the attribute name and the field type that was used to add the attribute's values. 

To view the values for a specific attribute:

1.  Hover your cursor over the line with the attribute's name. This will display an **Edit** button opposite the attribute's name:  
    ![]({{site.baseurl}}/attachments/7504857/8719315.png?effects=drop-shadow)
2.  Click the **Edit** button. This will display the attribute's details, including the list of its values:  
    ![]({{site.baseurl}}/attachments/7504857/8719316.png?effects=drop-shadow) 

## Assigning global attributes to products

After adding global attributes via the Classes & attributes section (**Catalog > Classes & attributes**), you need to assign these attributes to specific products.

In the following example, we will assign the global attribute "Color.....Orange" to the product named "12 oz. Plastic Cup, 100 count":

1.  In your store's Admin area, find the product to which you need to assign a global attribute, open its details and click on the** Attributes** tab:  
    ![]({{site.baseurl}}/attachments/7504857/8719303.png?effects=drop-shadow)  
    This will open a page where you can manage attributes for this product. 
2.  Click on the <u style="font-size: 14.0px;line-height: 1.4285715;">Global</u> link at the top of the page to access the subsection where you can add and assign global and "product class"-level attributes to this product:  
    ![]({{site.baseurl}}/attachments/7504857/8719304.png?effects=drop-shadow)  

3.  On the page that opens, scroll down to the **Global attributes** section and look at the list of attributes displayed in it:  
    ![]({{site.baseurl}}/attachments/7504857/8719319.png?effects=drop-shadow)  
    Here you can see the full list of your store's global attributes. The attributes for which the **Attribute option** field is empty are not yet assigned to the product and are not shown on the storefront. 
4.  For the attribute that needs to be assigned:
    *   click inside the **Attribute option **field and type in the value you require, or:
    *   click on the down arrow button at the right of the **Attribute option **field and select a previously configured attribute value from the drop-down list:   
        ![]({{site.baseurl}}/attachments/7504857/8719320.png?effects=drop-shadow)  
        We have selected the value "Orange". In the screenshot below you can see it displayed in the **Attribute option** field:  
        ![]({{site.baseurl}}/attachments/7504857/8719308.png?effects=drop-shadow)  
        If you have more global attributes that need to be assigned to the product, repeat this for each of them.  

5.  Choose whether you want to apply the selected attribute value(s) to this product only (select "Apply value changes locally") or to extend it/them to all the products of the same product class (select "Apply value changes globally").  
    ![]({{site.baseurl}}/attachments/7504857/8719309.png?effects=drop-shadow)  

6.  Click **Save changes**.  
    ![]({{site.baseurl}}/attachments/7504857/8719310.png?effects=drop-shadow)  
    The attribute(s) and their selected value(s) will be assigned to the product, after which you will be able to see them on the storefront.

# Viewing a product's global attributes

If a product has any global attributes assigned, you can view their list in the"Global attributes"section of the product's details (**Attributes** tab** >** **Global **subsection):

![]({{site.baseurl}}/attachments/7504857/8719308.png?effects=drop-shadow)  

# Editing global attributes

Sometimes you may need to change the name and/or values of a global attribute. You can do so using one of the following methods:

**Method 1:**

1.  In your store's Admin area, go to the Classes & attributes section (**Catalog > Classes & attributes**).
2.  Click on the <u>Edit attributes (N)</u> link opposite the **Global attributes** title:  
    ![]({{site.baseurl}}/attachments/7504857/8719313.png?effects=drop-shadow)  
    This opens a page where you will be able to manage your store's global attributes.
3.  In the list of global attributes, locate the attribute you need to edit and hover your cursor over its name. The **Attribute name** field will become visible and an **Edit** button will be displayed next to it:  
    ![]({{site.baseurl}}/attachments/7504857/8719315.png?effects=drop-shadow)
4.  If you just need to change the attribute name, click inside the **Attribute name** field and edit the attribute name as you require. If you need to change the attribute values (or both the attribute name and values), click the **Edit** button; this will open a popup titled **Edit attribute values** where you will be able make the necessary changes.
5.  If you want some or all of the attribute value(s) to be applied automatically to all the products that will be created in your store in future, be sure to "enable" the Check mark icon(s) opposite the names of these attribute values (the Check mark icons should turn green).
6.  Once you're done editing, click **Save changes**.

**Method 2:**

1.  In your store's Admin area, find the product for which you want to edit a global attribute (This can be any product that has this attribute: you will be able to extend the changes to the other products in your store), open its details and click on the** Attributes** tab.
2.  On the **Attributes** tab, click <u>Global</u>.
3.  On the page that opens, locate the **Global attributes** page section.
4.  Find the attribute you want to edit and make any changes you require:  

    *   To edit the attribute name, hover your cursor over it (the **Attribute name** field will become visible), click inside the **Attribute name** field and edit the attribute name as you require. 
    *   To edit the attribute values, edit the **Attribute value** field(s).  

5.  Specify whether you want to apply the changes globally or locally:  

    *   Apply value changes globally => Changes of attribute values will apply for all the products in your store.
    *   Apply value changes locally => Changes of attribute values will affect only this product. Changes of attribute names and of the attribute list (for example, changes of the order of attributes in the list, or removal of attributes) will affect all the products in your store.
6.  Click **Save changes**.

# Deleting global attributes

Sometimes you may need to delete a global attribute. You can do so using one of the following methods:

**Method 1:**

1.  In your store's Admin area, go to the Classes & attributes section (**Catalog > Classes & attributes**).
2.  Click on the <u>Edit attributes (N)</u> link opposite the **Global attributes** title.  
    This opens a page where you will be able to manage your store's global attributes.
3.  In the list of global attributes, locate the attribute you need to delete and click on the **Trash **icon opposite its name. The attribute will be marked for deletion.
4.  Click **Save changes**.  
    The attribute will be deleted from the list of your store's global attributes and will be removed from the details of all products.

**Method 2:**

1.  In your store's Admin area, find any product that has the global attribute you want to delete, open its details and click on the** Attributes** tab.
2.  On the **Attributes** tab, click <u>Global</u>.
3.  On the page that opens, scroll down to the **Global attributes** section.
4.  Find the attribute you want to delete and click on the **Trash** icon opposite its name. The attribute will be marked for deletion.
5.  It does not matter whether the option "Apply value changes globally" is selected or not: deleting a global attribute here will be applied globally in any case (The attribute will be deleted from the list of your store's global attributes and will be removed from the details of all products).
6.  Click **Save changes**.

_Related pages:_

*   {% link "Product classes and attributes" ref_F1TNi0gL %}
*   {% link "Types of product attributes - by scope" ref_UdUa8HcM %}

## Attachments:

![](images/icons/bullet_blue.gif) [new_global_attribute.png]({{site.baseurl}}/attachments/7504857/7602466.png) (image/png)  
![](images/icons/bullet_blue.gif) [add_global_attr.png]({{site.baseurl}}/attachments/7504857/7602504.png) (image/png)  
![](images/icons/bullet_blue.gif) [global_attributes.png]({{site.baseurl}}/attachments/7504857/7602505.png) (image/png)  
![](images/icons/bullet_blue.gif) [new_global_attribute1.png]({{site.baseurl}}/attachments/7504857/7602506.png) (image/png)  
![](images/icons/bullet_blue.gif) [new_global_attribute2.png]({{site.baseurl}}/attachments/7504857/7602507.png) (image/png)  
![](images/icons/bullet_blue.gif) [new_global_attribute3.png]({{site.baseurl}}/attachments/7504857/7602508.png) (image/png)  
![](images/icons/bullet_blue.gif) [new_global_attribute4.png]({{site.baseurl}}/attachments/7504857/7602509.png) (image/png)  
![](images/icons/bullet_blue.gif) [new_global_attribute5.png]({{site.baseurl}}/attachments/7504857/7602510.png) (image/png)  
![](images/icons/bullet_blue.gif) [global_attr_value_check_mark.png]({{site.baseurl}}/attachments/7504857/7602511.png) (image/png)  
![](images/icons/bullet_blue.gif) [new_global_attribute6.png]({{site.baseurl}}/attachments/7504857/7602512.png) (image/png)  
![](images/icons/bullet_blue.gif) [attr_tab.png]({{site.baseurl}}/attachments/7504857/7602513.png) (image/png)  
![](images/icons/bullet_blue.gif) [global_attr_subsection.png]({{site.baseurl}}/attachments/7504857/7602514.png) (image/png)  
![](images/icons/bullet_blue.gif) [global_attr_section.png]({{site.baseurl}}/attachments/7504857/7602515.png) (image/png)  
![](images/icons/bullet_blue.gif) [field_type_selector.png]({{site.baseurl}}/attachments/7504857/7602516.png) (image/png)  
![](images/icons/bullet_blue.gif) [new_global_attr.png]({{site.baseurl}}/attachments/7504857/7602517.png) (image/png)  
![](images/icons/bullet_blue.gif) [new_global_attr1.png]({{site.baseurl}}/attachments/7504857/7602518.png) (image/png)  
![](images/icons/bullet_blue.gif) [new_global_attr2.png]({{site.baseurl}}/attachments/7504857/7602519.png) (image/png)  
![](images/icons/bullet_blue.gif) [new_global_attr3.png]({{site.baseurl}}/attachments/7504857/7602520.png) (image/png)  
![](images/icons/bullet_blue.gif) [new_global_attr4.png]({{site.baseurl}}/attachments/7504857/7602521.png) (image/png)  
![](images/icons/bullet_blue.gif) [edit_global_attr.png]({{site.baseurl}}/attachments/7504857/7602522.png) (image/png)  
![](images/icons/bullet_blue.gif) [edit_global_attr1.png]({{site.baseurl}}/attachments/7504857/7602523.png) (image/png)  
![](images/icons/bullet_blue.gif) [global_attr_list.png]({{site.baseurl}}/attachments/7504857/7602547.png) (image/png)  
![](images/icons/bullet_blue.gif) [global_attr_list.png]({{site.baseurl}}/attachments/7504857/7602548.png) (image/png)  
![](images/icons/bullet_blue.gif) [global_attr_list.png]({{site.baseurl}}/attachments/7504857/7602546.png) (image/png)  
![](images/icons/bullet_blue.gif) [stores_global_attr_list.png]({{site.baseurl}}/attachments/7504857/7602549.png) (image/png)  
![](images/icons/bullet_blue.gif) [global_attr_values.png]({{site.baseurl}}/attachments/7504857/7602550.png) (image/png)  
![](images/icons/bullet_blue.gif) [assign_global_attributes.png]({{site.baseurl}}/attachments/7504857/7602571.png) (image/png)  
![](images/icons/bullet_blue.gif) [assign_global_attributes1.png]({{site.baseurl}}/attachments/7504857/7602573.png) (image/png)  
![](images/icons/bullet_blue.gif) [assign_global_attributes2.png]({{site.baseurl}}/attachments/7504857/7602574.png) (image/png)  
![](images/icons/bullet_blue.gif) [attr_tab1.png]({{site.baseurl}}/attachments/7504857/7602570.png) (image/png)  
![](images/icons/bullet_blue.gif) [global_attr_subsection1.png]({{site.baseurl}}/attachments/7504857/7602569.png) (image/png)  
![](images/icons/bullet_blue.gif) [attr_tab1.png]({{site.baseurl}}/attachments/7504857/7602568.png) (image/png)  
![](images/icons/bullet_blue.gif) [assign_global_attributes.png]({{site.baseurl}}/attachments/7504857/7602572.png) (image/png)  
![](images/icons/bullet_blue.gif) [assign_global_attributes.png]({{site.baseurl}}/attachments/7504857/7602559.png) (image/png)  
![](images/icons/bullet_blue.gif) [assign_global_attributes1.png]({{site.baseurl}}/attachments/7504857/7602560.png) (image/png)  
![](images/icons/bullet_blue.gif) [assign_global_attributes2.png]({{site.baseurl}}/attachments/7504857/7602561.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_edit_global_attr.png]({{site.baseurl}}/attachments/7504857/8719312.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_global_attr_page.png]({{site.baseurl}}/attachments/7504857/8719295.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_new_global_attr.png]({{site.baseurl}}/attachments/7504857/8719296.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_new_attr_popup.png]({{site.baseurl}}/attachments/7504857/8719297.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_color_global_attr.png]({{site.baseurl}}/attachments/7504857/8719298.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_edit_color_global_attr_values.png]({{site.baseurl}}/attachments/7504857/8719299.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_edit_color_global_attr_values1.png]({{site.baseurl}}/attachments/7504857/8719300.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_edit_color_global_attr_values2.png]({{site.baseurl}}/attachments/7504857/8719301.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_edit_color_global_attr_values3.png]({{site.baseurl}}/attachments/7504857/8719302.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_cup_attributes_tab.png]({{site.baseurl}}/attachments/7504857/8719317.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_cup_global_tab.png]({{site.baseurl}}/attachments/7504857/8719318.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_global_attributes_section.png]({{site.baseurl}}/attachments/7504857/8719305.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_add_attr.png]({{site.baseurl}}/attachments/7504857/8719306.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_new_blank_global.png]({{site.baseurl}}/attachments/7504857/8719307.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_global_color_orange.png]({{site.baseurl}}/attachments/7504857/8719321.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_color_globally.png]({{site.baseurl}}/attachments/7504857/8719322.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_color_globally_save.png]({{site.baseurl}}/attachments/7504857/8719323.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_global_color_orange_saved.png]({{site.baseurl}}/attachments/7504857/8719311.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_edit_global_attr.png]({{site.baseurl}}/attachments/7504857/8719294.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_edit_global_attr1.png]({{site.baseurl}}/attachments/7504857/8719325.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_global_attr_list.png]({{site.baseurl}}/attachments/7504857/8719314.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_global_color_edit.png]({{site.baseurl}}/attachments/7504857/8719326.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_color_global_attr_values.png]({{site.baseurl}}/attachments/7504857/8719316.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_cup_attributes_tab.png]({{site.baseurl}}/attachments/7504857/8719303.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_cup_global_tab.png]({{site.baseurl}}/attachments/7504857/8719304.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_cup_global_color.png]({{site.baseurl}}/attachments/7504857/8719319.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_global_color_dropdown.png]({{site.baseurl}}/attachments/7504857/8719320.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_global_color_orange.png]({{site.baseurl}}/attachments/7504857/8719324.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_color_globally.png]({{site.baseurl}}/attachments/7504857/8719309.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_color_globally_save.png]({{site.baseurl}}/attachments/7504857/8719310.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_global_color_orange.png]({{site.baseurl}}/attachments/7504857/8719308.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_edit_global_attr1.png]({{site.baseurl}}/attachments/7504857/8719313.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_classes_attr_global_color_edit.png]({{site.baseurl}}/attachments/7504857/8719315.png) (image/png)