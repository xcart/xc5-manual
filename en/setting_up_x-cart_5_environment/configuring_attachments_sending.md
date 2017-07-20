---
lang: en
layout: article_with_sidebar
updated_at: '2017-07-20 17:31 +0400'
identifier: ref_yCxquUhl
title: Configuring the huge attachments sending
order: 100
published: true
version: X-Cart 5.3.3.2
---
This guide offers some tips on how to configure your X-Cart server to allow huge file attachments (100 Mb and more) to be downloaded by the customers. Without configuring the following settings any large download will hang up. 

First of all, you have to update your `etc/config.php` configuration file and add the following setting to the `[other]` section:

```
; Use X-Sendfile and X-Accel-Redirect to download files
; Note that server should be properly configured
use_sendfile = On
```

Later on, you'll have to perform some server-specific configuration.

## Apache-specific configuration

You'll need to edit the main `.htaccess` file in the root of the X-Cart folder and add the following settings:

```
XSendFile On
```

On X-Cart 5.3.3.2 or later installations this option is included by default.

## nginx-specific configuration

You'll need to add the following `location` directive to the server configuration file into the `server` section and replace the `<STORE ROOT>` part with the path to the X-Cart folder:

```
    location /storage_download/ {
        internal;
        alias <STORE ROOT>/files/;
    }
```

{% note warning %}
If your site is placed in subdirectory of your web-root, you should provide path to this subdirectory in the `<STORE ROOT>` part.
{% endnote %}
