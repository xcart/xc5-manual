---
identifier: ref_Q4IypyMu
updated_at: 2016-01-26 00:00
layout: article_with_sidebar
lang: en
title: 'CSV field attributes'
categories:
  - User manual

---


Below is an explanation of some attributes that we use to describe specific fields in an import CSV file from the viewpoint of value type that can be imported through them. Use this information to read the CSV format tables in the following sections:

*   {% link "CSV import: Products" ref_ZIASzvfX %}
*   {% link "CSV import: Classes & Attributes" ref_XL9cXXMB %}
*   {% link "CSV import: Product attribute values" ref_MwVcuG1v %}
*   {% link "CSV import: Categories" ref_AQ5lnWqL %}
*   {% link "CSV import: Customers" ref_ErThmVXU %}

<table class="confluenceTable">

<tbody>

<tr>

<th class="confluenceTh">Field attribute</th>

<th class="confluenceTh">Description</th>

<th class="confluenceTh">Example</th>

</tr>

<tr>

<td class="confluenceTd">Value format</td>

<td class="confluenceTd">

The format you need to follow when setting a value for the field. The most common formats are **String, Integer, Float, Yes/No (Boolean), Enum** and **Date**.  
**Date** is specified in **php** `strtotime()` format.

</td>

<td class="confluenceTd">

Some text (String)  
100 (Integer)  
0.39 (Float)  
1 Jan 2013 (Date)  
Yes (Yes/No) 

</td>

</tr>

<tr>

<td class="confluenceTd">Max. length</td>

<td class="confluenceTd">The field has a limit on the number of characters that can be entered into it.</td>

<td class="confluenceTd">Max. length: 32  
(This means that the field can be 32 chars long max)</td>

</tr>

<tr>

<td class="confluenceTd">Multilingual</td>

<td class="confluenceTd">The field contains language labels. Fields with this attribute are language-specific, and their names are formed according to the format `<field>_<language>` (for example, **name_en**). A single CSV file may contain multiple columns with the same field name but different languages (for example. **name_en**, **name_ru**, **name_de**).</td>

<td class="confluenceTd">n/a</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">HTML allowed</td>

<td colspan="1" class="confluenceTd">The field may contain HTML tags for layouting. Most typically, there is a WYSIWYG editor in the Admin back end for this field.</td>

<td colspan="1" class="confluenceTd"><h5>It's HTML TEXT!</h5></td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">Scripting allowed </td>

<td colspan="1" class="confluenceTd">The field may contain anything, even <script> tags.</td>

<td colspan="1" class="confluenceTd">n/a</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">Multiple</td>

<td colspan="1" class="confluenceTd">This attribute shows that the field can have multiple values. You must separate each value with **'&&'** symbol.</td>

<td colspan="1" class="confluenceTd">Wholesaler&&Clubmember</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">Multirow</td>

<td colspan="1" class="confluenceTd">The field may contain multiple rows of values. Each multirow value must be vertically adjacent.</td>

<td colspan="1" class="confluenceTd">

<table class="confluenceTable">

<tbody>

<tr>

<td class="confluenceTd">SKU1</td>

<td class="confluenceTd">Variant1</td>

</tr>

<tr>

<td class="confluenceTd"> </td>

<td class="confluenceTd">Variant2</td>

</tr>

<tr>

<td class="confluenceTd"> </td>

<td class="confluenceTd">Variant3</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">SKU2</td>

<td colspan="1" class="confluenceTd">Variant1</td>

</tr>

</tbody>

</table>

</td>

</tr>

</tbody>

</table>