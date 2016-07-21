---
identifier: ref_o0sHduTv
updated_at: 2015-07-08 00:00
layout: article_with_sidebar
lang: en
title: 'Setting up a bookable product with variants'
categories:
  - User manual

---


To create a bookable product with product variants, follow these steps:

1.  Start creating a new product the normal way: specify a product name, choose a category, add images, etc.   
    ![]({{site.baseurl}}/attachments/8750040/8718732.png?effects=drop-shadow)
2.  Leave the fields **Price** and **Quantity in stock** at their default values (Remember, we are creating a product with variants, so we'll set a price and a quantity for each variant individually a bit later).   
    ![]({{site.baseurl}}/attachments/8750040/8718733.png?effects=drop-shadow)
3.  Disable shipping calculation for the product by setting the **Shippable** property to "No":  
    ![]({{site.baseurl}}/attachments/8750040/8718735.png?effects=drop-shadow)  

4.  Provide the rest of general information about the product as needed and click **Add product** to save it. The product will be created.  
    ![]({{site.baseurl}}/attachments/8750040/8718744.png?effects=drop-shadow)  

5.  Continue configuring the product you have created: Switch to the **Booking** tab of the product details and set the **Product booking **option to "Enabled" to specify that this product is bookable:  
    ![]({{site.baseurl}}/attachments/8750040/8718736.png?effects=drop-shadow)  
    Be sure to click **Update** to save the changes.  

6.  Configure the attributes whose values will be used to form product variants for the product. If you are going to have more than one bookable product in your store, consider setting up a product class and configuring attributes on the class level. If all your products are going to be bookable, configure attributes on the global level. For the sake of example, we'll create a product class "Hotel" with the attributes "Room type" and "Number of guests":
    1.  In the **Classes & attributes** section, select to add a new product class:  
        ![]({{site.baseurl}}/attachments/8750040/8718728.png?effects=drop-shadow)  

    2.  Provide a name for the new product class (in our case, "Hotel") and save the changes:  
        ![]({{site.baseurl}}/attachments/8750040/8718729.png?effects=drop-shadow)  

    3.  Click the <u>Edit attributes</u> link opposite the product class name to go to a page where you can configure attributes:  
        ![]({{site.baseurl}}/attachments/8750040/8718730.png?effects=drop-shadow)  

    4.  On the page that opens, select to add a new attribute:  
        ![]({{site.baseurl}}/attachments/8750040/8718731.png?effects=drop-shadow)  

    5.  In the **New attribute** popup, provide the details of your attribute. We've entered the attribute name "Room type" and left the attribute type set to "Plain field":  
        ![]({{site.baseurl}}/attachments/8750040/8718739.png?effects=drop-shadow)  

    6.  Click **Next**. A popup titled **Edit attribute values** will appear. In this popup, click the **New value** button a few times to add some blank new lines where you will enter your values for the attribute "Room type":  
        ![]({{site.baseurl}}/attachments/8750040/8718740.png?effects=drop-shadow)  

    7.  Enter attribute value names on the lines you have added. You'll need a value for every room type that can be booked on your site. As you can see on the screenshot below, we've added four room types: "Double or Twin Room - Attic", "Superior Double or Twin Room", "Standard Room Sea View" and "Standard Room Land View". We'll only need the former two of these values for the product we are creating right now; the latter two we'll use later for another hotel. If we need more room types, we'll be able to add them later.  
        ![]({{site.baseurl}}/attachments/8750040/8718741.png?effects=drop-shadow)  

        Click **Save changes**. The attribute values will be saved.
    8.  Repeat Steps d-h to create the attribute "Number of guests" and add values for it.  
        ![]({{site.baseurl}}/attachments/8750040/8718745.png?effects=drop-shadow)  

    9.  If necessary, add other attributes (Things like "Free WiFi: Yes/No", "Air Conditioning: Yes/No", "Meals: Room only / Half Board / Full Board").  
        ![]({{site.baseurl}}/attachments/8750040/8718747.png?effects=drop-shadow)  

7.  Assign appropriate attribute values to your bookable product via the **Attributes** tab.  
    ![]({{site.baseurl}}/attachments/8750040/8718746.png?effects=drop-shadow)  

8.  Use the **Variants** tab to create specific bookable variants for the product.   

    1.  Choose the attributes on which your variants will be based and select how you would like to create the variants (manually or automatically). We have selected to create variants based on the "Group type" attribute only and are going to use the link <u>Create all possible variants (2)</u> for the variants to be generated automatically:  
        ![]({{site.baseurl}}/attachments/8750040/8718750.png?effects=drop-shadow)  
        Once all the necessary variants have been created based on the available option combinations, you should have a list like the following:  
        ![]({{site.baseurl}}/attachments/8750040/8718751.png?effects=drop-shadow)  

    2.  Adjust the **Price**, **SKU**, **Quantity** (maximum bookable quantity) and **Weight** values for each of the variants; upload variant images. Be sure to save the changes.  
        ![]({{site.baseurl}}/attachments/8750040/8718752.png?effects=drop-shadow)

That is all; you have configured a bookable product with product variants.

Now, if you haven't yet done so, go to the "Booking" module settings page and specify which of the attributes you have added for your bookable products need to be used to display your product variants in the form of a table on the product details page on the storefront. For example, if you want the individual lines of your booking table corresponding to the product variants to have titles based on the values of the product's main variant-forming attribute ("Room type", "Car type" or similar), this attribute needs to be specified as the "Room type" attribute for your site. If you want your booking table to have a column for the number of guests per room / number of seats per car / etc., specify which of your attributes ("Number of guests", "Number of seats" or similar) should be used as the "Number of guests" attribute for your site. See {% link "Configuring the module "Booking"" ref_LdKhQD4I %} for more information.

We have adjusted the module settings as follows:

![]({{site.baseurl}}/attachments/8750040/8718758.png?effects=drop-shadow)

Now the variants of our product on the storefront should look something like this:

  ![]({{site.baseurl}}/attachments/8750040/8718818.png?effects=drop-shadow)

Expanding a variant by clicking the arrow icon next to its title allows you to view and select product options specific for that variant. For example, on the screenshot below we can see the option selector "Meals" allowing us to choose the type of meals we want at the hotel:

![]({{site.baseurl}}/attachments/8750040/8718820.png?effects=drop-shadow)

In case you are wondering why we are seeing just the attribute "Meals" here, but are not seeing the attributes "Free WiFi: Yes" and "Air Conditioning: Yes", although we have configured them earlier for this product, the explanation is simple: the booking table only shows Yes/No attributes if they are configured as multi-value product options:

![]({{site.baseurl}}/attachments/8750040/8718821.png?effects=drop-shadow)

If such multi-value attributes are not used for variants, we see them as checkboxes:

![]({{site.baseurl}}/attachments/8750040/8718822.png?effects=drop-shadow)

If they are used to form product variants, we see them simply as a part of product variant description. For example, if we base our variants on "Room type" and "Free WiFi" like so:

![]({{site.baseurl}}/attachments/8750040/8718823.png?effects=drop-shadow)

The result will be this:

![]({{site.baseurl}}/attachments/8750040/8718824.png?effects=drop-shadow)

When, however, Yes/No attributes are configured as non-multi-value options:

![]({{site.baseurl}}/attachments/8750040/8718825.png?effects=drop-shadow)

we only see them in the Specification section:

![]({{site.baseurl}}/attachments/8750040/8718827.png?effects=drop-shadow)

Note that the default wording used by the module "Booking" may not work well for your type of bookable products. For example, the phrases  "Room type" and  "Check dates (N-night stay)" will not work for a car rental website. Not to worry - the wording can be fixed by editing the "Booking" module text labels. For details see {% link "Editing "Booking" module text labels to your needs" ref_k4DWqNTo %}.

_Related pages:_

*   *   {% link "Configuring the module "Booking"" 8749990.html %}
    *   {% link "Editing "Booking" module text labels to your needs" 8750032.html %}
    *   {% link "Setting up a simple bookable product" ref_WO2CMR6d %}

## Attachments:

![](images/icons/bullet_blue.gif) [new_class_hotel.png]({{site.baseurl}}/attachments/8750040/8718728.png) (image/png)  
![](images/icons/bullet_blue.gif) [new_class_hotel1.png]({{site.baseurl}}/attachments/8750040/8718729.png) (image/png)  
![](images/icons/bullet_blue.gif) [edit_attr_for_hotel.png]({{site.baseurl}}/attachments/8750040/8718737.png) (image/png)  
![](images/icons/bullet_blue.gif) [new_attr_hotel.png]({{site.baseurl}}/attachments/8750040/8718738.png) (image/png)  
![](images/icons/bullet_blue.gif) [add_hotel.png]({{site.baseurl}}/attachments/8750040/8718732.png) (image/png)  
![](images/icons/bullet_blue.gif) [quantity_price_default.png]({{site.baseurl}}/attachments/8750040/8718734.png) (image/png)  
![](images/icons/bullet_blue.gif) [quantity_price_default.png]({{site.baseurl}}/attachments/8750040/8718733.png) (image/png)  
![](images/icons/bullet_blue.gif) [hotel_shippable_no.png]({{site.baseurl}}/attachments/8750040/8718735.png) (image/png)  
![](images/icons/bullet_blue.gif) [product_booking_enabled_hotel.png]({{site.baseurl}}/attachments/8750040/8718736.png) (image/png)  
![](images/icons/bullet_blue.gif) [edit_attr_for_hotel.png]({{site.baseurl}}/attachments/8750040/8718730.png) (image/png)  
![](images/icons/bullet_blue.gif) [new_attr_hotel.png]({{site.baseurl}}/attachments/8750040/8718731.png) (image/png)  
![](images/icons/bullet_blue.gif) [new_attr_room_type.png]({{site.baseurl}}/attachments/8750040/8718739.png) (image/png)  
![](images/icons/bullet_blue.gif) [new_attr_value.png]({{site.baseurl}}/attachments/8750040/8718740.png) (image/png)  
![](images/icons/bullet_blue.gif) [attr_values_for_room_type2.png]({{site.baseurl}}/attachments/8750040/8718741.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2015-6-28 17:0:47.png]({{site.baseurl}}/attachments/8750040/8718742.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2015-6-28 17:1:10.png]({{site.baseurl}}/attachments/8750040/8718743.png) (image/png)  
![](images/icons/bullet_blue.gif) [hotel_added.png]({{site.baseurl}}/attachments/8750040/8718744.png) (image/png)  
![](images/icons/bullet_blue.gif) [guests_attr.png]({{site.baseurl}}/attachments/8750040/8718745.png) (image/png)  
![](images/icons/bullet_blue.gif) [assign_attr.png]({{site.baseurl}}/attachments/8750040/8718748.png) (image/png)  
![](images/icons/bullet_blue.gif) [all_attr_hotel.png]({{site.baseurl}}/attachments/8750040/8718753.png) (image/png)  
![](images/icons/bullet_blue.gif) [assign_attr.png]({{site.baseurl}}/attachments/8750040/8718749.png) (image/png)  
![](images/icons/bullet_blue.gif) [assign_attr.png]({{site.baseurl}}/attachments/8750040/8718754.png) (image/png)  
![](images/icons/bullet_blue.gif) [create_variants.png]({{site.baseurl}}/attachments/8750040/8718757.png) (image/png)  
![](images/icons/bullet_blue.gif) [hotel_variants.png]({{site.baseurl}}/attachments/8750040/8718756.png) (image/png)  
![](images/icons/bullet_blue.gif) [hotel_variants1.png]({{site.baseurl}}/attachments/8750040/8718755.png) (image/png)  
![](images/icons/bullet_blue.gif) [all_attr_hotel.png]({{site.baseurl}}/attachments/8750040/8718747.png) (image/png)  
![](images/icons/bullet_blue.gif) [assign_attr.png]({{site.baseurl}}/attachments/8750040/8718746.png) (image/png)  
![](images/icons/bullet_blue.gif) [hotel_variants1.png]({{site.baseurl}}/attachments/8750040/8718752.png) (image/png)  
![](images/icons/bullet_blue.gif) [hotel_variants.png]({{site.baseurl}}/attachments/8750040/8718751.png) (image/png)  
![](images/icons/bullet_blue.gif) [create_variants.png]({{site.baseurl}}/attachments/8750040/8718750.png) (image/png)  
![](images/icons/bullet_blue.gif) [module-settings.png]({{site.baseurl}}/attachments/8750040/8718758.png) (image/png)  
![](images/icons/bullet_blue.gif) [hotel_variants_booking.png]({{site.baseurl}}/attachments/8750040/8718819.png) (image/png)  
![](images/icons/bullet_blue.gif) [hotel_variants_booking.png]({{site.baseurl}}/attachments/8750040/8718818.png) (image/png)  
![](images/icons/bullet_blue.gif) [hotel_variants_booking1.png]({{site.baseurl}}/attachments/8750040/8718820.png) (image/png)  
![](images/icons/bullet_blue.gif) [multi-value.png]({{site.baseurl}}/attachments/8750040/8718821.png) (image/png)  
![](images/icons/bullet_blue.gif) [checkbox_option.png]({{site.baseurl}}/attachments/8750040/8718822.png) (image/png)  
![](images/icons/bullet_blue.gif) [wifi_variants.png]({{site.baseurl}}/attachments/8750040/8718823.png) (image/png)  
![](images/icons/bullet_blue.gif) [non-checkbox.png]({{site.baseurl}}/attachments/8750040/8718824.png) (image/png)  
![](images/icons/bullet_blue.gif) [non-multi.png]({{site.baseurl}}/attachments/8750040/8718826.png) (image/png)  
![](images/icons/bullet_blue.gif) [non-multi.png]({{site.baseurl}}/attachments/8750040/8718825.png) (image/png)  
![](images/icons/bullet_blue.gif) [specification.png]({{site.baseurl}}/attachments/8750040/8718827.png) (image/png)