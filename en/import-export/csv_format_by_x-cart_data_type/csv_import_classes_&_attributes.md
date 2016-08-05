---
identifier: ref_qTbDu6Ov
updated_at: 2016-06-16 00:00
layout: article_with_sidebar
lang: en
title: 'CSV import: Classes &amp; Attributes'
categories:
  - User manual

---


Below is a list of supported fields and their respective value types for the import of product classes and attributes.

| Field in CSV file | What this field describes | {% link "Value type" ref_2LwMTTTW %}** |
| _Fields supported by **X-Cart core**_ |
| position | Internal value of the attribute order. Should not be negative. Lower number means higher place in order. | 

Integer

 |
| product | 

SKU of the product, if it is a product attribute. Leave blank for global.

 | String,
Max. length: 32  |
| **name*** | Text representation of the attribute. Serves as a part of unique identifier. | String,
Multilingual,
Max. length: 255 |
| class | Attribute class. Serves as a part of unique identifier. | String,
Multilingual,
Max. length: 255 |
| group | Attribute group. Can be blank. Serves as a part of unique identifier. | String,
Multilingual,
Max. length: 255  |
| options | 

List of possible attribute options. Options are separated with **'&&'** symbol.

Example: S&&M&&L&&XL&&XXL&&XXXL

 | String
Multiple,
Multilingual,
Max. length: 255 |
| **type*** | 

Type of the attribute. Possible values are:

*   T - Text
*   S - Select
*   C - Yes/No

 | Enum |

<sub>* Required field.</sub>

<sub>** See {% link "CSV field attributes" ref_2LwMTTTW %} for more info.</sub>

**Tips**:

*   If you are going to import data into X-Cart and do not wish to update certain X-Cart fields during the import process, you should not include these fields into your CSV file for import. Simply remove the respective column(s) from the file.

*   If necessary, import can be used to clear previously set field values from non-numeric fields. To clear a field value via import, in your CSV file to be imported specify the value of the field as "NULL". After the import process is completed, the fields in which the value "NULL" has been imported will be cleared. This feature is supported by the attribute options field.