---
identifier: ref_BvyxeQSQ
updated_at: 2016-01-08 00:00
layout: article_with_sidebar
lang: en
title: 'Setting up seo-friendly URLs'
categories:
  - User manual

---


# Introduction

This article aims to help merchants set up X-Cart to use SEO-friendly URLs for product and categories, instead of default ones with GET parameters (e.g. `cart.php?target=category&category_id=2`)

# Table of Contents

*   [Introduction](#introduction)
*   [Table of Contents](#table-of-contents)
*   [General set up](#general-set-up)
*   [Setting up Apache](#setting-up-apache)
*   [Setting up IIS](#setting-up-iis)
*   [Setting up nginx](#setting-up-nginx)
*   [Disabling SEO-friendly URLs](#disabling-seo-friendly-urls)
*   [Troubleshooting](#troubleshooting)

# General set up

Log in to your store's Admin area and go to the **System Settings** > **Environment** section there.

![]({{site.baseurl}}/attachments/7505785/8716521.png?effects=drop-shadow)

Click the **Enable clean URL** button on the half-way through to the bottom. 

![]({{site.baseurl}}/attachments/7505785/9437498.png?effects=drop-shadow)

Generally, from now on your store will start using seo-friendly URLs, and after a couple of seconds you will see the **Clean URLs are enabled** message:

![]({{site.baseurl}}/attachments/7505785/9437499.png?effects=drop-shadow)

If your server environment is not compatible with handling redirects properly and thus not be able to work with SEO-friendly URLs right now, you will see the following message: 

![]({{site.baseurl}}/attachments/7505785/9437500.png?effects=drop-shadow)

It means, you need to set up your server before you can use SEO-friendly URLs. This setting up may differ depending on your server software. This article describes how you can set up {% link "Apache" ref_BvyxeQSQ %}, {% link "IIS" Setting-up-seo-friendly-URLs_7505785.html %} or {% link "nginx" Setting-up-seo-friendly-URLs_7505785.html %}.

# Setting up Apache

You need to enable Apache's module [mod_rewrite](http://httpd.apache.org/docs/current/mod/mod_rewrite.html) and it will enable the **Enable clean URLs** button in the **Environment** section described above. Typically, you should edit the **httpd.conf** file of your Apache and replace there the following line:

{% highlight php %}{% raw %}
#LoadModule rewrite_module modules/mod_rewrite.so
{% endraw %}{% endhighlight %}

with the next one:

{% highlight php %}{% raw %}
LoadModule rewrite_module modules/mod_rewrite.so
{% endraw %}{% endhighlight %}

After that, restart your Apache server and check the results.

# Setting up IIS

Use the [Import of Apache rules](http://www.iis.net/learn/extensions/url-rewrite-module/importing-apache-modrewrite-rules) feature in order to set up your IIS. Follow the process described in the [http://www.iis.net/learn/extensions/url-rewrite-module/importing-apache-modrewrite-rules](http://www.iis.net/learn/extensions/url-rewrite-module/importing-apache-modrewrite-rules) article and import rules from your `<X-Cart>/.htaccess` file.

# Setting up nginx

You should put the following lines into the [server {} section](http://nginx.org/en/docs/http/ngx_http_core_module.html#server) into your nginx configuration file (nginx.conf):

{% highlight php %}{% raw %}
# Example nginx configuration
location / {
  index cart.php;

  if (!-e $request_filename){
     rewrite ^/sitemap.xml(\?.+)?$ /cart.php?target=sitemap;
     rewrite ^/((([/_A-Za-z0-9-]+)/)?([_A-Za-z0-9-]+)/)?([_A-Za-z0-9-]+)(/?)(\.([_A-Za-z0-9-]+))?$ /cart.php?url=$5&last=$4&rest=$3&ext=$7 last;
  }
}
{% endraw %}{% endhighlight %}

You should obviously set location to corresponding directory in case your X-Cart installation is placed in subdirectory of your web-root.

# Disabling SEO-friendly URLs

If you need to disable SEO-friendly URLs for some reason, you can simply switch Clean URL selector off:

![]({{site.baseurl}}/attachments/7505785/9437502.png?effects=drop-shadow)

# Troubleshooting

Steps listed below usually fix the problem that SEO-friendly URLs cannot be enabled or are not working:

1.  Make sure that the following line in your `.htaccess` file reflects an actual path to your store: 

    {% highlight php %}{% raw %}
    RewriteBase /
    {% endraw %}{% endhighlight %}

    It must be the same as the value specified in the `web_dir` variable in the `<X-Cart>/etc/config.php` file.

2.  Make sure that the `AllowOverride` directive is set to `All` in the `conf.httpd` file on your server: 

    {% highlight php %}{% raw %}
     AllowOverride All
    {% endraw %}{% endhighlight %}

## Attachments:

![](images/icons/bullet_blue.gif) [system-settings-enviroment.png]({{site.baseurl}}/attachments/7505785/7995393.png) (image/png)  
![](images/icons/bullet_blue.gif) [enable-clean-urls-button.png]({{site.baseurl}}/attachments/7505785/7995394.png) (image/png)  
![](images/icons/bullet_blue.gif) [clean-urls-enabled-message.png]({{site.baseurl}}/attachments/7505785/7995395.png) (image/png)  
![](images/icons/bullet_blue.gif) [clean-urls-disbaled-message.png]({{site.baseurl}}/attachments/7505785/7995396.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_environment.png]({{site.baseurl}}/attachments/7505785/8716521.png) (image/png)  
![](images/icons/bullet_blue.gif) [X Cart online store builder Environment.png]({{site.baseurl}}/attachments/7505785/9437501.png) (image/png)  
![](images/icons/bullet_blue.gif) [X Cart online store builder Environment2.png]({{site.baseurl}}/attachments/7505785/9437499.png) (image/png)  
![](images/icons/bullet_blue.gif) [X Cart online store builder Environment3.png]({{site.baseurl}}/attachments/7505785/9437500.png) (image/png)  
![](images/icons/bullet_blue.gif) [X Cart online store builder Environment.png]({{site.baseurl}}/attachments/7505785/9437498.png) (image/png)  
![](images/icons/bullet_blue.gif) [X Cart online store builder Environment4.png]({{site.baseurl}}/attachments/7505785/9437502.png) (image/png)