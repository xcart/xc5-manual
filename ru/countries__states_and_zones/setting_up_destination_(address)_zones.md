---
lang: ru
layout: article_with_sidebar
updated_at: '2017-10-27 17:12 +0400'
identifier: ref_fVgOaXam
title: ''
order: 100
published: false
---
## Что такое зона доставки?

В X-Cart 5 зоны позволяют рассчитывать налог и стоимость доставки для разных географического местонахождений покупателей.  Зона - это набор стран, штатов/областей и индексов, которые составляют регион. К региону применяются свои индивидуальные правила доставки.

Несколько примеров действия зон доставки:

*   Налог с продаж в размере 7% для Нью Джерси в США: Создайте зону доставки, включающую только этот штат, Нью Джерси. Затем, настройте соответствующую ставку налога для данной зоны доставки. 
*   Бесплатная доставка в пределах Великобритании, фиксированная стоимость доставки £7.50 во все другие страны Европы и фиксированная стоимость доставки £13.95 во все страны мира: Создайте три зоны доставки - зону 1, включающую только Соединенное Королевство; зону 2, включающую все страны Европы, в которые вы будете доставлять; зону 3, включающую все остальные страны, куда вы будете доставлять свои товары. Теперь настройте налог для каждой из этих зон.
*   Бесплатная доставка на адреса в непосредственной близости от магазина: Создайте зону доставки по индексу своего магазина (или нескольким индексам прилегающих территорий) и настройте бесплатную доставку для этой зоны адресов.

Количество зон доставки зависит от настроек налогов и доставки. Зон доставки должно быть столько, сколько необходимо для действия настроенных правил расчета налогов и стоимости доставки. Зоны для налогов и зоны для доставки могут не совпадать.

## Как X-Cart определяет адресную зону покупателя

Чтобы определить, какой налог и какую стоимость доставки применить к заказу, X-Cart проверяет, к какой зоне доставки относится адрес покупателя. Для этого X-Cart последовательно проверяет каждое поле адреса - страну, область, индекс - и сравнивает данные с этими же полями зон доставки. Если X-Cart находит страну покупателя в составе стран какой-то зоны, X-Сart переходит к проверке области. Если в найденной зоне не указаны области (т.е. в нее входят все области страны), значит, адрес покупателя входит в эту зону доставки. Если для найденной зоны указаны области, и области покупателя нет в этом списке, значит, адрес покупателя не входит в данную зону доставки. В этом случае, X-Cart переходит к проверке другой зоны доставки, в которую мог бы входить адрес покупателя. Если для зоны указаны области, и область покупателя есть в этом списке, X-Cart переходит к проверке индекса. Аналогично, если для зоны не указаны индексы, адрес покупателя входит в данную зону доставки, если указаны - X-Cart сравнивает индекс покупателя с индексами зоны.   

Если X-Cart находит адрес покупателя в нескольких зонах, он должен выбрать наиболее подходящую. Чем больше параметров зоны совпадает с адресом покупателя (страна, область, индекс), тем более подходящей считается зона доставки.  Чтобы определить налог и стоимость доставки для заказа, когда адрес покупателя входит в несколько зон доставки, прежде всего, X-Cart проверяет расценки наиболее подходящей зоны. Если для этой зоны не заданы ставка налоги и стоимость доставки, X-Cart переходит к проверке расценок следующей подходящей зоны. Последняя зона, до которой может дойти проверка - Все адреса. Это стандартная зона доставки, она не может быть более или менее подходящей и используется, когда ни одна другая зона доставки не подходит. 

## Creating zones

For example, we need to create a zone "Atlantic Canada" that would include four territories: New Brunswick, Prince Edward Island, Nova Scotia and Newfoundland and Labrador. 

Let's do it:

1.  In your store's Admin area, go to **Store setup > Countries, states and zones**.
    ![]({{site.baseurl}}/attachments/6389840/9437215.png)
2.  Click the **Zones** tab:
    ![]({{site.baseurl}}/attachments/6389840/9437216.png)
    This opens the Zones section where you can create and manage your address zones:
    ![]({{site.baseurl}}/attachments/6389840/9437225.png)

3.  Click the **Create zone** button.
    ![]({{site.baseurl}}/attachments/6389840/9437217.png)
    In the list of your store's zones, a new blank line will be added:
    ![]({{site.baseurl}}/attachments/6389840/9437224.png)
4.  Use the new blank line in the list of zones to specify the name of the destination zone you will be creating (For the sake of example, we will use the name "Atlantic Canada"); then click the **Save changes** button at the bottom of the page:

    ![]({{site.baseurl}}/attachments/6389840/9437218.png)The new zone will be added to the list:
    ![]({{site.baseurl}}/attachments/6389840/9437219.png)

5.  Hover your cursor over the name of the zone you have created. The field with the zone name will be displayed as editable, and an **Edit** button will be displayed next to it. If necessary, you can edit the zone name right here. To configure the zone details, click the **Edit** button:
    ![]({{site.baseurl}}/attachments/6389840/9437220.png)
    A page with the zone details will be displayed:
    ![]({{site.baseurl}}/attachments/6389840/9437221.png)

6.  Adjust the zone details as needed. 

    *   If necessary, edit the name of the zone in the **Zone name** field. 

    *   Use the sections **Countries**, **States **and **Zip/postal code masks** to specify the regions/territories that belong to the zone being edited. In the sections **Countries** and **States**, you need to select all the countries and states that should be part of the zone from the box(es) on the left-hand side and move them to the box(es) on the right-hand side using the "**>>**" button. 

        ![]({{site.baseurl}}/attachments/6389840/9437222.png)
       
        In the section Zip/postal masks, you need to specify the zip/postal codes (or zip/postal code masks) that should belong to the zone.
 
        Zip/postal code masks help you specify zip/postal code ranges. You simply replace any number of digits with the "%" symbol. For example, "1001%" corresponds to all the zip/postal codes in the "10010 - 10019" range, "102%" - to all the zip/postal codes in the "10200 - 10299" range.

        Please be sure to place each zip/postal code mask entry or full zip/postal code on a separate line like so:
        
        1001%
        
        102%
        
        
        To configure the zone "Atlantic Canada", we would need to select the following territories:

        *   in the section **Countries** - Canada;

        *   in the section **States** - Canada:New Brunswick, Canada:Newfoundland and Labrador, Canada:Nova Scotia and Canada:Prince Edward Island;

        *   in the section **Zip/postal code masks** - nothing.

7.  Once you are done configuring the zone, click the **Save changes** button at the bottom of the page to save the changes.
    ![]({{site.baseurl}}/attachments/6389840/9437223.png)
    The zone details will be saved.

## The "All Addresses" (default) zone


