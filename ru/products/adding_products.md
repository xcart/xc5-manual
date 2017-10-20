---
lang: ru
layout: article_with_sidebar
updated_at: '2017-10-20 11:52 +0400'
identifier: ref_REno3u9g
title: ''
order: 100
published: false
---
Данная статья рассказывает, как создать продукты в магазине вручную. Кроме того, продукты можно внести в магазин путем {% link "импорта" ref_TANvG2De %}. 

## Создание нового продукта

1.  В панели управления магазина откройте страницу **"Каталог / Товары"** 
    ![]({{site.baseurl}}/attachments/6389859/8716836.png)
2.  Нажмите кнопку **"Добавить товар"**
    ![]({{site.baseurl}}/attachments/6389859/8716837.png)
    Откроется страница создания товара 
    ![]({{site.baseurl}}/attachments/6389859/8716838.png)
3.  Заполните поля информацией о новом товаре. **Название**  - единственное обязательное поле.  
4.  Нажмите кнопку **"Добавить товар"** 
    ![]({{site.baseurl}}/attachments/6389859/8716867.png)
    Продукт готов.

## Информация о товаре

Создавая новый продукт, вы можете указать следующие данные:

*   **SKU**: A unique SKU for this product.
*   **Product name**: The name by which you and your customers will identify this product.
*   **Category**: The category (or categories) to which this product belongs. 
*   **Images**: Use this section to add images of the product.
*   **Memberships**: Membership levels to which this product should be available. Non-members and users belonging to other membership levels will not be able to see the product on the storefront.
*   **Tax class**: The tax class to which the product belongs (Defines what taxes should be applied to the product). For more info on tax classes, see: {% link "Setting up tax classes" ref_pAWOdG8N %}.
*   **Price**: The product price.
*   **Product on sale**: Use this to put the product on sale.
*   **Quantity in stock**: The exact current quantity in stock, or any value if you do not intend to track the inventory of this product. (In the latter case you will need to disable inventory tracking after the product has been created.) 
*   **Weight**: Product weight.
*   **Shippable**: Whether the product is shippable.
*   **Free shipping**: Whether the product should be shipped free of charge.
*   **Ship in a separate box**: Whether the product needs to be shipped separately from other products. If it is shippable in a separate box, you can define the box dimensions and how many products can be put in this box;
*   **Available for sale**: Whether the product should be displayed on the storefront. Uncheck this option to temporarily remove the product from the storefront (Store visitors will not be able to see it).
*   **Arrival date**: This field allows you to record the date since when the product is available in your store. On its own, the information entered in this field serves purely informational purposes, but may be employed by X-Cart modules (For example, a module that allows you to add a new product to your catalog in advance and let it be published on the storefront automatically when its arrival date is reached).
*   **Product page title**: The title to be used in the title bar of this product details page (for SEO purposes). 
*   **Brief** **description**: A short product description that will be displayed on product list pages.
*   **Full description**: A longer product description that will be displayed on the product details page.
*   **Open Graph meta tags**: The custom META tags for sharing the product page on Facebook.
*   **Meta keywords**: The keywords to be used in the keywords META tag on the product page (for SEO purposes).
*   **Meta description**: The description to be used in the description META tag on the product page (for SEO purposes).
*   **Clean URL**: The product page Clean URL (for SEO purposes).

## Отслеживание изменения количества товара

1.  Откройте страницу товара, для которого нужно настроить отслеживание количества. 
2.  Перейдите на вкладку **"Контроль остатков"**:
    ![]({{site.baseurl}}/attachments/6389859/8716870.png)
    На страницу управления количеством товара можно, также, перейти по ссылке **"Контроль остатков"** в разделе **"Цены и наличие на складе"** в информации о товаре:
    ![]({{site.baseurl}}/attachments/6389859/8716871.png)
    Открывается страница настроек:
    ![]({{site.baseurl}}/attachments/6389859/8716869.png)
3.  Настройка отслеживание количества товара:
    *   **Контроль остатков (включен / отключен)** - с помощью этого переключателя можно _включить_ или _отключить_ отслеживание количества товара в наличии. Если запас товара не ограничен, эту опцию можно _отключить_.
    *   **Остаток** - точное текущее количество штук данного товара в наличии.
    *   **Уведомлять администратора при уменьшении остатка данного товара на складе до определенного предела** (включено / отключено) - если опция _включена_, администратор магазина получает уведомление о снижении количества товара. Данная опция требует заполнения следующего поля ("Минимальное количество"), в котором устанавливается количество товара, при котором администратор получает предупреждение. Если опция _отключена_, администратор не получает сообщений о том, что продукт заканчивается.  
    *   **Минимально количество** - в этом поле указывается количество товара, которое считается низким. При включенной опции выше, администратор получает предупреждение, когда количество товара достигает этого значения. 
4.  Нажмите **"Сохранить"**.

## Дополнительные параметры товара (цвет, материал, страна-производитель и т.д.)

Такую информацию можно добавить как свойства товара на вкладке **"Атрибуты"**.

![]({{site.baseurl}}/attachments/6389859/8716868.png)

Покупатели увидят эти атрибуты в разделе **"Характеристики"** на странице товара.

Атрибуты товаров подробно описаны в статье {% link "Product classes and attributes" ref_T90ZcEpP %}.

## Варианты товаров (цвет, размер и т.д.)

В X-Cart 5 варианты товаров настраиваются на основе атрибутов. Задайте атрибут "Размер" и несколько значений для него - "XS", "S", "M". так, покупатель сможет выбрать один из вариантов размера. Примеры создания вариантов на основе атрибутов описаны в статье {% link "Managing attribute values" ref_bTfJ9bTS %}. Более подробная информация об атрибутах товаров - {% link "Product classes and attributes" ref_T90ZcEpP %}.

