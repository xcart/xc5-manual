---
identifier: ref_ErThmVXU
updated_at: 2016-06-16 00:00
layout: article_with_sidebar
lang: en
title: 'CSV import: Customers'
categories:
  - User manual

---


Below is a list of supported fields and their respective value types for the import of customers:

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

<td colspan="1" class="confluenceTd">**login***</td>

<td colspan="1" class="confluenceTd">Unique identifier of the user. Email is used as login.</td>

<td colspan="1" class="confluenceTd">

String,  
Max. length: 128

</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">**status***</td>

<td colspan="1" class="confluenceTd">

User status. Possible values are:

*   E - user is enabled;
*   D - user is disabled.

</td>

<td colspan="1" class="confluenceTd">Enum</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">added</td>

<td colspan="1" class="confluenceTd">Service field containing the date of registration</td>

<td colspan="1" class="confluenceTd">Date</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">firstLogin</td>

<td colspan="1" class="confluenceTd">Service field containing the date of first successful login</td>

<td colspan="1" class="confluenceTd">Date</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">lastLogin</td>

<td colspan="1" class="confluenceTd">Service field containing the date of last successful login</td>

<td colspan="1" class="confluenceTd">Date</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">referer</td>

<td colspan="1" class="confluenceTd">Referer link</td>

<td colspan="1" class="confluenceTd"> </td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">language</td>

<td colspan="1" class="confluenceTd">Two-symbol code of the language (e.g. **en**)</td>

<td colspan="1" class="confluenceTd">

String,  
Max. length: 2 

</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">membership</td>

<td colspan="1" class="confluenceTd">Membership of the user</td>

<td colspan="1" class="confluenceTd">String</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">password</td>

<td colspan="1" class="confluenceTd">Password. Will be encrypted and stored as a hash.</td>

<td colspan="1" class="confluenceTd">String</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">forceChangePassword</td>

<td colspan="1" class="confluenceTd">Should be Yes if user is required to change his password on next logon and No otherwise.</td>

<td colspan="1" class="confluenceTd">Yes/No</td>

</tr>

<tr>

<td class="confluenceTd">addressField</td>

<td class="confluenceTd">

Very special service field. Has a row on each address and a column on each address part, such as zipcode. Column name is combined from part name and 'addressField' word.

Example:

<table class="confluenceTable">

<tbody>

<tr>

<td colspan="1" class="confluenceTd">login</td>

<td class="confluenceTd">cityAddressField</td>

<td class="confluenceTd">countryCodeAddressField</td>

<td class="confluenceTd">stateAddressField</td>

<td class="confluenceTd">zipcodeAddressField</td>

<td class="confluenceTd">phoneAddressField</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd">{% link "greg.bowes@gmail.com" mailto:greg.bowes@gmail.com %}</td>

<td class="confluenceTd">Edmond</td>

<td class="confluenceTd">US</td>

<td class="confluenceTd">Oklahoma</td>

<td class="confluenceTd">73003</td>

<td class="confluenceTd">123456789</td>

</tr>

<tr>

<td colspan="1" class="confluenceTd"> </td>

<td class="confluenceTd">Richmond Hill</td>

<td class="confluenceTd">CA</td>

<td class="confluenceTd">Ontario</td>

<td class="confluenceTd">L4C5L4</td>

<td class="confluenceTd">905-508-3521</td>

</tr>

</tbody>

</table>

</td>

<td class="confluenceTd">

Multicolumn,  
Multirow

</td>

</tr>

</tbody>

</table>

<sub>* Required field.</sub>

<sub>** See {% link "CSV field attributes" CSV-field-attributes_9306552.html %} for more info.</sub>

**Tips**: 

*   If you are going to import data into X-Cart and do not wish to update certain X-Cart fields during the import process, you should not include these fields into your CSV file for import. Simply remove the respective column(s) from the file.