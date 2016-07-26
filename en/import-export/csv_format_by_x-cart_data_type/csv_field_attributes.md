---
identifier: ref_2LwMTTTW
updated_at: 2016-01-26 00:00
layout: article_with_sidebar
lang: en
title: 'CSV field attributes'
categories:
  - User manual

---


Below is an explanation of some attributes that we use to describe specific fields in an import CSV file from the viewpoint of value type that can be imported through them. Use this information to read the CSV format tables in the following sections:

*   {% link "CSV import: Products" ref_WmJBfwxA %}
*   {% link "CSV import: Classes & Attributes" ref_qTbDu6Ov %}
*   {% link "CSV import: Product attribute values" ref_Z7XdREZl %}
*   {% link "CSV import: Categories" ref_ekmg5iLG %}
*   {% link "CSV import: Customers" ref_JobVfzZg %}

| Field attribute | Description | Example |
| Value format | 

The format you need to follow when setting a value for the field. The most common formats are **String, Integer, Float, Yes/No (Boolean), Enum** and **Date**.
**Date** is specified in **php** `strtotime()` format.

 | 

Some text (String)
100 (Integer)
0.39 (Float)
1 Jan 2013 (Date)
Yes (Yes/No) 

 |
| Max. length | The field has a limit on the number of characters that can be entered into it. | Max. length: 32
(This means that the field can be 32 chars long max) |
| Multilingual | The field contains language labels. Fields with this attribute are language-specific, and their names are formed according to the format `<field>_<language>` (for example, **name_en**). A single CSV file may contain multiple columns with the same field name but different languages (for example. **name_en**, **name_ru**, **name_de**). | n/a |
| HTML allowed | The field may contain HTML tags for layouting. Most typically, there is a WYSIWYG editor in the Admin back end for this field. | <h5>It's HTML TEXT!</h5> |
| Scripting allowed  | The field may contain anything, even <script> tags. | n/a |
| Multiple | This attribute shows that the field can have multiple values. You must separate each value with **'&&'** symbol. | Wholesaler&&Clubmember |
| Multirow | The field may contain multiple rows of values. Each multirow value must be vertically adjacent. | 

| SKU1 | Variant1 |
|   | Variant2 |
|   | Variant3 |
| SKU2 | Variant1 |

 |