---
identifier: ref_ekmg5iLG
updated_at: 2016-06-16 00:00
layout: article_with_sidebar
lang: en
title: 'CSV import: Categories'
categories:
  - User manual

---


Below is a list of supported fields and their respective value types for category import.

| Field in CSV file | What this field describes | {% link "Value type" ref_2LwMTTTW %}** |
| _Fields supported by **X-Cart core**_ |
| **path*** | Path to category. Serves as identifier.
Example: Toys >>> Science Toys  | 

String,
Max. length: 32

 |
| enabled | Is the category enabled? | Yes/No |
| showTitle | Option to show category title | Yes/No |
| position | Internal value of the category order. May not be negative. A smaller number means a higher position in the order. | Integer |
| memberships | Membership types, which members can see the category. Do not set it if you want to make the category visible to all customers. Otherwise, it will be visible to the users assigned to specified membership only. | String,
Multiple  |
| image | 

Location of the image representing the category. This can be one of the following:

*   Image URL
*   Path to the image on the server relative to the <xcart directory>/var/import folder; for example, images/categories/image1.png.

When exporting data from X-Cart, image paths are written to the export file using the latter method (relative path). This way when you need to re-import images back into X-Cart, you simply move the folder <xcart directory>/var/export/images to var/import/ - and use the existing relative paths).

 | String |
| cleanURL | 

SEO friendly URL of the category page.

Example: toys

 | String |
| ***name** | Category name. | String,
Multilingual  |
| description | Full description of the category. | 

String,
Multilingual,
HTML allowed 

 |
| metaTags | Defines the content of <meta name="keywords" content="%value%"> meta tag | String,
Multilingual,
Max. length: 255  |
| metaDesc | Defines the content of <meta name="description" content="%value%"> meta tag | String,
Multilingual  |
| metaDescType | 

Defines meta description content type. Can be either **A** or **C**, where:

*   **A** stands for automatic mode when meta description will be generated from category description;
*   C stands for custom mode when meta desciption will be taken from **metaDesc_*** field in appropriate translation*;
    *this means that if the store is in _English_ language, meta description will be taken from **metaDesc_en** field.

 | String,
Max. length: 1  |
| metaTitle | Defines the content of <meta name="title" content="%value%"> meta tag | String,
Multilingual,
Max. length: 255  |
| _Fields added by **GoSocial** module_ |
| useCustomOpenGraphMeta | Defines whether use custom Open Graph meta tags for this product or use default ones | Yes/No |
| openGraphMeta | If **useCustomOpenGraphMeta** is **Yes**, then defines custom Open Graph meta tags | 

String,
HTML allowed,
Scripting allowed 

 |
| _Fields added by **Product Filter** module_ |
| productClasses |   |   |
| useClasses |   |   |

<sub>* Required field.</sub>

<sub>** See CSV field attributes for more info.</sub>

**Tips**:

*   If you are going to import data into X-Cart and do not wish to update certain X-Cart fields during the import process, you should not include these fields into your CSV file for import. Simply remove the respective column(s) from the file.

*   If necessary, import can be used to clear previously set field values from non-numeric fields. To clear a field value via import, in your CSV file to be imported specify the value of the field as "NULL". After the import process is completed, the fields in which the value "NULL" has been imported will be cleared. 
    This feature is supported by the following fields pertaining to categories:
    - memberships;
    - image;
    - banner;
    - productClasses (processed by the module Product Filter).