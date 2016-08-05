---
identifier: ref_Z7XdREZl
updated_at: 2016-06-16 00:00
layout: article_with_sidebar
lang: en
title: 'CSV import: Product attribute values'
categories:
  - User manual

---


Below is a list of supported fields and their respective value types for the import of product attribute values:

| Field in CSV file | What this field describes | {% link "Value type" ref_2LwMTTTW %}** |
| _Fields supported by **X-Cart core**_ |
| **productSKU*** | SKU of the product which has this attribute value. Serves as a part of unique identifier. | 

String,
Max. length: 32 

 |
| **type*** | 

Type of the attribute. Possible values are:

*   T - Text
*   S - Select
*   C - Yes/No

 | Enum |
| ***name** | Text representation of the attribute. Serves as a part of unique identifier. | String,
Multilingual,
Max. length: 255 |
| class | Attribute class. Serves as a part of unique identifier. | String,
Multilingual,
Max. length: 255 |
| group | Attribute group. Can be blank. Serves as a part of unique identifier. | String,
Multilingual,
Max. length: 255  |
| owner | 

Yes if the attribute value is introduced locally by product, but not class or global attribute; otherwise No.

 | Yes/No |
| ***value** | 

Actual attribute value

 | String |
| priceModifer | Modifier of the product price. Should be written with a sign, either positive or negative (e.g. +1.5) | Signed float |
| weightModifier | Modifier of the product weight. Should be written with a sign, either positive or negative (e.g. +1.5) | Signed float |
| editable | Applied only if type is Text. Indicates that this value is editable by customer on the product page. | String |

<sub>* Required field.</sub>

<sub>** See {% link "CSV field attributes" ref_2LwMTTTW %} for more info.</sub>

**Tips**:

*   If you are going to import data into X-Cart and do not wish to update certain X-Cart fields during the import process, you should not include these fields into your CSV file for import. Simply remove the respective column(s) from the file.