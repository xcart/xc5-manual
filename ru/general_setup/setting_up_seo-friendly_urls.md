---
lang: ru
layout: article_with_sidebar
updated_at: '2017-10-13 14:10 +0400'
identifier: ref_7IDJJdrM
title: ''
order: 100
published: false
---
## Введение

Данная статья описывает процесс создания оптимизированных для поисковых систем ссылок на продукты и категории взамен стандартных ссылок с параметром GET (например, `cart.php?target=category&category_id=2`)

## Содержание

*   [Общие настройки](#general-setup)
*   [Настройка Apache](#setting-up-apache)
*   [Настройка IIS](#setting-up-iis)
*   [Настройка nginx](#setting-up-nginx)
*   [Изменение семантических ссылок](#tweaking-cleanurls)
*   [Алиас семантической ссылки](#clean-url-aliases)
*   [Решение проблем](#troubleshooting)


## Общие настройки

Войдите в зону администратора X-Cart, откройте раздел **"Настройки магазина** / **SEO настройки"** и активируйте опцию **"Включение ЧПУ"**.

![1.jpg]({{site.baseurl}}/attachments/ref_7IDJJdrM/1.jpg)

Появится подтверждение, что опция включена, и с этого момента ваш магазин готов к использованию семантических ссылок. 

![2.jpg]({{site.baseurl}}/attachments/ref_7IDJJdrM/2.jpg)

Если ваш сервер не поддерживает переадресацию и, следовательно, семантические ссылки, вы увидите такое предупреждение:

![3.jpg]({{site.baseurl}}/attachments/ref_7IDJJdrM/3.jpg)

Это значит, что для работы семантических ссылок необходимо настроить сервер. Данные настройки могут варьироваться в зависимости от серверного програмного обеспечения. Данная статья рассказывает, как настроить  [Apache](#setting-up-apache), [IIS](#setting-up-iis) и [nginx](#setting-up-nginx).

## Настройка Apache

Прежде всего, включите Apache модуль [mod_rewrite](http://httpd.apache.org/docs/current/mod/mod_rewrite.html), чтобы появилась кнопка **"Включение ЧПУ"**. Для этого в Apache файле **httpd.conf** замените следующую строку:

```php
#LoadModule rewrite_module modules/mod_rewrite.so
```

на такую:

```php
LoadModule rewrite_module modules/mod_rewrite.so
```

Теперь перезапустите Apache сервер и проверьте результат. 

## Настройка IIS

Для настройки IIS потребуется [импорт правил Apache](http://www.iis.net/learn/extensions/url-rewrite-module/importing-apache-modrewrite-rules). Следуйте инструкциям в [статье](http://www.iis.net/learn/extensions/url-rewrite-module/importing-apache-modrewrite-rules) для импортирования правил из файла `<X-Cart>/.htaccess`.












