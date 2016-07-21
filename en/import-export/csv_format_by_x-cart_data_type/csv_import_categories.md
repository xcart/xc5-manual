---
identifier: ref_AQ5lnWqL
updated_at: 2016-06-16 00:00
layout: article_with_sidebar
lang: en
title: 'CSV import: Categories'
categories:
  - User manual

---


Below is a list of supported fields and their respective value types for category import.

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

<td colspan="1" class="confluenceTd">**path***</td>

<td colspan="1" class="confluenceTd">Path to category. Serves as identifier.  
Example: Toys >>> Science Toys </td>

<td colspan="1" class="confluenceTd">

String,  
Max. length: 32

</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">enabled</td>

<td colspan="1" class="confluenceTd">Is the category enabled?</td>

<td colspan="1" class="confluenceTd">Yes/No</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">showTitle</td>

<td colspan="1" class="confluenceTd">Option to show category title</td>

<td colspan="1" class="confluenceTd">Yes/No</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">position</td>

<td colspan="1" class="confluenceTd">Internal value of the category order. May not be negative. A smaller number means a higher position in the order.</td>

<td colspan="1" class="confluenceTd">Integer</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">memberships</td>

<td colspan="1" class="confluenceTd">Membership types, which members can see the category. Do not set it if you want to make the category visible to all customers. Otherwise, it will be visible to the users assigned to specified membership only.</td>

<td colspan="1" class="confluenceTd">String,  
Multiple </td>

</tr>

<tr>

<td class="confluenceTd">image</td>

<td class="confluenceTd">

Location of the image representing the category. This can be one of the following:

*   Image URL
*   Path to the image on the server relative to the <xcart directory>/var/import folder; for example, images/categories/image1.png.

When exporting data from X-Cart, image paths are written to the export file using the latter method (relative path). This way when you need to re-import images back into X-Cart, you simply move the folder <xcart directory>/var/export/images to var/import/ - and use the existing relative paths).

</td>

<td class="confluenceTd">String</td>

</tr>

<tr>

<td class="confluenceTd">cleanURL</td>

<td class="confluenceTd">

SEO friendly URL of the category page.

Example: toys

</td>

<td class="confluenceTd">String</td>

</tr>

<tr>

<td class="confluenceTd">***name**</td>

<td class="confluenceTd">Category name.</td>

<td class="confluenceTd">String,  
Multilingual </td>

</tr>

<tr>

<td class="confluenceTd">description</td>

<td colspan="1" class="confluenceTd">Full description of the category.</td>

<td colspan="1" class="confluenceTd">

String,  
Multilingual,  
HTML allowed 

</td>

</tr>

<tr>

<td class="confluenceTd">metaTags</td>

<td class="confluenceTd">Defines the content of <meta name="keywords" content="%value%"> meta tag</td>

<td class="confluenceTd">String,  
Multilingual,  
Max. length: 255 </td>

</tr>

<tr>

<td class="confluenceTd">metaDesc</td>

<td class="confluenceTd">Defines the content of <meta name="description" content="%value%"> meta tag</td>

<td class="confluenceTd">String,  
Multilingual </td>

</tr>

<tr>

<td class="confluenceTd">metaDescType</td>

<td class="confluenceTd">

Defines meta description content type. Can be either **A** or **C**, where:

*   **A** stands for automatic mode when meta description will be generated from category description;
*   C stands for custom mode when meta desciption will be taken from **metaDesc_*** field in appropriate translation*;  
    *this means that if the store is in _English_ language, meta description will be taken from **metaDesc_en** field.

</td>

<td class="confluenceTd">String,  
Max. length: 1 </td>

</tr>

<tr>

<td class="confluenceTd">metaTitle</td>

<td class="confluenceTd">Defines the content of <meta name="title" content="%value%"> meta tag</td>

<td class="confluenceTd">String,  
Multilingual,  
Max. length: 255 </td>

</tr>

<tr>

<td colspan="3" class="confluenceTd">_Fields added by **GoSocial** module_</td>

</tr>

<tr>

<td class="confluenceTd">useCustomOpenGraphMeta</td>

<td class="confluenceTd">Defines whether use custom Open Graph meta tags for this product or use default ones</td>

<td class="confluenceTd">Yes/No</td>

</tr>

<tr>

<td class="confluenceTd">openGraphMeta</td>

<td class="confluenceTd">If **useCustomOpenGraphMeta** is **Yes**, then defines custom Open Graph meta tags</td>

<td class="confluenceTd">

String,  
HTML allowed,  
Scripting allowed 

</td>

</tr>

<tr>

<td colspan="3" class="confluenceTd">_Fields added by **Product Filter** module_</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">productClasses</td>

<td colspan="1" class="confluenceTd"> </td>

<td colspan="1" class="confluenceTd"> </td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">useClasses</td>

<td colspan="1" class="confluenceTd"> </td>

<td colspan="1" class="confluenceTd"> </td>

</tr>

</tbody>

</table>

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