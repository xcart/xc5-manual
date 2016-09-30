---
lang: en
layout: article_with_sidebar
updated_at: '2016-09-30 13:18 +0400'
identifier: ref_OqJ2oZTE
title: Submitting your shop to search engines
categories:
  - User manual
published: true
order: 120
---


The module **XML Sitemap** for X-Cart 5 serves SEO purposes. It generates an XML sitemap that can help popular search engines to crawl your store website better. 

The module can be installed from the X-Cart Marketplace. For general module installation instructions, see {% link "Installing modules from the Marketplace" ref_Vn1mMUw9 %}.![](attachments/6389770/8719381.png?effects=drop-shadow)Once the module XML Sitemap has been installed, you will be able to access the XML sitemap section (**Store setup** > **XML sitemap**) in your store's Admin area.![]({{site.baseurl}}/attachments/6389770/8719453.png?effects=drop-shadow)In the XML sitemap section, you can adjust the settings based on which the XML sitemap for your store will be generated:

*   The subsection titled "**Mark the search engines you want to inform of the structure of your site using the site map**" allows you to specify the search engines to which the information from your site's XML sitemap should be made available.
*   The settings "**Frequency of content renewal for X page**" allow you to specify how frequently specific types of pages on your store site are likely to change. The frequency of content renewal value provides general information to search engines and may not correlate exactly to how often they crawl the page. 
*   The settings "**Priority for X page**" allow you to set the priority for specific types of pages on your store site — relative to other types of pages on your site. Valid values range from 0.0 to 1.0\. The priority value does not affect how your pages are compared to pages on other sites—it only lets the search engines know which pages you deem most important for the crawlers. The default priority value for all page types is 0.5. Search engines may use the priority information when selecting between URLs on the same site, so you can use this setting to increase the likelihood that your most important pages are present in a search index. Note that assigning a high priority to all of the page types on your site is not likely to help you. Since the priority is relative, it is only used to select between URLs on your site.

Once you are done adjusting the XML sitemap settings, be sure to click the **Submit** button to save the changes.

To re-generate your store's XML sitemap after changing the settings, use the **Generate XML-Sitemap** button at the top of the page:

![]({{site.baseurl}}/attachments/6389770/8719785.png?effects=drop-shadow)

At the top of the page, you can find your XML sitemap URL:

![]({{site.baseurl}}/attachments/6389770/8719786.png?effects=drop-shadow)

This URL specifies the location of your store's XML sitemap index. The index lists all the available XML files for your store (There can be more than one XML files due to restrictions on the size of individual XML files and the number of URLs in each XML file). 

The XML sitemap URL can be submitted to search engines directly. We strongly recommend doing so if clean URLs are not configured or not working correctly for your store.

For more info on sitemaps, see [http://www.sitemaps.org](http://www.sitemaps.org).


