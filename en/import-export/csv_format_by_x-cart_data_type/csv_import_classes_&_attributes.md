---
identifier: ref_XL9cXXMB
updated_at: 2016-06-16 00:00
layout: article_with_sidebar
lang: en
title: 'CSV import: Classes &amp; Attributes'
categories:
  - User manual

---


Below is a list of supported fields and their respective value types for the import of product classes and attributes.

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

<td colspan="1" class="confluenceTd">position</td>

<td colspan="1" class="confluenceTd">Internal value of the attribute order. Should not be negative. Lower number means higher place in order.</td>

<td colspan="1" class="confluenceTd">

Integer

</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">product</td>

<td colspan="1" class="confluenceTd">

SKU of the product, if it is a product attribute. Leave blank for global.

</td>

<td colspan="1" class="confluenceTd">String,  
Max. length: 32 </td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">**name***</td>

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

<td colspan="1" class="confluenceTd">options</td>

<td colspan="1" class="confluenceTd">

List of possible attribute options. Options are separated with **'&&'** symbol.

Example: S&&M&&L&&XL&&XXL&&XXXL

</td>

<td colspan="1" class="confluenceTd">String  
Multiple,  
Multilingual,  
Max. length: 255</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">**type***</td>

<td colspan="1" class="confluenceTd">

Type of the attribute. Possible values are:

*   T - Text
*   S - Select
*   C - Yes/No

</td>

<td colspan="1" class="confluenceTd">Enum</td>

</tr>

</tbody>

</table>

<sub>* Required field.</sub>

<sub>** See {% link "CSV field attributes" CSV-field-attributes_9306552.html %} for more info.</sub>

**Tips**:

*   If you are going to import data into X-Cart and do not wish to update certain X-Cart fields during the import process, you should not include these fields into your CSV file for import. Simply remove the respective column(s) from the file.  

*   If necessary, import can be used to clear previously set field values from non-numeric fields. To clear a field value via import, in your CSV file to be imported specify the value of the field as "NULL". After the import process is completed, the fields in which the value "NULL" has been imported will be cleared. This feature is supported by the attribute options field.