---
lang: ru
layout: article_with_sidebar
updated_at: '2017-10-31 16:46 +0400'
identifier: ref_SuWz9rmN
title: Работа со значениями атрибутов
order: 30
published: false
---
Данная статья рассматривает следующие вопросы::

*   [Типы полей значений атрибутов](#attribute-value-field-types)  в X-Cart 5;
*   Как задать опции продукта посредством [многозначных атрибутов](#multi-value-attributes-product-options);
*   Как [персонализировать](#personilization-options-editable-textarea) продукт (сделать на странице продукта редактируемое поле, в котором покупатели смогут писать тексты);
*   Как настроить продукт, чтобы [цена и/или вес изменялись](#price-and-weight-modifiers) в зависимости от выбранных покупателем опций продукта;
*   Как сделать [одно из значений атрибута значением по умолчанию](#setting-the-default-attribute-value).

## Типы полей значений атрибутов в X-Cart 5

X-Cart 5 поддерживает три типа полей значений атрибутов:

*   [Предзаполненное поле](#plain-field)
*   [Текстовое поле](#textarea)
*   [Да/Нет](#yesno)

Выберите наиболее подходящий тип значений при настройке атрибута. Ниже каждый тип описан подробно.

### Предзаполненное поле

Этот тип представляет значения атрибута в виде фразы или слова и подходит для настройки вариантов цвета, размера продукта и т.п., т.е. для любых свойств продукта, которые можно описать парой слов. Например, размеры сумок:

![1.jpg]({{site.baseurl}}/attachments/ref_SuWz9rmN/1.jpg)

Покупатели в магазине видят эту информацию так:

![2.jpg]({{site.baseurl}}/attachments/ref_SuWz9rmN/2.jpg)

Обратите внимание, что такой тип поля позволяет задать несколько значений одного атрибута. Дополнительная информация: [Многозначные атрибуты (опции продукта)](#multi-value-attributes-product-options).

### Текстовое поле

С помощью поля такого типа можно сделать подробное описание атрибута. Например, описание материала:

![3.jpg]({{site.baseurl}}/attachments/ref_SuWz9rmN/3.jpg)

Покупатели в магазине видят эту информацию так:

![5.jpg]({{site.baseurl}}/attachments/ref_SuWz9rmN/5.jpg)

Текстовое поле позволяет персонализировать продукт, т.е. добавить текстовое поле на странице продукта, в котором покупатели могут писать свои тексты. Дополнительная информация: [Персонализация продукта](#personilization-options-editable-textarea).

### Да/Нет

Такой тип поля предназначен для значений атрибута, которые подразумевают наличие или отсутствие какого-то свойства. Например, наушники могут быть с проводом и без провода:

![6.jpg]({{site.baseurl}}/attachments/ref_SuWz9rmN/6.jpg)

Покупатели в магазине видят эту информацию так:

![7.jpg]({{site.baseurl}}/attachments/ref_SuWz9rmN/7.jpg)

Обратите внимание, что поле _Да/Нет_ может, также, применяться для опций продуктов. Дополнительная информация: [Многозначные атрибуты (опции продукта)](#multi-value-attributes-product-options).

## Многозначные атрибуты (опции продукта)

_Предзаполненное поле_ и поле _Да/Нет_ позволяют задать несколько значений для одного атрибута. Таким образом в  X-Cart 5 создаются опции продуктов, из которых покупатель может выбирать. Например, с помощью _предзаполненного поля_ можно задать разные размеры предмета одежды. Отдельные размеры XS, S, M и L можно сделать опциями продукта, если сделать их значениями атрибута _Размер_:

![8.jpg]({{site.baseurl}}/attachments/ref_SuWz9rmN/8.jpg)

Как это видят покупатели:

![9.jpg]({{site.baseurl}}/attachments/ref_SuWz9rmN/9.jpg)

Таким образом, размеры  XS, S, M и L стали опциями продукта, которые можно выбрать из выпадающего меню.

Как это настроить:

1.  В поле **Значение атрибута** впишите значение атрибута, оно будет первым в списке значений. Например,  XS.
2.  Наведите курсор на поле **Значение атрибута**, справа появится флажок **Несколько значений**:
    ![10.jpg]({{site.baseurl}}/attachments/ref_SuWz9rmN/10.jpg)
3.  Поставьте галочку, чтобы задать несколько значений для атрибута. Ниже появится новое пустое поле **Значение атрибута**:
    ![11.jpg]({{site.baseurl}}/attachments/ref_SuWz9rmN/11.jpg)
4.  Use the **Attribute option** field on the new line to type in the next attribute value name. As soon as you start typing, another empty line will be added to the list:
    ![]({{site.baseurl}}/attachments/7504859/8719333.png)
5.  Continue until you have added all the attribute values you require.
6.  Choose whether you want to apply the changes locally or globally.
7.  Click **Save changes**.

With the _Yes/No_ field type, it is quite similar; the only difference is that there are just two options, _Yes_ and _No_, and you do not have to type them manually, but can select them from a list.

![]({{site.baseurl}}/attachments/7504859/8719334.png)

On the storefront, customers can choose the option they require by adjusting the respective check box:

![]({{site.baseurl}}/attachments/7504859/7602537.png)

It should be noted that the method for specifying product options described above does not provide a way to track how many product units with a specific option you have sold and how many you still have on hand. Also, if the product has more than one multi-valued attribute, there is no way to specify, which option combinations (product variants) are actually available. If you need these features, consider installing X-Cart's [Product Variants](http://www.x-cart.com/extensions/addons/product-variants.html) module. This module allows you to create product variants from options and make them have their own prices, SKUs and stock levels.

## Personilization options (editable Textarea)
