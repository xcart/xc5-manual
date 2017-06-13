---
lang: en
layout: article_with_sidebar
updated_at: '2017-06-13 13:51 +0400'
identifier: ref_OBh3V1k1
title: Optimizing your catalog pages for SEO
categories:
  - User manual
published: false
order: 110
---
When working on the SEO optimization of your X-Cart store, the following things may require your attention:

   *   [Clean URLs](#clean-urls)
   *   [Title and Meta elements](#title-end-meta-elements)
   *   [robots.txt](#robotstxt)

## Clean URLs

The pages of your X-Cart based store are generated dynamically, and the URL of each page is also formed dynamically based on a query to the store's database. For example, a typical product page URL looks like the following: ``http://www.example.com/xcart/cart.php?target=product&product_id=31``.

Dynamic URLs containing query strings pose a problem for SEO, because they stop many search engines from indexing the pages in which they are used. They are also difficult to read and remember for your store's human visitors.

To solve the problems posed by dynamic URLs, we recommend using the so-called "clean" URLs feature. Clean URLs are SEO-friendly and human-readable URLs that are used instead of the original dynamic ones. With clean URLs enabled, the above cited page URL could look like ``http://www.example.com/xcart/cup-of-mojo-bluetooth-speaker.html`` or  ``http://www.example.com/xcart/cup-of-mojo-speaker.html`` (You have full control of what the URL says to your customers.)

Information on setting up the clean URLs feature in X-Cart 5 is available in the section {% link "Setting up seo-friendly URLs" ref_nJxrzFEZ %} of this manual.

In your store, clean URLs can be defined for products (see the Marketing section of the product information page when adding a new product or editing an existing one):
   ![xc5_seo_product_clean_url.png]({{site.baseurl}}/attachments/ref_OBh3V1k1/xc5_seo_product_clean_url.png)

categories:
   ![xc5_seo_category_clean_url.png]({{site.baseurl}}/attachments/ref_OBh3V1k1/xc5_seo_category_clean_url.png)

and pages in the Pages section (**Content** > **Pages**):
   ![xc5_seo_page_clean_url.png]({{site.baseurl}}/attachments/ref_OBh3V1k1/xc5_seo_page_clean_url.png)

Note that by default X-Cart generates clean URLs for pages automatically, and you can have X-Cart create a clean URL for a page at any time simply by saving/updating the page with the **Autogenerate Clean URL** checkbox option enabled. 
If, however, you would like to add or edit a previously added clean URL manually, you can do so by unchecking the **Autogenerate Clean URL** option and editing the contents of the Clean URL field directly.

## Title and Meta elements
define meta elements of your product and category pages - such as the page title, meta description and meta keywords.

## robots.txt

_See also:_

*   [SEO for beginners. Part 1: First Steps in Making Your Store Visible to Search Engines](http://blog.x-cart.com/seo-for-beginners-first-steps-in-making-your-store-visible-to-search-engines.html)
