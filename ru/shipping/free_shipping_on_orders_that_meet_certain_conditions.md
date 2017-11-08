---
lang: ru
layout: article_with_sidebar
updated_at: '2017-11-08 14:19 +0400'
identifier: ref_XrlVrrcu
title: 'Бесплатная доставка заказов, отвечающих определенным требованиям'
order: 30
published: false
---
X-Cart позволяет настроить бесплатную доставку для заказов, которые отвечают определенным требованиям. Например:

   * для заказов с суммой выше определенного значения (бесплатная доставка для заказов с суммой выше RUB 3000);
   * для заказов, доставляемых в пределах определенной адресной зоны (бесплатная доставка в пределах Российской Федерации);
   * для заказов, содержащих определенное количество продуктов (купи 3 и более и получи бесплатную доставку);
   * для заказов с определенным диапазоном веса продуктов (бесплатная доставка заказов весом до 200 г).
   
   При необходимости, можно настроить комплексные условия на основе сочетаний условий выше (бесплатная доставка в пределах Российской Федерации при сумме заказа выше RUB 3000).

Рассмотрим, как настраивается бесплатная доставка на основе различный условий.

   *  [Пример 1: Бесплатная доставка при сумме заказа выше RUB 3000](#example-1-free-shipping-on-orders-over-50);
   *  [Пример 2: Бесплатная доставка в пределах Российской Федерации](#example-2-free-shipping-within-germany);
   *  [Пример 3: Бесплатная доставка, если в заказе 3 продукта и более](#example-3-free-shipping-on-orders-of-3-or-more-items)
   *  [Пример 4: Бесплатная доставка при весе заказа до 200 г](#example-4-free-shipping-on-orders-of-up-to-200-g-weight)
   * [Пример 5: Бесплатная доставка в пределах Российской Федерации при сумме заказа выше RUB 3000](#example-5-free-shipping-on-orders-over-50-shipped-within-Germany) (комбинированные условия)

## Пример 1: Бесплатная доставка при сумме заказа выше RUB 3000

1.  Откройте страницу **Способы доставки** (**Настройка магазина / Доставка**):

    1.  Нажмите **Добавить способ доставки**.
        ![xc5_freeshipping_add_shipmethod.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_add_shipmethod.png)

    2.  В открывшемся диалоговом окне перейдите на вкладку **Ручная настройка**.
        ![xc5_freeshipping_custom_table_rates_tab.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_custom_table_rates_tab.png)

    3.  Внесите общую информацию о способе доставки и настройте расчет стоимости:
        *   Укажите название способа доставки (например, _Бесплатная доставка при сумме заказа выше RUB 3000_).
        *   В поле **Зона доставки** укажите адресную зону, в которой будет действовать этот способ доставки.
        *   Установите базу для расчета _Стоимость товаров_ и значение соответствующего поля **Стоимость товаров** _RUB 3000 - $ ∞_. Поля **фиксированный тариф**, **за единицу товара**, **%** и **за единицу веса** не требуют заполнения.
        ![xc5_freeshipping_method_over50.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_over50.png)
        
    4.  Нажмите Создать.
        ![xc5_freeshipping_method_over50_create.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_over50_create.png)

    5.  Активируйте новый способ доставки.
        ![xc5_freeshipping_method_over50_active.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_over50_active.png)

2.  В настройках всех продуктов, для которых действует новый способ доставки, должна быть включена опция **Требуется доставка**.
    ![xc5_freeshipping_requires_shipping.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_requires_shipping.png)

Настройка завершена. Новый способ доставки будет доступен покупателям, сумма заказов которых RUB 3000 и выше.
    ![xc5_freeshipping_method_over50_checkout.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_over50_checkout.png)
    

## Пример 2: Бесплатная доставка в пределах Российской Федерации

1.  В панели управления магазина откройте страницу **Настройки магазина / Страны, области и зоны** и создайте зону доставки Российская Федерация.
       ![xc5_freeshipping_germany_zone.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_germany_zone.png)

2.  Откройте страницу Способы доставки (**Настройка магазина / Доставка**):

    1.  Нажмите **Добавить способ доставки**.
        ![xc5_freeshipping_add_shipmethod.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_add_shipmethod.png)

    2.  В открывшемся диалоговом окне перейдите на вкладку **Ручная настройка**.
        ![xc5_freeshipping_custom_table_rates_tab.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_custom_table_rates_tab.png)

    3.  Внесите общую информацию о способе доставки и настройте расчет стоимости:
        *   Укажите название способа доставки (например, _Бесплатная доставка в пределах Российской Федерации_).
        *   В поле **Зона доставки** выберите новую зону (_Российская Федерация_).
        *   Никакие другие поля не требуют заполнения.
        ![xc5_freeshipping_method_germany.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_germany.png)
        
    4.  Нажмите Создать.
        ![xc5_freeshipping_method_germany_create.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_germany_create.png)

    5.  Активируйте новый способ доставки:
        ![xc5_freeshipping_method_germany_active.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_germany_active.png)
       
3.  В настройках всех продуктов, для которых действует новый способ доставки, должна быть включена опция **Требуется доставка**.
    ![xc5_freeshipping_requires_shipping.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_requires_shipping.png)

Новый способ доставки создан. Бесплатная доставка будет предложена покупателям, адрес доставки которых входит в указанную зону доставки (_Российская Федерация_).
     ![xc5_freeshipping_method_germany_checkout.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_germany_checkout.png)
     
    
## Пример 3: Бесплатная доставка, если в заказе 3 продукта и более

1.  Откройте страницу Способы доставки (**Настройка магазина / Доставка**):

    1.  Нажмите **Добавить способ доставки**.
        ![xc5_freeshipping_add_shipmethod.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_add_shipmethod.png)

    2.  В открывшемся диалоговом окне перейдите на вкладку **Ручная настройка**.
        ![xc5_freeshipping_custom_table_rates_tab.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_custom_table_rates_tab.png)

    3.  Внесите общую информацию о способе доставки и настройте расчет стоимости:
        *   Укажите название способа доставки (например, _Бесплатная доставка, если в заказе 3 продукта и более_).
        *   В поле **Зона доставки** выберите адресную зону, в которую вы будете доставлять товары данным способом.
        *   Укажите базу для расчета _Количество товаров_ и значение соответствующего поля **Количество товаров** _3 - ∞_. Поля **фиксированный тариф**, **за единицу товара**, **%** и **за единицу веса** не требуют заполнения.
        ![xc5_freeshipping_method_3items.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_3items.png)
        
    4.  Нажмите Создать.
        ![xc5_freeshipping_method_3items_create.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_3items_create.png)

    5.  Активируйте новый способ доставки.
        ![xc5_freeshipping_method_3items_active.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_3items_active.png)

2.  В настройках всех продуктов, для которых действует новый способ доставки, должна быть включена опция **Требуется доставка**.
    ![xc5_freeshipping_requires_shipping.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_requires_shipping.png)

Настройка завершена. Бесплатная доставка будет доступна покупателям, в заказах которых 3 и более продукта.
    ![xc5_freeshipping_method_3items_checkout.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_3items_checkout.png)


## Пример 4: Бесплатная доставка при весе заказа до 200 г

1.  Откройте страницу Способы доставки (**Настройка магазина / Доставка**):

    1.  Нажмите **Добавить способ доставки**.
        ![xc5_freeshipping_add_shipmethod.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_add_shipmethod.png)

    2.  В открывшемся диалоговом окне перейдите на вкладку **Ручная настройка**.
        ![xc5_freeshipping_custom_table_rates_tab.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_custom_table_rates_tab.png)

    3.  Внесите общую информацию о способе доставки и настройте расчет стоимости:
        *   Укажите название способа доставки (например, _Бесплатная доставка при весе заказа до 200 г_).
        *   В поле **Зона доставки** выберите адресную зону, в которую вы будете доставлять товары данным способом.
        *   Выберите базу для расчета _Вес_ и укажите диапазон веса _0 - 0.2_. Единица веса по умолчанию должна быть килограмм. Проверьте единицу измерения веса магазина на странице **Настройка магазина / Локализация**. Поля **фиксированный тариф**, **за единицу товара**, **%** и **за единицу веса** не требуют заполнения.
        ![xc5_freeshipping_method_weight200.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_weight200.png)
        
    4.  Нажмите Создать.
        ![xc5_freeshipping_method_weight200_create.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_weight200_create.png)

    5.  Активируйте новый способ доставки.
        ![xc5_freeshipping_method_weight200_active.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_weight200_active.png)

2.  В настройках всех продуктов, для которых действует новый способ доставки, должна быть включена опция **Требуется доставка**.
    ![xc5_freeshipping_requires_shipping1.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_requires_shipping1.png)

Способ доставки настроен. Бесплатная доставка будет предложена покупателям, вес всех продуктов в заказах которых не превышает 200 г.
    ![xc5_freeshipping_method_weight200_checkout.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_weight200_checkout.png)

## Пример 5: Бесплатная доставка в пределах Российской Федерации при сумме заказа выше RUB 3000 (комбинированные условия)

1.  В панели управления магазина откройте страницу **Настройки магазина / Страны, области и зоны** и создайте зону доставки _Российская Федерация_.
       ![xc5_freeshipping_germany_zone.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_germany_zone.png)

2.  Откройте страницу **Способы доставки** (**Настройка магазина / Доставка**):

    1.  Нажмите **Добавить способ доставки**.
        ![xc5_freeshipping_add_shipmethod.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_add_shipmethod.png)

    2.  В открывшемся диалоговом окне перейдите на вкладку **Ручная настройка**.
        ![xc5_freeshipping_custom_table_rates_tab.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_custom_table_rates_tab.png)

    3.  Внесите общую информацию о способе доставки и настройте расчет стоимости:
        *   Укажите название способа доставки (например, _Бесплатная доставка в пределах Российской Федерации при сумме заказа выше RUB 3000_).
        *   В поле **Зона доставки** выберите новую зону (_Российская Федерация_).
        *   Выберите _Стоимость товаров_ как основу для расчета и в поле **Стоимость товаров** укажите диапазон сумм _RUB 3000 - $ ∞_. Поля **фиксированный тариф**, **за единицу товара**, **%** и **за единицу веса** не требуют заполнения.
        ![xc5_freeshipping_method_over50_germany.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_over50_germany.png)
        
    4.  Нажмите Создать:
        ![xc5_freeshipping_method_over50_germany_create.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_over50_germany_create.png)

    5.  Активируйте новый способ доставки:
        ![xc5_freeshipping_method_over50_germany_active.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_over50_germany_active.png)

3.  В настройках всех продуктов, для которых действует новый способ доставки, должна быть включена опция **Требуется доставка**.
    ![xc5_freeshipping_requires_shipping.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_requires_shipping.png)

Сособ доставки настроен. Бесплатная доставка будет предложена покупателям, сумма заказа которых составляет RUB 3000 и выше, а адрес доставки входит в указаную зону (_Российская Федерация_).
    ![xc5_freeshipping_method_over50_germany_checkout.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_over50_germany_checkout.png)

_Дополнительная информация:_

   * {% link "Free shipping on specific products" ref_IU9J0uuT %}



