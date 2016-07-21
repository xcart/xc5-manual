---
identifier: ref_ZIASzvfX
updated_at: 2016-06-16 00:00
layout: article_with_sidebar
lang: en
title: 'CSV import: Products'
categories:
  - User manual

---


A product CSV file for import must have the name **products-xxxxxx.csv**, where the part **-xxxxxx** can be anything you want, or can be even omitted.

Examples of correct product CSV file names:

*   products.csv;
*   products-13-01-01.csv;
*   products-from-my-provider.csv

A product CSV file must contain at least two fields:

1.  **sku** - unique identifier of the product;
2.  **name** - product name.

Example of the simplest product CSV file:

![Simplest products.csv file]({{site.baseurl}}/attachments/7503877/7602177.png "Simplest products.csv file")

There are many more fields which you can include into your product CSV file. Below we provided a list of supported fields and value types accepted by X-Cart via these fields:

<table class="confluenceTable">

<tbody>

<tr>

<th class="confluenceTh">Field in CSV file</th>

<th colspan="1" class="confluenceTh">What this field describes</th>

<th colspan="1" class="confluenceTh">{% link "Value type" ref_Q4IypyMu %}**</th>

</tr>

<tr>

<td colspan="3" class="confluenceTd">_Fields supported by **X-Cart core**_</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">****sku*****</td>

<td colspan="1" class="confluenceTd">Unique identifier of the product.</td>

<td colspan="1" class="confluenceTd">

String,  
Max. length: 32

</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">**name***</td>

<td colspan="1" class="confluenceTd">Product name.</td>

<td colspan="1" class="confluenceTd">String,  
Multilingual </td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">price</td>

<td colspan="1" class="confluenceTd">Default product price.</td>

<td colspan="1" class="confluenceTd">Float (e.g. 1.00)</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">memberships</td>

<td colspan="1" class="confluenceTd">

Membership types, which members can see the product. Do not set it if you want to make the product visible to all customers. Otherwise it will be visible to the users assigned to specified membership only.

</td>

<td colspan="1" class="confluenceTd">String,  
Multiple </td>

</tr>

<tr>

<td class="confluenceTd">description</td>

<td colspan="1" class="confluenceTd">Full description of the product.</td>

<td colspan="1" class="confluenceTd">

String,  
Multilingual,  
HTML allowed 

</td>

</tr>

<tr>

<td class="confluenceTd">briefDescription</td>

<td colspan="1" class="confluenceTd">Brief description of the product that is shown on the catalog pages.</td>

<td colspan="1" class="confluenceTd">String,  
Multilingual,  
HTML allowed </td>

</tr>

<tr>

<td class="confluenceTd">enabled</td>

<td colspan="1" class="confluenceTd">Whether product is enabled.</td>

<td colspan="1" class="confluenceTd">Yes/No</td>

</tr>

<tr>

<td class="confluenceTd">weight</td>

<td colspan="1" class="confluenceTd">Product weight.</td>

<td colspan="1" class="confluenceTd">Float (e.g. 8.00)</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">shippable</td>

<td colspan="1" class="confluenceTd">Whether product can be shipped</td>

<td colspan="1" class="confluenceTd">Yes/No</td>

</tr>

<tr>

<td class="confluenceTd">images</td>

<td colspan="1" class="confluenceTd">

For any image that needs to be imported you need to specify the image location. This can be one of the following:

*   Image URL
*   Path to the image on the server relative to the <xcart directory>/var/import folder; for example, images/products/image1.png.

When exporting data from X-Cart, image paths are written to the export file using the latter method (relative path).

This way when you need to re-import images back into X-Cart, you simply move the folder <xcart directory>/var/export/images to var/import/ - and use the existing relative paths).

It is possible to specify more than one images for import by separating the image paths with the '&&' symbols; for example, images/products/image1.png&&images/products/images2.png.

</td>

<td colspan="1" class="confluenceTd">String,  
Multiple </td>

</tr>

<tr>

<td class="confluenceTd">imagesAlt</td>

<td colspan="1" class="confluenceTd">

Text for alt property of images. This text will be shown when an image is not loaded for some reason.

If many images are assigned to the product, many alt texts can be imported as well. These alt texts must be separated by '&&' construction.

Examples:

*   Alt text for first image (1 alt text)
*   Alt text for first image&&Alt text for second image (2 alt texts)

</td>

<td colspan="1" class="confluenceTd">String,  
Multiple,  
Max. length: 255 </td>

</tr>

<tr>

<td class="confluenceTd">arrivalDate</td>

<td colspan="1" class="confluenceTd">Date when the product will be available for sale.</td>

<td colspan="1" class="confluenceTd">Date (e.g. 1 Jan 2013)</td>

</tr>

<tr>

<td class="confluenceTd">date</td>

<td colspan="1" class="confluenceTd">Date when the product is created in X-Cart admin area.</td>

<td colspan="1" class="confluenceTd">Date (e.g. 1 Jan 2013)</td>

</tr>

<tr>

<td class="confluenceTd">updateDate</td>

<td colspan="1" class="confluenceTd">Date when the product was updated last time.</td>

<td colspan="1" class="confluenceTd">Date (e.g. 1 Jan 2013)</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">inventoryTrackingEnabled</td>

<td colspan="1" class="confluenceTd">Whether inventory (stock) tracking is enabled.</td>

<td colspan="1" class="confluenceTd">Yes/No</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">stockLevel</td>

<td colspan="1" class="confluenceTd">Current stock level.</td>

<td colspan="1" class="confluenceTd">Integer</td>

</tr>

<tr>

<td class="confluenceTd">lowLimitLevel</td>

<td class="confluenceTd">When stock of the product reaches this amount, admin will get a notification about low limit of these goods.</td>

<td class="confluenceTd">Integer (e.g. 10)</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">lowLimitEnabled</td>

<td colspan="1" class="confluenceTd">Whether low stock notification is enabled</td>

<td colspan="1" class="confluenceTd">Yes/No</td>

</tr>

<tr>

<td class="confluenceTd">categories</td>

<td colspan="1" class="confluenceTd">

Defines what categories this product belongs to. Nested categories are separated by >>> construction.

It allows to specify multiple categories. They are separated by && construction.

Examples:

*   Toys (product is assigned to root category Toys)
*   Toys>>>Cube Goodies (product is assigned to the second level category Toys/Cube Goodies)
*   Toys&&Toys>>>Cube Goodies (products is assigned to two categories: Toys and Toys/Cube Goodies)

</td>

<td colspan="1" class="confluenceTd">String,  
Multiple </td>

</tr>

<tr>

<td class="confluenceTd">cleanURL</td>

<td colspan="1" class="confluenceTd">

SEO friendly URL of the product page.

Example: apple.html

</td>

<td colspan="1" class="confluenceTd">String</td>

</tr>

<tr>

<td class="confluenceTd">useSeparateBox</td>

<td colspan="1" class="confluenceTd">Whether you use separate box for this item when you ship it</td>

<td colspan="1" class="confluenceTd">Yes/No</td>

</tr>

<tr>

<td class="confluenceTd">boxWidth</td>

<td colspan="1" class="confluenceTd">If **useSeparateBox** option is **Yes**, this field defines the width of the custom box for this product</td>

<td colspan="1" class="confluenceTd">Float (e.g. 1.00)</td>

</tr>

<tr>

<td class="confluenceTd">boxLength</td>

<td colspan="1" class="confluenceTd">If **useSeparateBox** option is **Yes**, this field defines the length of the custom box for this product</td>

<td colspan="1" class="confluenceTd">Float (e.g. 1.00)</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">boxHeight</td>

<td colspan="1" class="confluenceTd">If **useSeparateBox** option is **Yes**, this field defines the height of the custom box for this product</td>

<td colspan="1" class="confluenceTd">Float (e.g. 1.00)</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">itemsPerBox</td>

<td colspan="1" class="confluenceTd">If **useSeparateBox** option is **Yes,** this field defines what quantity of the product can be shipped in this box.</td>

<td colspan="1" class="confluenceTd">Integer (e.g. 3)</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">metaTags</td>

<td colspan="1" class="confluenceTd">Defines the content of <meta name="keywords" content="%value%"> meta tag</td>

<td colspan="1" class="confluenceTd">String,  
Multilingual,  
Max. length: 255 </td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">metaDesc</td>

<td colspan="1" class="confluenceTd">Defines the content of <meta name="description" content="%value%"> meta tag</td>

<td colspan="1" class="confluenceTd">String,  
Multilingual </td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">metaDescType</td>

<td colspan="1" class="confluenceTd">

Defines meta description content type. Can be either **A** or **C**, where:

*   **A** stands for automatic mode when meta description will be generated from product description;
*   C stands for custom mode when meta desciption will be taken from **metaDesc_*** field in appropriate translation*;  
    *this means that if the store is in _English_ language, meta description will be taken from **metaDesc_en** field.

</td>

<td colspan="1" class="confluenceTd">String,  
Max. length: 1 </td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">metaTitle</td>

<td colspan="1" class="confluenceTd">Defines the content of <meta name="title" content="%value%"> meta tag</td>

<td colspan="1" class="confluenceTd">String,  
Multilingual,  
Max. length: 255 </td>

</tr>

<tr>

<td class="confluenceTd">productClass</td>

<td class="confluenceTd">

Defines attribute class for a product. See also:

*   {% link "Product classes and attributes" ref_F1TNi0gL %}

</td>

<td class="confluenceTd">String</td>

</tr>

<tr>

<td class="confluenceTd">taxClass</td>

<td class="confluenceTd">Defines tax class for a product</td>

<td class="confluenceTd">String</td>

</tr>

<tr>

<td colspan="3" class="confluenceTd">_Fields added by **Go Social** module_</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">useCustomOpenGraphMeta</td>

<td colspan="1" class="confluenceTd">Defines whether use custom Open Graph meta tags for this product or use default ones</td>

<td colspan="1" class="confluenceTd">Yes/No</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">openGraphMeta</td>

<td colspan="1" class="confluenceTd">If **useCustomOpenGraphMeta** is **Yes**, then defines custom Open Graph meta tags</td>

<td colspan="1" class="confluenceTd">

String,  
HTML allowed,  
Scripting allowed 

</td>

</tr>

<tr>

<td colspan="3" class="confluenceTd">_Fields added by **Product Attachments** module_</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">attachments</td>

<td colspan="1" class="confluenceTd">

Defines what files are attached to this product.

Multiple files can be attached and they must be separated by && construction.

Examples:

*   path/to/my/files/user-manual.pdf (1 file)
*   path/to/my/files/user-manual.pdf&&path/to/my/files/spec.pdf (2 files)

</td>

<td colspan="1" class="confluenceTd">

String,  
Multiple 

</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">attachmentsTitle</td>

<td colspan="1" class="confluenceTd">

Defines the titles of attachment files.

This field supports titles for many attachments and they must be separated by && construction.

Examples:

*   User manual (title of 1 attachment)
*   User manual&&Tech spec (title of 2 attachments)

</td>

<td colspan="1" class="confluenceTd">

String,  
Multiple,  
Multilingual,  
Max. length: 128 

</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">

attachmentsDescription

</td>

<td colspan="1" class="confluenceTd">

Defines the description of attachments file.

This field supports descriptions for many attachments and they must be separated by && construction.

Examples:

*   This is a user manual for the product (description for 1 attachment)
*   This is a user manual for the product&&This is a tech spec for the product (description for 2 attachments)

</td>

<td colspan="1" class="confluenceTd">String,  
Multiple,  
Multilingual </td>

</tr>

<tr>

<td colspan="3" class="confluenceTd">_Fields added by **E-Goods** module_</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">attachmentsPrivate</td>

<td colspan="1" class="confluenceTd">

Defines what attachments are private and available after order is paid (e-goods) and what attachments are available right from the product page (modules **Product Attachments** and **E-Goods** must be enabled)

In case of many attachments, you can mark some of them as private and some as publicly available. Multiple values must be separated by && construction.

Example:

*   Yes (the product has one attachment and it is private)
*   Yes&&No (the product has two attachments, the first is private and the second is public)

</td>

<td colspan="1" class="confluenceTd">Yes/No,  
Multiple </td>

</tr>

<tr>

<td colspan="3" class="confluenceTd">_Fields added by **Market Price** module_</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">marketPrice</td>

<td colspan="1" class="confluenceTd">

Defines the market price of the product, so your customers can estimate how much discount they get, if they buy a product from you.

</td>

<td colspan="1" class="confluenceTd">Float (e.g. 5.00)</td>

</tr>

<tr>

<td colspan="3" class="confluenceTd">_Fields added by **Sale** module_</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">sale</td>

<td colspan="1" class="confluenceTd">

Defines your discount for this product.

It can have two types of values (absolute discount and percent one):

*   10.00 means that this product will receive $10 discount, assuming that dollar is your store currency.
*   %10 means that this product will receive 10% discount

</td>

<td colspan="1" class="confluenceTd">String</td>

</tr>

<tr>

<td colspan="3" class="confluenceTd">_Fields added by **Multivendor** module_</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">vendor</td>

<td colspan="1" class="confluenceTd">Product vendor login name</td>

<td colspan="1" class="confluenceTd">String</td>

</tr>

<tr>

<td colspan="3" class="confluenceTd">_Fields added by **Product Variants** module_</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">variantSKU</td>

<td colspan="1" class="confluenceTd">Product variant SKU (if empty, takes SKU from parent product)</td>

<td colspan="1" class="confluenceTd">String,  
Max. length: 32,  
Multirow </td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">variantPrice</td>

<td colspan="1" class="confluenceTd">Product variant price (if empty, takes price from parent product)</td>

<td colspan="1" class="confluenceTd">Float,  
Multirow </td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">variantQuantity</td>

<td colspan="1" class="confluenceTd">Product variant quantity (if empty, takes quantity from parent product)</td>

<td colspan="1" class="confluenceTd">Integer,  
Multirow </td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">variantWeight</td>

<td colspan="1" class="confluenceTd">Product variant weight (if empty, takes weight from parent product)</td>

<td colspan="1" class="confluenceTd">Float,  
Multirow </td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">variantImage</td>

<td colspan="1" class="confluenceTd">Product variant image location</td>

<td colspan="1" class="confluenceTd">String,  
Multirow </td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">variantImageAlt</td>

<td colspan="1" class="confluenceTd">Product variant image alt text</td>

<td colspan="1" class="confluenceTd">String,  
Max. length: 32,  
Multirow </td>

</tr>

<tr>

<td colspan="3" class="confluenceTd">_Fields added by **Wholesale** module_</td>

</tr>

<tr>

<td class="confluenceTd">wholesalePrices</td>

<td class="confluenceTd">

Defines wholesale prices for the product.

Examples:

1.  You want to set up price tiers as follows:  
    If a customer buys from 1 to 5 items, each item will cost $50  
    If they buy from 6 items, then the price will be $45  

    Then you would need to specify this system as follows in the CSV file:  
    **1-5=50.00&&6=45.00**   

2.  You want to set up price tiers as follows:  
    If a customer buys from 1 to 5 items, each item will cost $50  
    If they buy from 6 items, then the price will be $45  
    If a customer with Wholesaler membership buys from 3 items, then the price will be $40   

    Then you would need to specify this system as follows in the CSV file:  
     **1-5=50.00&&6=45.00&&3(Wholesaler)=40.00**

</td>

<td class="confluenceTd">String,  
Multiple </td>

</tr>

<tr>

<td class="confluenceTd">variantWholesalePrices</td>

<td class="confluenceTd">

Defines wholesale prices for the product variant.

**Product Variants** module must be enabled.

</td>

<td class="confluenceTd">String,  
Multiple,  
Multirow </td>

</tr>

<tr>

<td colspan="3" class="confluenceTd">_Fields added by **System Fields** module_</td>

</tr>

<tr>

<td class="confluenceTd">upcIsbn</td>

<td class="confluenceTd">UPC/ISBN code</td>

<td class="confluenceTd">String,  
Max. length: 32 </td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">mnfVendor</td>

<td colspan="1" class="confluenceTd">Manufacturer of the product</td>

<td colspan="1" class="confluenceTd">String,  
Max. length: 64 </td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">

variantupcIsbn

</td>

<td colspan="1" class="confluenceTd">

Product variant UPC/ISBN code.

 **Product Variants** module must be enabled.

</td>

<td colspan="1" class="confluenceTd">String,  
Max. length: 32,  
Multirow </td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">variantmnfVendor</td>

<td colspan="1" class="confluenceTd">

Manufacturer of the product variant.

**Product Variants** module must be enabled.

</td>

<td colspan="1" class="confluenceTd">String,  
Max. length: 64,  
Multirow </td>

</tr>

<tr>

<td colspan="3" class="confluenceTd">_Fields added by **Upselling Product** module_</td>

</tr>

<tr>

<td class="confluenceTd">relatedProducts</td>

<td class="confluenceTd">

SKUs of related products. You can specify several products separating them with '&&' symbols.

Examples:

*   SKU1 (1 product)
*   SKU1&&SKU2 (2 products)

</td>

<td class="confluenceTd">String,  
Multiple </td>

</tr>

</tbody>

</table>

<sub>* Required field.</sub>

<sub>** See {% link "CSV field attributes" CSV-field-attributes_9306552.html %} for more info.</sub>

**Tips**:

*   If you are going to import data into X-Cart and do not wish to update certain X-Cart fields during the import process, you should not include these fields into your CSV file for import. Simply remove the respective column(s) from the file.  

*   If necessary, import can be used to clear previously set field values from non-numeric fields. To clear a field value via import, in your CSV file to be imported specify the value of the field as "NULL". After the import process is completed, the fields in which the value "NULL" has been imported will be cleared.   
    This feature is supported by the following product fields:  
    - memberships;  
    - categories;  
    - images;  
    - imagesAlt;  
    - attributeValue;  
    - variantImage (Product Variants module).  

## Attachments:

![](images/icons/bullet_blue.gif) [import-1.png]({{site.baseurl}}/attachments/7503877/7602177.png) (image/png)