---
lang: en
layout: article_with_sidebar
updated_at: '2017-06-13 13:51 +0400'
identifier: ref_OBh3V1k1
title: Optimizing your catalog pages for SEO
categories:
  - User manual
published: true
order: 110
---
When working on the SEO optimization of your X-Cart store, the following things may require your attention:

   *   [Clean URLs](#clean-urls)
   *   [Title and Meta elements](#title-end-meta-elements)
   *   [robots.txt](#robotstxt)
   *   [XML sitemap](#xml-sitemap)

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
The HEAD section of every page in your store contains elements providing metadata about the page. Some of these elements (page title, meta description and meta keywords) may have a significant impact on how the page is ranked by search engines and how it is described in search engine results pages. In X-Cart, you have substantial control over the meta elements and can use them for SEO optimization.

## robots.txt 
Another thing to consider when dealing with the SEO optimization of your X-Cart store is the file robots.txt.

The file robots.txt is used to give instructions about the site to web robots, and its primary function is to block web robots from accessing the pages of your site that do not need to be indexed by search engines. Your X-Cart store comes bundled with a robots.txt file that should be good for any store installed in the root (top-level directory) of your domain. If, however, your X-Cart store is installed in a subdirectory off the domain root, you will need to take a few additional steps to ensure that the robots.txt file for your store actually works (see further below for instructions). 

Simply put, when a robot looks for the file robots.txt, it strips the path component from the URL (everything from the first single slash), and puts "robots.txt" in its place. For example, on ``www.example.com``, the robots will expect to find the robots.txt file at ``www.example.com/robots.txt``. If your store's address is ``www.example.com``, your store's robots.txt file can be found exactly at that location, which means it can be accessed by web robots ok, and nothing needs to be done. However, if your X-Cart store is installed, for example, at ``www.example.com/shop``, the location of the file robots.txt is ``www.example.com/shop/robots.txt``. That is not ok and needs to be fixed. 

So, if your store is installed in a subdirectory, you will need to move the file robots.txt to the level of your domain root, or - if there is already another robots.txt file at that level - to copy the instructions from the robots.txt file in your X-Cart store directory to the robots.txt at the domain root. In both the cases, you will also need to adjust the paths in the robots.txt file at the domain root level. For example, after moving from ``www.example.com/shop/robots.txt`` to ``www.example.com/robots.txt``, the directive ``Disallow: /Includes/`` should be replaced by ``Disallow: /shop/Includes/``. The same should be done for any of the paths mentioned in robots.txt.

## XML sitemap
Another thing that should be checked upon when SEO-optimizing your X-Cart store is XML sitemap. XML sitemap is a collection of xml files whose purpose is exactly the opposite of robots.txt: your store's XML sitemap informs search engines about the URLs on your store website that are available for crawling. To enable search engines to crawl your website better, we strongly recommend submitting your store's XML sitemap to search engines via the inclusion of the XML sitemap URL into robots.txt or manual submission of the URL directly to your chosen search engine. For more info on the use of XML sitemap, see the section {% link "Submitting your shop to search engines" ref_OqJ2oZTE %} of this manual.

_See also:_

*   [SEO for beginners. Part 1: First Steps in Making Your Store Visible to Search Engines](http://blog.x-cart.com/seo-for-beginners-first-steps-in-making-your-store-visible-to-search-engines.html)
