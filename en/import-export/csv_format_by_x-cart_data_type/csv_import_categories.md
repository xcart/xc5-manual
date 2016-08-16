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

<table class="ui celled padded compact small table">
  <thead>
    <tr>
      <th class="confluenceTh">Field in CSV file</th>
      <th colspan="1" class="confluenceTh">What this field describes</th>
      <th colspan="1" class="confluenceTh" markdown="1">{% link 'Value type' ref_2LwMTTTW %}</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td colspan="3" class="confluenceTd"><em> Fields supported by <strong>X-Cart core</strong></em>
      </td>
    </tr>
    <tr>
      <td colspan="1" class="confluenceTd"><strong>path*</strong>
      </td>
      <td colspan="1" class="confluenceTd">Path to category. Serves as identifier.
        <br>Example: Toys &gt;&gt;&gt; Science Toys&nbsp;</td>
      <td colspan="1" class="confluenceTd">
        <p>String,
          <br>Max. length: 32</p>
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
      <td colspan="1" class="confluenceTd">Membership types, which members can see the category. <span style="color: rgb(0,0,0);">Do not set it if you want to make the category visible to all customers. Otherwise, it will be visible to the users assigned to specified membership only.</span>
      </td>
      <td colspan="1" class="confluenceTd">String,
        <br>Multiple&nbsp;</td>
    </tr>
    <tr>
      <td class="confluenceTd">image</td>
      <td class="confluenceTd">
        <p>Location of the image representing the category. This can be one of the following:</p>
        <ul>
          <li>Image URL</li>
          <li>Path to the image on the server relative to the &lt;xcart directory&gt;/var/import folder; for example,&nbsp;images/categories/image1.png.</li>
        </ul>
        <p>When exporting data from X-Cart, image paths are written to the export file using the latter method (relative path). This way when you need to re-import images back into X-Cart, you simply move the folder &lt;xcart directory&gt;/var/export/images to var/import/ - and use the existing relative paths).</p>
      </td>
      <td class="confluenceTd">String</td>
    </tr>
    <tr>
      <td class="confluenceTd">cleanURL</td>
      <td class="confluenceTd">
        <p>SEO friendly URL of the category page.</p>
        <p>Example: toys</p>
      </td>
      <td class="confluenceTd">String</td>
    </tr>
    <tr>
      <td class="confluenceTd"><strong>*name</strong>
      </td>
      <td class="confluenceTd">Category name.</td>
      <td class="confluenceTd">String,
        <br>Multilingual&nbsp;</td>
    </tr>
    <tr>
      <td class="confluenceTd">description</td>
      <td colspan="1" class="confluenceTd">Full description of the category.</td>
      <td colspan="1" class="confluenceTd">
        <p>String,
          <br>Multilingual,
          <br>HTML allowed&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td class="confluenceTd">metaTags</td>
      <td class="confluenceTd"><span>Defines the content of &lt;meta name="keywords" content="%value%"&gt; meta tag</span>
      </td>
      <td class="confluenceTd">String,
        <br>Multilingual,
        <br>Max. length: 255&nbsp;</td>
    </tr>
    <tr>
      <td class="confluenceTd">metaDesc</td>
      <td class="confluenceTd">Defines the content of &lt;meta name="description" content="%value%"&gt; meta tag</td>
      <td class="confluenceTd">String,
        <br>Multilingual&nbsp;</td>
    </tr>
    <tr>
      <td class="confluenceTd">metaDescType</td>
      <td class="confluenceTd">
        <p>Defines meta description content type. Can be either <strong>A </strong>or <strong>C</strong>, where:</p>
        <ul>
          <li><strong>A</strong> stands for automatic mode when meta description will be generated from category description;</li>
          <li>C stands for custom mode when meta desciption will be taken from <strong>metaDesc_* </strong>field in appropriate translation*;
            <br>*this means that if the store is in <em>English</em> language, meta description will be taken from <strong>metaDesc_en</strong> field.</li>
        </ul>
      </td>
      <td class="confluenceTd">String,
        <br>Max. length: 1&nbsp;</td>
    </tr>
    <tr>
      <td class="confluenceTd">metaTitle</td>
      <td class="confluenceTd"><span>Defines the content of &lt;meta name="title" content="%value%"&gt; meta tag</span>
      </td>
      <td class="confluenceTd">String<span>,</span>
        <br><span>Multilingual,</span>
        <br><span>Max. length: 255&nbsp;</span>
      </td>
    </tr>
    <tr>
      <td colspan="3" class="confluenceTd"><em>Fields added by <strong>GoSocial</strong> module</em>
      </td>
    </tr>
    <tr>
      <td class="confluenceTd"><span><span>useCustomOpenGraphMeta</span></span>
      </td>
      <td class="confluenceTd">Defines whether use custom Open Graph meta tags for this product or use default ones</td>
      <td class="confluenceTd">Yes/No</td>
    </tr>
    <tr>
      <td class="confluenceTd"><span>openGraphMeta</span>
      </td>
      <td class="confluenceTd">If <strong><span>useCustomOpenGraphMeta</span></strong> is <strong>Yes</strong>, then defines custom Open Graph meta tags</td>
      <td class="confluenceTd">
        <p>String,
          <br>HTML allowed,
          <br>Scripting allowed&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td colspan="3" class="confluenceTd"><em>Fields added by <strong>Product Filter</strong> module</em>
      </td>
    </tr>
    <tr>
      <td colspan="1" class="confluenceTd">productClasses</td>
      <td colspan="1" class="confluenceTd">&nbsp;</td>
      <td colspan="1" class="confluenceTd">&nbsp;</td>
    </tr>
    <tr>
      <td colspan="1" class="confluenceTd">useClasses</td>
      <td colspan="1" class="confluenceTd">&nbsp;</td>
      <td colspan="1" class="confluenceTd">&nbsp;</td>
    </tr>
  </tbody>
</table>

<sub>* Required field.</sub>

<sub markdown="1">** See CSV field attributes for more info.</sub>

**Tips**:

*   If you are going to import data into X-Cart and do not wish to update certain X-Cart fields during the import process, you should not include these fields into your CSV file for import. Simply remove the respective column(s) from the file.

*   If necessary, import can be used to clear previously set field values from non-numeric fields. To clear a field value via import, in your CSV file to be imported specify the value of the field as "NULL". After the import process is completed, the fields in which the value "NULL" has been imported will be cleared. 

    This feature is supported by the following fields pertaining to categories:

    *   memberships;
    *   image;
    *   banner;
    *   productClasses (processed by the module Product Filter).