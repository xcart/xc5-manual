---
lang: en
layout: article_with_sidebar
updated_at: '2016-09-28 18:18 +0400'
identifier: ref_nJxrzFEZ
title: Setting up seo-friendly URLs
categories:
  - User manual
published: true
order: 280
---


## Introduction

This article aims to help merchants set up X-Cart to use SEO-friendly URLs for product and categories, instead of default ones with GET parameters (e.g. `cart.php?target=category&category_id=2`)

## Table of Contents

*   [Introduction](#introduction)
*   [Table of Contents](#table-of-contents)
*   [General set up](#general-set-up)
*   [Setting up Apache](#setting-up-apache)
*   [Setting up IIS](#setting-up-iis)
*   [Setting up nginx](#setting-up-nginx)
*   [Disabling SEO-friendly URLs](#disabling-seo-friendly-urls)
*   [Troubleshooting](#troubleshooting)

## General set up

Log in to your store's Admin area and go to the **System Settings** > **Environment** section there.

![]({{site.baseurl}}/attachments/7505785/8716521.png?effects=drop-shadow)

Click the **Enable clean URL** button on the half-way through to the bottom. 

![]({{site.baseurl}}/attachments/7505785/9437498.png?effects=drop-shadow)

Generally, from now on your store will start using seo-friendly URLs, and after a couple of seconds you will see the **Clean URLs are enabled** message:

![]({{site.baseurl}}/attachments/7505785/9437499.png?effects=drop-shadow)

If your server environment is not compatible with handling redirects properly and thus not be able to work with SEO-friendly URLs right now, you will see the following message: 

![]({{site.baseurl}}/attachments/7505785/9437500.png?effects=drop-shadow)

It means, you need to set up your server before you can use SEO-friendly URLs. This setting up may differ depending on your server software. This article describes how you can set up [Apache](#setting-up-apache), [IIS](#setting-up-iis) or [nginx](#setting-up-nginx).

## Setting up Apache

You need to enable Apache's module [mod_rewrite](http://httpd.apache.org/docs/current/mod/mod_rewrite.html) and it will enable the **Enable clean URLs** button in the **Environment** section described above. Typically, you should edit the **httpd.conf** file of your Apache and replace there the following line:

```php
#LoadModule rewrite_module modules/mod_rewrite.so
```

with the next one:

```php
LoadModule rewrite_module modules/mod_rewrite.so
```

After that, restart your Apache server and check the results.

## Setting up IIS

Use the [Import of Apache rules](http://www.iis.net/learn/extensions/url-rewrite-module/importing-apache-modrewrite-rules) feature in order to set up your IIS. Follow the process described in the [http://www.iis.net/learn/extensions/url-rewrite-module/importing-apache-modrewrite-rules](http://www.iis.net/learn/extensions/url-rewrite-module/importing-apache-modrewrite-rules) article and import rules from your `<X-Cart>/.htaccess` file.

## Setting up nginx

You should put the following lines into the [server {} section](http://nginx.org/en/docs/http/ngx_http_core_module.html#server) into your nginx configuration file (nginx.conf):

## Configuration for X-Cart 5.3.1 and earlier

```php
## Example nginx configuration
location / {
  index cart.php;

  if (!-e $request_filename){
     rewrite ^/sitemap.xml(\?.+)?$ /cart.php?target=sitemap;
     rewrite ^/((([/_A-Za-z0-9-]+)/)?([_A-Za-z0-9-]+)/)?([_A-Za-z0-9-]+)(/?)(\.([_A-Za-z0-9-]+))?$ /cart.php?url=$5&last=$4&rest=$3&ext=$7 last;
  }
}
```

## Configuration for X-Cart 5.3.2 and later

Starting from X-Cart 5.3.2, configuration has to be changed to accept dots(.) in url path.

```php
## Example nginx configuration (X-Cart 5.3.2+)
location / {
  index cart.php;

  if (!-e $request_filename){
     rewrite ^/sitemap.xml(\?.+)?$ /cart.php?target=sitemap;
     rewrite ^(.*)$ /cart.php?url=$1 last;
  }
}
```

You should obviously set location to corresponding directory in case your X-Cart installation is placed in subdirectory of your web-root.

## Disabling SEO-friendly URLs

If you need to disable SEO-friendly URLs for some reason, you can simply switch Clean URL selector off:

![]({{site.baseurl}}/attachments/7505785/9437502.png?effects=drop-shadow)

## Troubleshooting

Steps listed below usually fix the problem that SEO-friendly URLs cannot be enabled or are not working:

1.  Make sure that the following line in your `.htaccess` file reflects an actual path to your store: 

    ```php
    RewriteBase /
    ```

    It must be the same as the value specified in the `web_dir` variable in the `<X-Cart>/etc/config.php` file.

2.  Make sure that the `AllowOverride` directive is set to `All` in the `conf.httpd` file on your server: 

    ```php
     AllowOverride All
    ```


