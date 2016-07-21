---
identifier: ref_MwVcuG1v
updated_at: 2016-06-16 00:00
layout: article_with_sidebar
lang: en
title: 'CSV import: Product attribute values'
categories:
  - User manual

---


Below is a list of supported fields and their respective value types for the import of product attribute values:

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

<td colspan="1" class="confluenceTd">**productSKU***</td>

<td colspan="1" class="confluenceTd">SKU of the product which has this attribute value. Serves as a part of unique identifier.</td>

<td colspan="1" class="confluenceTd">

String,  
Max. length: 32 

</td>

</tr>

<tr>

<td class="confluenceTd">**type***</td>

<td class="confluenceTd">

Type of the attribute. Possible values are:

*   T - Text
*   S - Select
*   C - Yes/No

</td>

<td class="confluenceTd">Enum</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">***name**</td>

<td colspan="1" class="confluenceTd">Text representation of the attribute. Serves as a part of unique identifier.</td>

<td colspan="1" class="confluenceTd">String,  
Multilingual,  
Max. length: 255</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">class</td>

<td colspan="1" class="confluenceTd">Attribute class. Serves as a part of unique identifier.</td>

<td colspan="1" class="confluenceTd">String,  
Multilingual,  
Max. length: 255</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">group</td>

<td colspan="1" class="confluenceTd">Attribute group. Can be blank. Serves as a part of unique identifier.</td>

<td colspan="1" class="confluenceTd">String,  
Multilingual,  
Max. length: 255 </td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">owner</td>

<td colspan="1" class="confluenceTd">

Yes if the attribute value is introduced locally by product, but not class or global attribute; otherwise No.

</td>

<td colspan="1" class="confluenceTd">Yes/No</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">***value**</td>

<td colspan="1" class="confluenceTd">

Actual attribute value

</td>

<td colspan="1" class="confluenceTd">String</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">priceModifer</td>

<td colspan="1" class="confluenceTd">Modifier of the product price. Should be written with a sign, either positive or negative (e.g. +1.5)</td>

<td colspan="1" class="confluenceTd">Signed float</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">weightModifier</td>

<td colspan="1" class="confluenceTd">Modifier of the product weight. Should be written with a sign, either positive or negative (e.g. +1.5)</td>

<td colspan="1" class="confluenceTd">Signed float</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">editable</td>

<td colspan="1" class="confluenceTd">Applied only if type is Text. Indicates that this value is editable by customer on the product page.</td>

<td colspan="1" class="confluenceTd">String</td>

</tr>

</tbody>

</table>

<sub>* Required field.</sub>

<sub>** See {% link "CSV field attributes" CSV-field-attributes_9306552.html %} for more info.</sub>

**Tips**:

*   If you are going to import data into X-Cart and do not wish to update certain X-Cart fields during the import process, you should not include these fields into your CSV file for import. Simply remove the respective column(s) from the file.