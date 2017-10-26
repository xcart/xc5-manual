---
lang: ru
layout: article_with_sidebar
updated_at: '2017-10-26 11:10 +0400'
identifier: ref_ZBKZ38v7
title: Настройка налога с продаж
order: 20
published: false
---
За расчет налогов в X-Cart 5 отвечает модуль **Налог с продаж**. Во время установки магазина этот модуль устанавливается и активируется автоматически. Если модуля нет в магазине, его можно легко {% link "установить из  Маркетплейса" ref_Vn1mMUw9 %}. 

Если модуль установлен, но отключен, {% link "активируйте" ref_uEnDBBA7 %} его.

![1.jpg]({{site.baseurl}}/attachments/ref_ZBKZ38v7/1.jpg)

Настройка налогов в X-Cart 5 не представляет большой сложности, т.к. функциональность X-Cart позволяет установить даже самые сложные формулы расчета налогов: налог может рассчитываться по-разному в зависимости от класса налогов продуктов в заказе, от адреса покупателя и от группы пользователей, к которой принадлежит покупатель. 

Данная статься рассказывает, как настроить расчет налогов с помощью модуля Налог с продаж. 

## Настройка налога с продаж

Прежде чем настроить налог:

1.  Проверьте продукты, для которых нужно настроить налог, - для каждого из них должен быть установлен класс налога. Можно создать новые классы налога или использовать стандартный класс налога, который установлен для всех продуктов по умолчанию.  

    Дополнительная информация:
    
    *   {% link "Creating tax classes" ref_pAWOdG8N#creating-tax-classes %};
    
    *   {% link "Assigning tax classes to products" ref_pAWOdG8N#assigning-tax-classes-to-products %}.

2.  В магазине должны быть настроены зоны доставки. Они нужны, чтобы применять разные налоговые ставки в зависимости от адреса покупателя.

    Дополнительная информация:

    *   {% link "Setting up destination (address) zones" ref_r68iO5Rm %}
    
3.  В магазине должны быть настроены группы покупателей. Они нужны, чтобы применять разные налоговые ставки в зависимости от группы, в которую входит покупатель..

    Дополнительная информация:

    *   {% link "Adding user membership levels" ref_9ITFspcC %}
    
Настройка налога с продаж:

1.  В панели управления магазина откройте страницу **Настройка магазина / Налоги**
    ![2.jpg]({{site.baseurl}}/attachments/ref_ZBKZ38v7/2.jpg)
    
2.  Перейдите на вкладку **Налог с продаж**
    ![3.jpg]({{site.baseurl}}/attachments/ref_ZBKZ38v7/3.jpg)
    
3.  Заполните поля в разделе **Общие настройки налога**
    ![4.jpg]({{site.baseurl}}/attachments/ref_ZBKZ38v7/4.jpg)
    
    *   В поле **Налог** нужно написать общее название, описывающее тип  налога. Это название налога будет видно на странице оплаты и в счете у покупателя. Пример: налог, налог с продаж, налог на товары и т.п.
    *   **Использовать одни и те же ставки налога для всех групп покупателей** - отметьте эту опцию, если налог должен рассчитываться одинаково для всех групп покупателей. 
    *   В поле **Адрес для расчета налога с продаж** следует указать адрес, на основе которого будет рассчитываться налог.  Можно выбрать _Адрес получателя_ или _Адрес плательщика_. По выбранному адресу будет определена зона адресов, по которой, в свою очередь, будет выбрана налоговая ставка. Например, в онлайн магазинах в США налог должен рассчитываться по месту доставки товара, а не по месту его оплаты. Поэтому, владелец магазина в США в этом поле выбрал бы _Адрес получателя_. 
    
4.  Создайте правило (или несколько) расчета налога:

    *   Если налоговая ставка должна применяться к стоимости продуктов в заказе (сумма заказа или сумма заказа с учетом скидок) или к стоимости продуктов с учетом стоимости доставки (сумма заказа+стоимость доставки или сумма заказа с учетом скидки+стоимость доставки), настройте налоговые ставки в разделе **Основные ставки налогов**:

        1.  В меню **Налогооблагаемая база** выберите, от какой суммы будет рассчитываться налог. 
            ![5.jpg]({{site.baseurl}}/attachments/ref_ZBKZ38v7/5.jpg)
            Возможные варианты:
            *   _Сумма заказа+стоимость доставки;_
            *   _Сумма заказа с учетом скидки+стоимость доставки;_
            *   _Сумма заказа;_
            *   _Сумма заказа с учетом скидки;_
            *   _Индивидуальные настройки для каждой ставки налога._ Например, если вы выбрали сумма заказа+стоимость доставки, сумма налога будет рассчитана как процент от суммы заказа за вычетом скидок и от стоимости доставки. 

            Чтобы применять различные налоги к различным суммам, выберите последний вариант - _Индивидуальные настройки для каждой ставки налога_. Эта опция позволяет выбрать базу для расчета налога отдельно для каждой ставки налога. 

        2.  В разделе **Основные ставки налогов** задайте налоговые ставки. 
            ![6.jpg]({{site.baseurl}}/attachments/ref_ZBKZ38v7/6.jpg)
            Вам поможет раздел **Настройка ставки налога с продаж** далее в этой статье.

    *   Если налог нужно применять только к стоимости доставки, нажмите ссылку **Нажмите здесь, чтобы задать ставки налогов на стоимость доставки**.
        ![7.jpg]({{site.baseurl}}/attachments/ref_ZBKZ38v7/7.jpg)
        Откроется раздел **Ставки налогов на стоимость доставки**. 
        ![8.jpg]({{site.baseurl}}/attachments/ref_ZBKZ38v7/8.jpg)
        Здесь вы можете настроить налоги только на доставку. обратитесь к параграфу  Вам поможет раздел  **Настройка ставки налога с продаж** далее в этой статье.

5.  У поля **Налог** есть переключатель **Включен / Выключен**. Чтобы налоги с продаж действовали в магазине, этот переключатель должен быть **Включен** (зеленого цвета).
    ![9.jpg]({{site.baseurl}}/attachments/ref_ZBKZ38v7/9.jpg)
    
6.  Нажмите **Сохранить**.

## Setting up sales tax rates

You need to set up sales tax rates to {% link "configure your sales tax" ref_aJPK4DHN %}. Depending on whether you need to set up general tax rates or tax rates that apply only to shipping charges, use the appropriate section: **General tax rates** or **Tax rates on shipping cost**. The procedure for setting up general tax rates and tax rates on shipping cost is essentially the same:

1.  Click the **New rate** button.
    ![]({{site.baseurl}}/attachments/8225533/8716429.png) 
2.  In the section that expands below, provide information about your new sales tax rate:
    ![]({{site.baseurl}}/attachments/8225533/8716431.png)

    *   **Tax class**: Specify the type of products (tax class) to which the tax rate should be applied. For example, if you select the _Default tax class_ option here, the tax rate will be applied to all the products that have the default tax class assigned. 
    *   **User membership**: Specify the user membership level for which the tax rate should be applied. The option _Ignore membership_ allows you to create a tax rate that will be applied to all orders irrespective of the buyer's membership (**Note**: The "User membership" column becomes available when the option "Use the same tax rates for all user membership levels" is disabled in the common tax settings).
    *   **Zone**: Specify the address zone to which the tax rate should be applied. The tax rate will be applied to orders of customers whose address belongs to the selected address zone. Whether it is their Billing or Shipping address depends on the option selected in the **Address for sales tax calculation** field of the sales tax configuration.
    *   **Taxable base**: Specify the type of costs based on which your tax rate should be calculated. (**Note: **The "Taxable base" column becomes available for general tax rates when the option _Individual settings for every rate_ is selected in the "Taxable base" field of the sales tax configuration. For tax rates on shipping cost the ability to specify a taxable base is not provided, because in this case the taxable base is always the same: the cost of shipping).  
    *   **Rate**: Specify the tax rate amount as a percentage of the selected taxable base.
3.  If necessary, use the **New rate** button to add rows for more tax rates. Complete the fields in each row as you require.
4.  Click the **Save changes** button at the bottom of the page to save the changes.
    ![]({{site.baseurl}}/attachments/8225533/8716432.png)

## Enabling/Disabling sales tax calculation

Once configured and enabled, sales tax calculation can be disabled/re-enabled using the **On**/**Off** button to the right of the **Tax title** field on the **Sales tax** panel in the Taxes section (**Store setup** > **Taxes**). When sales tax calculation is enabled, the **On/Off** icon on the button is green. When it is disabled, the icon is grey.

![]({{site.baseurl}}/attachments/8225533/8716428.png)

_Related pages:_

*   {% link "Setting up tax classes" ref_pAWOdG8N %}
*   {% link "Assigning tax classes to products" ref_pAWOdG8N#assigning-tax-classes-to-products %}
*   {% link "Setting up destination (address) zones" ref_r68iO5Rm %}
*   {% link "Adding user membership levels" ref_9ITFspcC %}
*   {% link "Setting up VAT / GST (for the UK, EU, Australia, etc)" ref_Rzp45QlN %}
*   {% link "Setting up Canadian taxes" ref_hxmof6xX %}
