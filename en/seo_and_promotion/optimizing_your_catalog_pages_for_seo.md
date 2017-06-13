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

Information on setting up the clean URLs feature in X-Cart 5 is available in the section {% link %} of this manual.

In your store, clean URLs can be defined for the pages of such objects as products, categories, manufacturers and embedded static pages.

*   configure custom SEO-friendly "Clean URLs"  for your product and category pages.

For a product, SEO optimization related settings can be found on the **Info** tab of the product's details page:

![]({{site.baseurl}}/attachments/6389820/8719379.png)

For a category, these settings can be found on the **Category info** tab of the category's details page:

![]({{site.baseurl}}/attachments/6389820/8719380.png)

Note that by default X-Cart generates Clean URLs for product and category pages automatically: you simply need to make sure the **Autogenerate Clean URL** checkbox option is enabled before you click the button to save the details of the product or category you've been editing.

If necessary, you can manually edit the automatically generated Clean URLs; for that you would need to uncheck the **Autogenerate Clean URL **option and edit the **Clean URL** field directly.

## Title and Meta elements
define meta elements of your product and category pages - such as the page title, meta description and meta keywords.

## robots.txt

_See also:_

*   [SEO for beginners. Part 1: First Steps in Making Your Store Visible to Search Engines](http://blog.x-cart.com/seo-for-beginners-first-steps-in-making-your-store-visible-to-search-engines.html)
