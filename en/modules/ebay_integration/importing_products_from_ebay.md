---
lang: en
layout: article_with_sidebar
updated_at: '2017-07-26 12:54 +0400'
identifier: ref_ydMT71kb
title: Importing products from eBay
order: 100
published: false
---
If you already have items listed on eBay that you need to have in your X-Cart store as products, you can import them from eBay into your X-Cart store.

To be imported into an X-Cart store, an eBay item needs to have a SKU specified in the _Custom Label_ field; so, before you attemt importing any items, make sure they have SKUs. 

To import items from eBay:

1.  In your X-Cart store's Admin area, go to the Import eBay Items page (**Catalog** > **Import eBay Items**)
    ![]({{site.baseurl}}/attachments/9306779/9439199.png)

2.  Specify which orders you want to import by adjusting the following fields:

    * **eBay site**: Specify the eBay marketplace site from which you would like to import items.
    * **Item type**: Select the type of items you would like to import (_Active items_, _Inactive items_).
    * **eBay Item SKU**: Enter the eBay SKU of the item that needs to be imported (Such a SKU can be obtained from the _Custom Label_ field of the item). If you need to import multiple items, enter a comma separated list of SKUs.
    * **Upload item images**: With this option enabled, item images will be imported from eBay along with the item details and description to become product images in your X-Cart store. With this option disabled, eBay items will be imported without the images.
    * **Remove exists products**: Before importing an item from eBay, the module will check whether this item is new or already exists in your X-Cart store (See more info below). With this option enabled, any item found to be existing in your X-Cart store will be removed from the store and replaced with the respective item from eBay. 
    * **Import only new items**: Before importing an item from eBay, the module will check whether this item is new or already exists in your X-Cart store  (See more info below). With this option enabled, only the items that do not already exist in your X-Cart store will be imported.

3. Click **Import items** to launch the product import process.    

    
    **Information**: An item on eBay can be matched to an item in an X-Cart store using the item SKU and eBay Item Id. 
    An item SKU is a unique identifier of a product in an X-Cart store; when a product is exported to eBay, its SKU is saved in the _Custom Label_ field of the eBay item; for items created on eBay without the use of X-Cart, the contents of the _Custom Label_ field can be specified by the seller manually. 
    An eBay Item Id is a unique identifier of the item on eBay; in an X-Cart store, it is saved in the _eBay Item Id_ field on the eBay product options tab of the product page in Admin; this happens when a product is exported to eBay, when the product is imported from eBay, or when the store administrator updates the field value manually.
    Before importing any item from eBay into an X-Cart store, the eBay Integration module performs a check to determine whether this item already exists in the X-Cart store or should be considered new. First, it checks the item SKU: if the Custom Label of the item matches a SKU in the X-Cart store, the item is identified as already existing in the store. If no matching SKUs are found in the store database, the module goes on to check the eBay Item Id field. If the item Id on eBay matches some eBay Item Id in the X-Cart store database, the item is identified as already existing in the store; if no match is found, the item is considered new. Once a item has been imported into X-Cart, its _Custom Label_ field value becomes X-Cart product SKU.
    
