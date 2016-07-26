---
identifier: ref_WmJBfwxA
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

| Field in CSV file | What this field describes | {% link "Value type" ref_2LwMTTTW %}** |
| _Fields supported by **X-Cart core**_ |
| ****sku***** | Unique identifier of the product. | 

String,
Max. length: 32

 |
| **name*** | Product name. | String,
Multilingual  |
| price | Default product price. | Float (e.g. 1.00) |
| memberships | 

Membership types, which members can see the product. Do not set it if you want to make the product visible to all customers. Otherwise it will be visible to the users assigned to specified membership only.

 | String,
Multiple  |
| description | Full description of the product. | 

String,
Multilingual,
HTML allowed 

 |
| briefDescription | Brief description of the product that is shown on the catalog pages. | String,
Multilingual,
HTML allowed  |
| enabled | Whether product is enabled. | Yes/No |
| weight | Product weight. | Float (e.g. 8.00) |
| shippable | Whether product can be shipped | Yes/No |
| images | 

For any image that needs to be imported you need to specify the image location. This can be one of the following:

*   Image URL
*   Path to the image on the server relative to the <xcart directory>/var/import folder; for example, images/products/image1.png.

When exporting data from X-Cart, image paths are written to the export file using the latter method (relative path).

This way when you need to re-import images back into X-Cart, you simply move the folder <xcart directory>/var/export/images to var/import/ - and use the existing relative paths).

It is possible to specify more than one images for import by separating the image paths with the '&&' symbols; for example, images/products/image1.png&&images/products/images2.png.

 | String,
Multiple  |
| imagesAlt | 

Text for alt property of images. This text will be shown when an image is not loaded for some reason.

If many images are assigned to the product, many alt texts can be imported as well. These alt texts must be separated by '&&' construction.

Examples:

*   Alt text for first image (1 alt text)
*   Alt text for first image&&Alt text for second image (2 alt texts)

 | String,
Multiple,
Max. length: 255  |
| arrivalDate | Date when the product will be available for sale. | Date (e.g. 1 Jan 2013) |
| date | Date when the product is created in X-Cart admin area. | Date (e.g. 1 Jan 2013) |
| updateDate | Date when the product was updated last time. | Date (e.g. 1 Jan 2013) |
| inventoryTrackingEnabled | Whether inventory (stock) tracking is enabled. | Yes/No |
| stockLevel | Current stock level. | Integer |
| lowLimitLevel | When stock of the product reaches this amount, admin will get a notification about low limit of these goods. | Integer (e.g. 10) |
| lowLimitEnabled | Whether low stock notification is enabled | Yes/No |
| categories | 

Defines what categories this product belongs to. Nested categories are separated by >>> construction.

It allows to specify multiple categories. They are separated by && construction.

Examples:

*   Toys (product is assigned to root category Toys)
*   Toys>>>Cube Goodies (product is assigned to the second level category Toys/Cube Goodies)
*   Toys&&Toys>>>Cube Goodies (products is assigned to two categories: Toys and Toys/Cube Goodies)

 | String,
Multiple  |
| cleanURL | 

SEO friendly URL of the product page.

Example: apple.html

 | String |
| useSeparateBox | Whether you use separate box for this item when you ship it | Yes/No |
| boxWidth | If **useSeparateBox** option is **Yes**, this field defines the width of the custom box for this product | Float (e.g. 1.00) |
| boxLength | If **useSeparateBox** option is **Yes**, this field defines the length of the custom box for this product | Float (e.g. 1.00) |
| boxHeight | If **useSeparateBox** option is **Yes**, this field defines the height of the custom box for this product | Float (e.g. 1.00) |
| itemsPerBox | If **useSeparateBox** option is **Yes,** this field defines what quantity of the product can be shipped in this box. | Integer (e.g. 3) |
| metaTags | Defines the content of <meta name="keywords" content="%value%"> meta tag | String,
Multilingual,
Max. length: 255  |
| metaDesc | Defines the content of <meta name="description" content="%value%"> meta tag | String,
Multilingual  |
| metaDescType | 

Defines meta description content type. Can be either **A** or **C**, where:

*   **A** stands for automatic mode when meta description will be generated from product description;
*   C stands for custom mode when meta desciption will be taken from **metaDesc_*** field in appropriate translation*;
    *this means that if the store is in _English_ language, meta description will be taken from **metaDesc_en** field.

 | String,
Max. length: 1  |
| metaTitle | Defines the content of <meta name="title" content="%value%"> meta tag | String,
Multilingual,
Max. length: 255  |
| productClass | 

Defines attribute class for a product. See also:

*   {% link "Product classes and attributes" ref_T90ZcEpP %}

 | String |
| taxClass | Defines tax class for a product | String |
| _Fields added by **Go Social** module_ |
| useCustomOpenGraphMeta | Defines whether use custom Open Graph meta tags for this product or use default ones | Yes/No |
| openGraphMeta | If **useCustomOpenGraphMeta** is **Yes**, then defines custom Open Graph meta tags | 

String,
HTML allowed,
Scripting allowed 

 |
| _Fields added by **Product Attachments** module_ |
| attachments | 

Defines what files are attached to this product.

Multiple files can be attached and they must be separated by && construction.

Examples:

*   path/to/my/files/user-manual.pdf (1 file)
*   path/to/my/files/user-manual.pdf&&path/to/my/files/spec.pdf (2 files)

 | 

String,
Multiple 

 |
| attachmentsTitle | 

Defines the titles of attachment files.

This field supports titles for many attachments and they must be separated by && construction.

Examples:

*   User manual (title of 1 attachment)
*   User manual&&Tech spec (title of 2 attachments)

 | 

String,
Multiple,
Multilingual,
Max. length: 128 

 |
| 

attachmentsDescription

 | 

Defines the description of attachments file.

This field supports descriptions for many attachments and they must be separated by && construction.

Examples:

*   This is a user manual for the product (description for 1 attachment)
*   This is a user manual for the product&&This is a tech spec for the product (description for 2 attachments)

 | String,
Multiple,
Multilingual  |
| _Fields added by **E-Goods** module_ |
| attachmentsPrivate | 

Defines what attachments are private and available after order is paid (e-goods) and what attachments are available right from the product page (modules **Product Attachments** and **E-Goods** must be enabled)

In case of many attachments, you can mark some of them as private and some as publicly available. Multiple values must be separated by && construction.

Example:

*   Yes (the product has one attachment and it is private)
*   Yes&&No (the product has two attachments, the first is private and the second is public)

 | Yes/No,
Multiple  |
| _Fields added by **Market Price** module_ |
| marketPrice | 

Defines the market price of the product, so your customers can estimate how much discount they get, if they buy a product from you.

 | Float (e.g. 5.00) |
| _Fields added by **Sale** module_ |
| sale | 

Defines your discount for this product.

It can have two types of values (absolute discount and percent one):

*   10.00 means that this product will receive $10 discount, assuming that dollar is your store currency.
*   %10 means that this product will receive 10% discount

 | String |
| _Fields added by **Multivendor** module_ |
| vendor | Product vendor login name | String |
| _Fields added by **Product Variants** module_ |
| variantSKU | Product variant SKU (if empty, takes SKU from parent product) | String,
Max. length: 32,
Multirow  |
| variantPrice | Product variant price (if empty, takes price from parent product) | Float,
Multirow  |
| variantQuantity | Product variant quantity (if empty, takes quantity from parent product) | Integer,
Multirow  |
| variantWeight | Product variant weight (if empty, takes weight from parent product) | Float,
Multirow  |
| variantImage | Product variant image location | String,
Multirow  |
| variantImageAlt | Product variant image alt text | String,
Max. length: 32,
Multirow  |
| _Fields added by **Wholesale** module_ |
| wholesalePrices | 

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

 | String,
Multiple  |
| variantWholesalePrices | 

Defines wholesale prices for the product variant.

**Product Variants** module must be enabled.

 | String,
Multiple,
Multirow  |
| _Fields added by **System Fields** module_ |
| upcIsbn | UPC/ISBN code | String,
Max. length: 32  |
| mnfVendor | Manufacturer of the product | String,
Max. length: 64  |
| 

variantupcIsbn

 | 

Product variant UPC/ISBN code.

 **Product Variants** module must be enabled.

 | String,
Max. length: 32,
Multirow  |
| variantmnfVendor | 

Manufacturer of the product variant.

**Product Variants** module must be enabled.

 | String,
Max. length: 64,
Multirow  |
| _Fields added by **Upselling Product** module_ |
| relatedProducts | 

SKUs of related products. You can specify several products separating them with '&&' symbols.

Examples:

*   SKU1 (1 product)
*   SKU1&&SKU2 (2 products)

 | String,
Multiple  |

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

* [import-1.png]({{site.baseurl}}/attachments/7503877/7602177.png) (image/png)