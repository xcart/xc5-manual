---
lang: ru
layout: article_with_sidebar
updated_at: '2017-11-08 11:33 +0400'
identifier: ref_65Cs4QwQ
title: ''
order: 100
published: false
---
Принимая решения о стоимости доставки товаров покупателям, важно учесть, сколько доставка обходится вашему бизнесу. Наиболее точную оценку стоимости доставки предоставляют онлайн службы транспортных компаний. Также, можно установить и настроить свои расценки на доставку. 

В X-Cart можно задать уникальные ставки расчета стоимости доставки:

*   по промежуточной сумме заказа (стоимость доставки будет зависеть от промежуточной суммы заказа);
*   по весу (стоимость доставки будет зависеть от веса продуктов в заказе);
*   по количеству продуктов в заказе (стоимость доставки будет зависеть от количества продуктов в заказе);
*   по любой комбинации промежуточной суммы заказа, веса и количества продуктов (стоимость доставки будет зависеть нескольких параметров).

Как создать способ доставки с настраиваемыми ставками:

1.  В панели управления магазина откройте раздел Способы доставки (страница **Настройка магазина / Доставка**):
    ![]({{site.baseurl}}/attachments/9306242/9437466.png)
2.  Нажмите **Добавить способ доставки**:
    ![]({{site.baseurl}}/attachments/9306242/9437467.png)
    Откроется диалоговое окно, в котором можно выбрать тип стоимости доставки:
    ![]({{site.baseurl}}/attachments/9306242/9437468.png)
3.  Перейдите на вкладку **Ручная настройка**:
    ![]({{site.baseurl}}/attachments/9306242/9437469.png)
4.  Укажите общую информацию о способе доставки:
    ![]({{site.baseurl}}/attachments/9306242/9437470.png)

    *   **Название**: название способа доставки, которое будут видеть покупатели.
    *   **Время доставки**: предположительное время доставки.
    *   **Зона доставки**: зона адресов, внутри которой будет действовать способ доставки. Если вы еще не создали эту адресную зону, пройдите по ссылке Управление зонами и нажмите Создать зону.
    *   **База для расчета**: в поле Тариф на основе выберите один или несколько параметров, на базе которых будет рассчитываться стоимость доставки.
        *   _Подытог заказа_ - для расчета стоимости доставки по сумме заказа. Пример: фиксированная плата за доставку RUB 500 при промежуточной сумме заказа до RUB 3000 и бесплатная доставка при сумме выше RUB 3000.
        *   _Вес_ - для расчета стоимости доставки по весу продуктов в заказе. Пример:  фиксированная плата за доставку RUB 500 при весе заказа до 5 кг и RUB 200 за 1 кг при весе заказа выше 5 кг. Чтобы использовать этот тип расчета, необходимо указать точный вес в настройках всех продуктов, для которых действует этот способ доставки.
        *   _Продукты в  заказе_ - для расчета стоимости доставки по количеству продуктов в заказе. Пример: фиксированная стоимость доставки RUB 300, если в заказе 5 или менее продуктов, и RUB 50 за продукт, если в заказе 6 или более продуктов.
        *   _Подытог заказа, вес, продукты_ - для расчета стоимости доставки нескольким параметрам. Пример: фиксированная стоимость доставки RUB 500 при промежуточной сумме заказа до RUB 3000 и весе до 5 кг; бесплатная доставка при промежуточной сумме заказа RUB 300 и выше и весе до 5 кг, и фиксированная стоимость доставки RUB 600 при весе заказа выше 5 кг. Для использования этого способа расчета доставки необходимо указать вес в настройках  всех продуктов, для которых действует этот способ доставки.

5.  Как составить таблицу расценок на доставку для нового способа доставки:

    In the lower part of the screen where you have provided the details of your shipping method, a form is provided that will help you to create your custom rates table for this method. What you see here is, in fact, the first row of your table - with the default zero values. 
    ![]({{site.baseurl}}/attachments/9306242/9437471.png)
    The set of fields that you see in this table row may be different depending on the value of the "Table based on" setting above. For example, if you have chosen to base your table on "_Subtotal, weight, items_", there will be more fields; for lack of space, they will be displayed on two rows one below the other (as shown in the screenshot below):
    ![]({{site.baseurl}}/attachments/9306242/9437472.png)
    But in any case you should remember that all these fields pertain to the first row of your custom rates table, and all of them are intended for your first shipping rate.
    To create a shipping rate, you will need to adjust the values in the fields of this table row so that they form a rule according to which the shipping rate will be calculated. 
    If necessary, you will be able to add more table rows for more rates. In the end, be sure to save your changes.

    For example, let's configure a custom rates table that will allow us to offer our customers:
    *   $7 flat rate shipping for orders with a subtotal of up to $50 - if the order weight is up to 10 lb, 
    *   free shipping for orders with a subtotal of $50 or more - if the order weight is up to 10 lb,
        and
    *   $10 flat rate shipping for orders weighing over 10 lb.

        Our first rate needs to be "$7 flat rate shipping for orders with a subtotal of up to $50 - if the order weight is up to 10 lb". To get this rate, we need to configure our first table row as follows:
    ![]({{site.baseurl}}/attachments/9306242/9437473.png)
    *   Subtotal range: $0.00 - $49.99 
    *   Weight range: 0 - 10 lb 
    *   flat rate: $7
    Once we're done with the first rate, let's add two more table rows for the rates "Free shipping for orders with a subtotal of $50 or more - if the order weight is up to 10 lb" and "$10 flat rate shipping for orders weighing over 10 lb" . To add a new blank row, we'll use the [+] button:
    ![]({{site.baseurl}}/attachments/9306242/9437474.png)
    We'll configure these two rows we have added like so:
    ![]({{site.baseurl}}/attachments/9306242/9437475.png)
    "Free shipping for orders with a subtotal of $50 or more - if the order weight is up to 10 lb":
    *   Subtotal range: $50 - $  ∞
    *   Weight range: 0 - 10 lb
    *   flat rate: $0

        "$10 flat rate shipping for orders weighing over 10 lb":
    *   Subtotal range: $0 - $  ∞
    *   Weight range: 10 lb - ∞ 
    *   flat rate: $10

        We are now ready to save our table.

6.  Once you're satisfied with your rates table configuration, save your changes. The new shipping method will be added.

7.  Make sure the shipping method is active. 

8.  Make sure that all the products that will be shipped using this shipping method have the option **Requires shipping** (in older X-Cart versions - **Shippable**) enabled.

That is all. Now the shipping rates for orders shipped using this method will be calculated based on the custom rates table you have created.

