---
lang: en
layout: article_with_sidebar
updated_at: '2017-06-27 14:51 +0400'
identifier: ref_J70IfNxL
title: Choosing the data cache driver
order: 100
published: true
categories:
  - Environment configuration
---
Caching one of the most effective way of improving performance of web applications of all kinds. X-Cart 5 employs various types of caching the data at many levels within the system. However, you have to choose the most appropriate cache driver to get the maximum performance gain. 

X-Cart application gives you the following options of the caching mechanism:

-	[APC](http://php.net/manual/en/book.apc.php) cache
-	[Memcached \ Memcache](http://php.net/manual/en/book.memcached.php) driver
-	[XCache](https://xcache.lighttpd.net/) driver
-	File system caching

By default, X-Cart tries to detect and automatically select the caching driver for you in the aforemented order, eventually falling back to the file system caching (using it doesn't require any configuration).

{% note warning %}
File system caching stores the serialized, cached objects in the filesystem inside X-Cart application directory (`<X-Cart>/var/datacache` to be particular). You'll have to configure the periodic cleaning of the datacache directory, otherwise your storage space will be eventually full and the server will fail.

We suggest adding a task via the `crontab` shell program (on UNIX-based systems), e.g.:

```
0 0 * * * rm -rf <X-Cart dir>/var/datacache/
```

This example task will purge the datacache folder at midnight of the each day.

More info about setting up the cron tasks can be found [here](https://www.cyberciti.biz/faq/how-do-i-add-jobs-to-cron-under-linux-or-unix-oses/).
{% endif %}

## Configuring the X-Cart cache driver

You can select the cache driver manually by setting the `type` option in `[cache]` section inside `<X-Cart dir>/etc/config.php`

```
; ----------------------
;  Cache settings
; ----------------------
;
[cache]
; Type of cache used. Can take auto, memcache, memcached, apc, xcache, file values.
type=file
```

## Overview of the cache driver options

