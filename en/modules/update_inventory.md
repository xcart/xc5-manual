---
identifier: ref_uSIvmuTh
updated_at: 2016-04-01 00:00
layout: article_with_sidebar
lang: en
title: 'Update inventory'
categories:
  - User manual

---


Note

Icon

Starting with X-Cart version 5.2.13, X-Cart has a full-featured import mode for the updating of existing items, which allows you to update your product information (including the stock quantity, price and other product properties) using the standard X-Cart's "Import" feature - without the need to use the module "Update inventory". For more info, see {% link "Updating product properties (price, stock quantity, etc.) via import" ref_OEpBdtQ6 %}.

The **Update inventory** module by X-Cart team provides a quick and easy way to update product quantities by importing a simple [CSV](https://en.wikipedia.org/wiki/Comma-separated_values) file. This module works for both regular products and {% link "product variants" ref_0uApuQfx %}.

 ![]({{site.baseurl}}/attachments/9306477/9438200.png?effects=drop-shadow)

 The required CSV file format for importing product quantity information is as follows:

![]({{site.baseurl}}/attachments/9306477/9438201.png?effects=drop-shadow)

As you can see, the CSV file has just two fields:

| Field in CSV file | What this field describes | Value type |
| 

**sku **

 | Unique identifier of the product or variant | String,
Max. length: 32 |
| **qty** | Stock level | Positive integer |

In a store with the module Update inventory installed and enabled, the CSV file for updating product quantities can be imported via the Update quantity section (**Catalog** > **Update quantity**):

![]({{site.baseurl}}/attachments/9306477/9438202.png?effects=drop-shadow)

When importing a CSV file to update product quantities, the following rules apply:

*   If a SKU from the CSV file cannot be matched to the SKU of any existing product or (when using the module Product Variants) product variant  in the store's database, the error is logged, and the respective line in the CSV file is skipped.
*   Product quantities have to be positive numbers. If a product quantity in the qty field is specified in a wrong format, the error is logged, and the respective line in the CSV file is skipped.
*   Any errors generated in the process of importing the CSV file with SKUs and quantities are displayed after the import process has been completed.

_Related pages:_

*   {% link "Import-Export" ref_TANvG2De %}

*   {% link "Product variants" Product-variants_7504786.html %}

*   {% link "Updating product properties (price, stock quantity, etc.) via import" 9306814.html %}

## Attachments:

* [xc5_update_inventory_module.png]({{site.baseurl}}/attachments/9306477/9438200.png) (image/png)
* [xc5_update_inventory_csv_format.png]({{site.baseurl}}/attachments/9306477/9438201.png) (image/png)
* [xc5_update_quantity_section.png]({{site.baseurl}}/attachments/9306477/9438203.png) (image/png)
* [xc5_update_quantity_section.png]({{site.baseurl}}/attachments/9306477/9438202.png) (image/png)