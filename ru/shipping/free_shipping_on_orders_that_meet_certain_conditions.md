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

1.  Откройте страницу **Способы доставк**и (**Настройка магазина / Доставка**):

    1.  Нажмите **Добавить способ доставки**.
        ![xc5_freeshipping_add_shipmethod.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_add_shipmethod.png)

    2.  В открывшемся диалоговом окне перейдите на вкладку **Ручная настройка**.
        ![xc5_freeshipping_custom_table_rates_tab.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_custom_table_rates_tab.png)

    3.  Внесите общую информацию о способе доставки и настройте расчет стоимости:
        *   Укажите название способа доставки (например, _Бесплатна доставка при сумме заказа выше RUB 3000_).
        *   В поле **Зона доставки** укажите адресную зону, в которой будет действовать этот способ доставки.
        *   Установите базу для расчета _Стоимость товаров_ и значение соответствующего поля **Стоимость товаров** _RUB 3000 - $ ∞_. Поля **фиксированный тариф**, **за единицу товара**, **%** и **за единицу веса** не требуют заполнения.
        ![xc5_freeshipping_method_over50.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_over50.png)
        
    4.  Save your changes.
        ![xc5_freeshipping_method_over50_create.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_over50_create.png)

    5.  Make sure the method you have configured is active.
        ![xc5_freeshipping_method_over50_active.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_over50_active.png)

2.  Make sure that all the products that can be shipped using this shipping method have the option **Requires shipping** (in older X-Cart versions - **Shippable**) enabled.
    ![xc5_freeshipping_requires_shipping.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_requires_shipping.png)

That is all. You should now have a free shipping method that will be displayed at checkout only if the customer's order amount is $50 or more.
    ![xc5_freeshipping_method_over50_checkout.png]({{site.baseurl}}/attachments/ref_T9GhEfev/xc5_freeshipping_method_over50_checkout.png)

