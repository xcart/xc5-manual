---
lang: ru
layout: article_with_sidebar
updated_at: '2017-11-09 12:54 +0400'
identifier: ref_ELG1SBUJ
title: Стоимость доставки
order: 50
published: true
---
Индивидуальную стоимость доставки для одного продукта можно настроить с помощью модуля **Free shipping and Shipping freights**, разработанного командой X-Cart. Модуль входит в X-Cart Business, X-Cart Multivendor и X-Cart Ultimate.
    ![1.jpg]({{site.baseurl}}/attachments/ref_ELG1SBUJ/1.jpg)

Например, в магазине есть продукт _Говорящая копилка Алчный Гоблин_, который вы хотите доставлять за RUB 200.

Как это настроить:

1.  В панели управления магазина найдите продукт, для которого нужно задать индивидуальную стоимость доставки (_Говорящая копилка Алчный Гоблин из Диабло_).
2.  Нажмите на название продукта, чтобы открыть страницу редактирования продукта.
3.  На вкладке **Общее** найдите опцию **Фиксированная стоимость доставки** и укажите нужное значение (RUB 200 в нашем случае).
    ![2.jpg]({{site.baseurl}}/attachments/ref_ELG1SBUJ/2.jpg)

4.  Нажмите Обновить продукт.

На случай, когда в корзине покупателя только продукты с фиксированной стоимостью доставки, и других подходящих способов доставки в магазине нет, необходим способ доставки, который можно будет выбрать во время оформления заказа. Для того есть способ доставки **Доставка по фиксированной стоимости**. Он должен быть активирован:

![3.jpg]({{site.baseurl}}/attachments/ref_ELG1SBUJ/3.jpg)

Название и описание способа доставки можно редактировать. Нажмите на название способа и измените информацию:

![4.jpg]({{site.baseurl}}/attachments/ref_ELG1SBUJ/4.jpg)

Настройка завершена. Теперь каждая единица продукта _Говорящая копилка Алчный Гоблин из Диабло_ будет доставляться за RUB 200, две - за RUB 400, три - за RUB 600  и т.д. Если в заказе есть некоторое количество копилок Алчный Гоблин и еще какие-то продукты, стоимость доставки будет составлять RUB 200 за каждую копилку Алчный Гоблин плюс стоимость доставки, рассчитанная для остальных продуктов.

Фиксированная стоимость доставки может быть настроена только для материальных продуктов. Т.е. опция **Фиксированная стоимость доставки** отображается только при включенной опции **Требуется доставка**.