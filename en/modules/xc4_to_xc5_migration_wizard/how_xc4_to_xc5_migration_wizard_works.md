---
lang: en
layout: article_with_sidebar
updated_at: '2016-10-04 12:50 +0400'
identifier: ref_37NAeGlf
title: ''
order: 100
published: false
---
## Data types migratable by XC4 to XC5 Migration wizard

<table class="ui compact padded celled small table">
  <tbody>
    <tr>
      <th colspan="1" class="confluenceTh">&nbsp;</th>
      <th colspan="1" class="confluenceTh">&nbsp;</th>
    </tr>
    <tr>
      <td colspan="1" class="confluenceTd"><span>Сonfiguration settings</span>
      </td>
      <td colspan="1" class="confluenceTd">
        <p>*   Company;
          <br><span>&nbsp;</span>
          <br>*   General (Default customer address, Currency, Weight, Length symbols, Purchase limits);
          <br><span>&nbsp;</span>
          <br>*   Contact Us (If your X-Cart 4 database contains an entry for contact_us, the Migration wizard requests that the module "Contact Us" should be enabled in X-Cart 5; your X-Cart 4 store's Contact Us form settings are not checked and not migrated to X-Cart 5);
          <br><span>&nbsp;</span>
          <br>*   CleanURLs (If your X-Cart 4 store has the Clean URLs feature enabled, the Migration wizard automatically enables Clean URLs in X-Cart 5.)&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td colspan="1" class="confluenceTd"><span>Сontent</span>
      </td>
      <td colspan="1" class="confluenceTd">
        <p>*   Static pages (Only embedded ones; if such pages are present in X-Cart 4, the Migration wizard requires that the module "SimpleCMS" should be enabled in X-Cart 5);
          <br><span>&nbsp;</span>
          <br>*   Speed bar (In X-Cart 5, similar functionality is available through the module "SimpleCMS", so if the feature is used in X-Cart 4, the Migration wizard requires that the module "SimpleCMS" should be enabled in X-Cart 5).&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td colspan="1" class="confluenceTd"><span>Products</span>
      </td>
      <td colspan="1" class="confluenceTd">
        <p>All the general info, images and Clean URLs for the following entities:
          <br><span>&nbsp;</span>
          <br>*   Bestsellers (If the feature is used in X-Cart 4, the Migration wizard requires that the module "Bestsellers" should be enabled in X-Cart 5; your X-Cart 4 store's Bestsellers settings are not checked and not migrated to X-Cart 5);
          <br><span>&nbsp;</span>
          <br>*   Detailed product images;
          <br><span>&nbsp;</span>
          <br>*   Extra fields;
          <br><span>&nbsp;</span>
          <br>*   Feature comparison;
          <br><span>&nbsp;</span>
          <br>*   International descriptions;
          <br><span>&nbsp;</span>
          <br>*   Market price;
          <br><span>&nbsp;</span>
          <br>*   Product options (including variants and variant images);
          <br><span>&nbsp;</span>
          <br>*   Product reviews;
          <br><span>&nbsp;</span>
          <br>*   Related products;
          <br><span>&nbsp;</span>
          <br>*   Wholesale prices (Only for regular products: migration of wholesale prices of product variants is not yet supported).&nbsp;</p>
      </td>
    </tr>  
    <tr>
      <td colspan="1" class="confluenceTd"><span>Categories</span>
      </td>
      <td colspan="1" class="confluenceTd">
        <p>All the general info, images and Clean URLs for the following entities:
          <br><span>&nbsp;</span>
          <br>*   International descriptions;
          <br><span>&nbsp;</span>
          <br>*   Featured products.&nbsp;</p>
      </td>
    </tr>
    <tr>   
      <td colspan="1" class="confluenceTd"><span>Users</span>
      </td>
      <td colspan="1" class="confluenceTd">
        <p>As is (For older X-Cart 4 versions, user passwords are migrated; not so for newer versions).&nbsp;</p>
      </td>
    </tr>
    <tr>   
      <td colspan="1" class="confluenceTd"><span>Memberships</span>
      </td>
      <td colspan="1" class="confluenceTd">
        <p>As is (Including multilingual data).&nbsp;</p>
      </td>
    </tr>
    <tr>   
      <td colspan="1" class="confluenceTd"><span>Zones</span>
      </td>
      <td colspan="1" class="confluenceTd">
        <p>As is.&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td colspan="1" class="confluenceTd"><span>Payment settings</span>
      </td>
      <td colspan="1" class="confluenceTd">
        <p>Only for the following payment methods:
          <br><span>&nbsp;</span>
          <br>*   AuthorizeNet;
          <br><span>&nbsp;</span>
          <br>*   EWay;
          <br><span>&nbsp;</span>
          <br>*   Moneybookers;
          <br><span>&nbsp;</span>
          <br>*   PayPal (Standard, ExpressCheckout, PayflowLink, PayflowTransparentRedirect, PaypalAdvanced, PaypalWPS);
          <br><span>&nbsp;</span>
          <br>*   2Checkout.&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td colspan="1" class="confluenceTd"><span>Shipping settings</span>
      </td>
      <td colspan="1" class="confluenceTd">
        <p>*   User defined methods and rates
          <br><span>&nbsp;</span>
          <br>Real-time:
          <br><span>&nbsp;</span>
          <br>*   Australia Post;
          <br><span>&nbsp;</span>
          <br>*   Canada Post;
          <br><span>&nbsp;</span>
          <br>*   DHL;
          <br><span>&nbsp;</span>
          <br>*   FedEx;
          <br><span>&nbsp;</span>
          <br>*   USPS;
          <br><span>&nbsp;</span>
          <br>*   UPS (If the method is used in X-Cart 4, the Migration wizard requires that the module "UPS" should be enabled in X-Cart 5; your X-Cart 4 store's UPS settings are not checked and not migrated to X-Cart 5)&nbsp;</p>
      </td>
    </tr>
  </tbody>
</table>

## Functionality matching
The module performs a basic check of whether your X-Cart 5 installation has all the necessary modules installed and activated to cover the functionality that was available to you in your X-Cart 4 store. If it determines that a certain module needs to be installed/activated, an additional wizard step will be added to allow for this operation.

For instance, потребуются модули eWay, Variants, Market price

Полное соответствие условий необходимости установки модулей следующее

