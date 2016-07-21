---
identifier: ref_VLNBHNDw
updated_at: 2015-10-15 00:00
layout: article_with_sidebar
lang: en
title: 'Managing X-Cart order statuses (X-Cart 5.2.7 and later)'
categories:
  - User manual

---


In X-Cart versions 5.2.7 and later, order statuses can be managed using the module **Custom Order Statuses**.

![]({{site.baseurl}}/attachments/8750763/8719499.png?effects=drop-shadow)

With this module you can:

*   {% link "view and manage the list of order statuses" ref_VLNBHNDw %} supported by your X-Cart store;
*   {% link "add your own custom order statuses" 8750763.html %};
*   {% link "rename existing order statuses" 8750763.html %} (both {% link "system" ref_87Vtn3Al#UnderstandingX-Cartorderstatuses-DefaultOrderStatuses %} and custom ones);
*   {% link "delete custom order statuses" 8750763.html %} (NB: {% link "System" Understanding-X-Cart-order-statuses_8750830.html#UnderstandingX-Cartorderstatuses-DefaultOrderStatuses %} order statuses cannot be deleted). 

Note

Icon

The module Custom Order Statuses is not compatible with X-Cart versions prior to X-Cart 5.2.7\. For these older X-Cart versions, custom order statuses can be added using the method described in the article {% link "Adding new shipping/payment statuses (X-Cart 5.2.6 and earlier)" ref_fSdcDuA6 %}.

# Viewing order statuses

With the module **Custom Order Statuses** installed and enabled, the complete list of order statuses used by your X-Cart store can be found in the section Order statuses (**Orders** > **Order statuses**):

![]({{site.baseurl}}/attachments/8750763/8719462.png?effects=drop-shadow)

In fact, there are two lists, since payment statuses and shipping statuses are listed separately. You can switch between the lists using the respective tabs:

![]({{site.baseurl}}/attachments/8750763/8719463.png?effects=drop-shadow)

For each order status on the list the following information is provided:

*   **Name**: Order status name.
*   **Orders**: Number of orders currently in this status. The number is a link allowing you to access all the orders in this status as a list.

Order statuses that have Question mark icons displayed opposite their names in the column at the far right are the so-called _system order statuses_.

![]({{site.baseurl}}/attachments/8750763/8719494.png?effects=drop-shadow)  

These statuses are present in your X-Cart store from the very start and work out of the box. They cannot be removed, but, if necessary, can be renamed. Hovering the cursor over a Question mark icon for a specific system status allows you to see the letter code by which this order status is referred to in the software code:

![]({{site.baseurl}}/attachments/8750763/8719493.png?effects=drop-shadow)  

(Most people will have no use for this information, but we included it for X-Cart developers who will look into the code to see how order statuses work).

Order statuses that have Trash icons displayed opposite their names instead of Question mark icons - if any such statuses are present in your store - are _custom order statuses_.

![]({{site.baseurl}}/attachments/8750763/8719485.png?effects=drop-shadow)  

Such statuses can be deleted as well as renamed.

The order of statuses in the list determines the order in which the statuses appear in the drop-down selectors that the store administrator uses to assign payment and shipping statuses to an order.

![]({{site.baseurl}}/attachments/8750763/8719497.png?effects=drop-shadow)  

You can rearrange this order by dragging and dropping specific statuses in the list to the positions you require (Use the four-headed arrows in the column at the far left).

![]({{site.baseurl}}/attachments/8750763/8719498.png?effects=drop-shadow)  

# Adding custom order statuses

If X-Cart's {% link "system order statuses" Understanding-X-Cart-order-statuses_8750830.html#UnderstandingX-Cartorderstatuses-DefaultOrderStatuses %} do not meet the needs of your business, you can create your own statuses. It is possible to create both payment order statuses and shipping order statuses. 

Note

Icon

Custom order statuses do not currently have the ability to change the inventory levels of products in the order, but we are hoping to implement this feature in the nearest future.

To add a new order status:

1.  In your X-Cart store's Admin area, go to the Order statuses section (**Orders** > **Order statuses**). 
2.  Make sure you are viewing the correct page tab (Payment statuses are added on the tab that opens by default. To add a shipping status, you will need to switch to the **Shipping statuses** tab).   
    ![]({{site.baseurl}}/attachments/8750763/8719480.png?effects=drop-shadow)
3.  Click the **Add status** button:  
    ![]({{site.baseurl}}/attachments/8750763/8719478.png?effects=drop-shadow)  
    A new blank field is added on a new line at the top of the order status list:  
    ![]({{site.baseurl}}/attachments/8750763/8719479.png?effects=drop-shadow)  

4.  Use the blank field to enter the order status name you require.  

5.  Click the **Save changes** button at the bottom of the list.   
    ![]({{site.baseurl}}/attachments/8750763/8719482.png?effects=drop-shadow)  
    The new order status will be added:  
    ![]({{site.baseurl}}/attachments/8750763/8719484.png?effects=drop-shadow)  

# Renaming order statuses

It is possible to rename existing order statuses, both system and custom ones.

To rename an order status:

1.  In your X-Cart store's Admin area, go to the Order statuses section (**Orders** > **Order statuses**). 
2.  Make sure you are viewing the correct page tab (Payment statuses can be found on the tab that opens by default. To access shipping statuses, you will need to switch to the **Shipping statuses** tab). 
3.  In the list of order statuses, locate the status that needs to be renamed. 
4.  Click on the status name. The status name field becomes editable:  
    ![]({{site.baseurl}}/attachments/8750763/8719488.png?effects=drop-shadow)  

5.  Change the name of the status as you require.  
    ![]({{site.baseurl}}/attachments/8750763/8719489.png?effects=drop-shadow)  

6.  Click the **Save changes** button at the bottom of the list.  
    ![]({{site.baseurl}}/attachments/8750763/8719491.png?effects=drop-shadow)  
    The new status name will be saved.  
    ![]({{site.baseurl}}/attachments/8750763/8719492.png?effects=drop-shadow)  

# Deleting order statuses

It is possible to delete custom order statuses. 

Note

Icon

System order statuses cannot be deleted. If you are not happy with the name of a system order status, you may want to consider {% link "renaming" 8750763.html %} it.

To delete an order status:

1.  In your X-Cart store's Admin area, go to the Order statuses section (**Orders** > **Order statuses**). 
2.  Make sure you are viewing the correct page tab (Payment statuses can be found on the tab that opens by default. To access shipping statuses, you will need to switch to the **Shipping statuses** tab).   

3.  In the list of order statuses, locate the status that needs to be deleted.
4.  Click the Trash icon opposite its name.  
    ![]({{site.baseurl}}/attachments/8750763/8719485.png?effects=drop-shadow)  
    The status will be marked for deletion.
5.  Click the **Save changes** button at the bottom.   
    ![]({{site.baseurl}}/attachments/8750763/8719486.png?effects=drop-shadow)  
    The status will be deleted:  
    ![]({{site.baseurl}}/attachments/8750763/8719487.png?effects=drop-shadow)  

_Related pages:_

*   {% link "Understanding X-Cart order statuses" Understanding-X-Cart-order-statuses_8750830.html %}
*   {% link "Adding new shipping/payment statuses (X-Cart 5.2.6 and earlier)" 8224873.html %}

## Attachments:

![](images/icons/bullet_blue.gif) [xc5_order_statuses.png]({{site.baseurl}}/attachments/8750763/8719462.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_page_tabs.png]({{site.baseurl}}/attachments/8750763/8719463.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_add_new_button.png]({{site.baseurl}}/attachments/8750763/8719481.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_add_new.png]({{site.baseurl}}/attachments/8750763/8719479.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_select_tab.png]({{site.baseurl}}/attachments/8750763/8719480.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_add_new_button.png]({{site.baseurl}}/attachments/8750763/8719478.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_add_new1.png]({{site.baseurl}}/attachments/8750763/8719483.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_add_new1.png]({{site.baseurl}}/attachments/8750763/8719482.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_add_new2.png]({{site.baseurl}}/attachments/8750763/8719484.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_trash_icon.png]({{site.baseurl}}/attachments/8750763/8719496.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_delete.png]({{site.baseurl}}/attachments/8750763/8719486.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_deleted.png]({{site.baseurl}}/attachments/8750763/8719487.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_rename.png]({{site.baseurl}}/attachments/8750763/8719488.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_rename1.png]({{site.baseurl}}/attachments/8750763/8719490.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_rename1.png]({{site.baseurl}}/attachments/8750763/8719489.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_rename2.png]({{site.baseurl}}/attachments/8750763/8719491.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_rename3.png]({{site.baseurl}}/attachments/8750763/8719492.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_system_statuses.png]({{site.baseurl}}/attachments/8750763/8719495.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_system_statuses1.png]({{site.baseurl}}/attachments/8750763/8719494.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_system_statuses.png]({{site.baseurl}}/attachments/8750763/8719493.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_trash_icon.png]({{site.baseurl}}/attachments/8750763/8719485.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_status_selectors.png]({{site.baseurl}}/attachments/8750763/8719497.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_order_arrows.png]({{site.baseurl}}/attachments/8750763/8719498.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_order_statuses_custom_order_statuses_module.png]({{site.baseurl}}/attachments/8750763/8719499.png) (image/png)