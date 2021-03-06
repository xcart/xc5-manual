---
lang: ru
layout: article_with_sidebar
updated_at: '2017-10-23 11:03 +0400'
identifier: ref_yVLJrToe
title: Перенос X-Cart на другое местоположение
order: 70
published: true
---
## Введение

Допустим, вы установили X-Cart здесь `http://<HOST>/xcart/`, но хотели бы перенести его на новый адрес `http://<HOST>/xcart5/`.  

Данная статья расскажет, как это сделать.

## Содержание

*   [Перенос файлов и конфигурация](#section-2)
*   [Перенос базы данных](#section-3)

## Перенос файлов и конфигурация

  1. Сделайте бэкап файлов и базы магазина. Резервная копия необходима на случай, если что-то пойдет не так. 

  2. Перенесите файлы из первоначальной директории установки в новую.

    Для переноса X-Cart из одной директории  в другую (из `http://<HOST>/xcart/` в `http://<HOST>/xcart5/`), на Mac/Linux можно воспользоваться командой:

  ```
  cd ~/www/;
  mv xcart xcart5;
  ```

  {% note warning %}
  Помните, что также необходимо перенастроить сервер, чтобы он работал с файлами из оригинальной директории на домене `http://<HOST>/xcart5/`.
  {% endnote %}
   
  3. **[опционально]** чтобы перенести магазин на другой сервер или получить его копию, на новом сервере создайте новую базу данных из бэкапа, созданного на первом шаге. 

  4. **[опционально]** Чтобы создать новую базу данных, заполните параметры `host`, `name`, `user` и `password` в секции `[database_details]` файла `<X-Cart>/etc/config.php` новой установки X-Cart:

  ```
  [database_details]
  hostspec = "localhost"
  socket   = ""
  port     = ""
  database = "database"
  username = "username"
  password = "password"
  table_prefix = "xc_"
  ```
    
  5. В секции `[host_details]` файла `<X-Cart>/etc/config.php` укажите новый путь к установке X-Cart:  
 
  ```
  [host_details]
  http_host = "<HOST>"
  https_host = "<HOST>"
  web_dir = "/xcart"
  ```

  -	Необходимо указать хосты HTTP и HTTPS. Если вы переносите X-Cart в пределах одного сервера, оставьте эти значения без изменений.     

  -	Задайте параметр web_dir. При переносе из `http://<HOST>/xcart/` в `http://<HOST>/xcart5/`, этот параметр нужно поменять с `/xcart` на `/xcart5`.     
  При переносе X-Cart в корневой каталог: `http://<HOST>/`, оставьте это поле пустым.  
  
  
  6. В директиве `RewriteBase` в файле `<X-Cart>/.htaccess` укажите новый путь к установке X-Cart. Пример:
   
  ```
  RewriteBase /xcart5
  ```
  
  7. Удалите папку `<X-Cart>/var/datacache/`. 
 
## Перенос базы данных
 
 Когда файлы магазина уже перенесены, нужно переместить и базу данных. Это можно сделать посредством стандартных средств управления базами данных, например, команды [MySql source](https://dev.mysql.com/doc/mysql-backup-excerpt/5.7/en/reloading-sql-format-dumps.html). 
 
 Также, можно загрузить дамп базы из одной установки X-Cart в другую следующим образом:
 
 1. Прежде всего, удостоверьтесь, что в обоих магазинах установлены и включены одни и те же модули.
 
 2. Если дамп базы более 2MB, загрузите его в файл `<new X-Cart>/var/backup/sqldump.sql.php`. Дамп небольшого размера можно будет загрузить на следующем шаге. 
 
 3. В зоне администратора магазина откройте страницу **Инструменты**/**База данных**/**Восстановить базу** и запустите восстановление. 
 
 4. Загрузите бэкап в новую базу магазина, затем, скопируйте значение `shared_secret_key` из файла оригинальной установки X-Cart и внесите в файл `etc/config.php` новой установки X-Cart. Пример:
 
    ```
    shared_secret_key = "57c81e28ca9e12.95513295"
    ```
