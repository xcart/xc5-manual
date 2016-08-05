---
identifier: ref_JobVfzZg
updated_at: 2016-06-16 00:00
layout: article_with_sidebar
lang: en
title: 'CSV import: Customers'
categories:
  - User manual

---


Below is a list of supported fields and their respective value types for the import of customers:

| Field in CSV file | What this field describes | {% link "Value type" ref_2LwMTTTW %}** |
| _Fields supported by **X-Cart core**_ |
| **login*** | Unique identifier of the user. Email is used as login. | 

String,
Max. length: 128

 |
| **status*** | 

User status. Possible values are:

*   E - user is enabled;
*   D - user is disabled.

 | Enum |
| added | Service field containing the date of registration | Date |
| firstLogin | Service field containing the date of first successful login | Date |
| lastLogin | Service field containing the date of last successful login | Date |
| referer | Referer link |   |
| language | Two-symbol code of the language (e.g. **en**) | 

String,
Max. length: 2 

 |
| membership | Membership of the user | String |
| password | Password. Will be encrypted and stored as a hash. | String |
| forceChangePassword | Should be Yes if user is required to change his password on next logon and No otherwise. | Yes/No |
| addressField | 

Very special service field. Has a row on each address and a column on each address part, such as zipcode. Column name is combined from part name and 'addressField' word.

Example:

| login | cityAddressField | countryCodeAddressField | stateAddressField | zipcodeAddressField | phoneAddressField |
| {% link "greg.bowes@gmail.com" mailto:greg.bowes@gmail.com %} | Edmond | US | Oklahoma | 73003 | 123456789 |
|   | Richmond Hill | CA | Ontario | L4C5L4 | 905-508-3521 |

 | 

Multicolumn,
Multirow

 |

<sub>* Required field.</sub>

<sub>** See {% link "CSV field attributes" ref_2LwMTTTW %} for more info.</sub>

**Tips**: 

*   If you are going to import data into X-Cart and do not wish to update certain X-Cart fields during the import process, you should not include these fields into your CSV file for import. Simply remove the respective column(s) from the file.