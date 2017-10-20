---
lang: ru
layout: article_with_sidebar
updated_at: '2017-10-20 16:42 +0400'
identifier: ref_guGkzxGn
title: ''
order: 100
published: false
---
Для приема оплаты от покупателей, вам нужно настроить один или несколько способов оплаты в магазине. На странице **Настройки магазина** / **Прием платежей** вы можете управлять способами оплаты:

![1.jpg]({{site.baseurl}}/attachments/ref_guGkzxGn/1.jpg)

Данная статья описывает:

*   [Просмотр списка способов оплаты магазина](#viewingyour-stores-payment-methods-list);
*   [Создание нового способа оплаты](#adding-payment-methods);
*   [Изменение настроек существующих способов оплаты](#editing-existing-payment-methods);
*   [Включение и отключение способов отплаты](#enabling--disabling-payment-methods);
*   [Удаление способов оплаты](#deleting-payment-methods).

## Просмотр списка способов оплаты магазина

В X-Cart можно настроить два вида способов оплаты:

1.  _Оффлайн_ способы оплаты (покупатель может оплатить товар, не предоставляя платежные данные). Например, заказ по телефону, чек, почтовый перевод, банковский перевод, наложенный платеж и т.д.  
2.  _Онлайн_ способы оплаты (покупатель вводит платежную информацию онлайн, платеж сразу поступает администратору магазина через платежную систему, которую использовал покупатель). Например, Paypal, Authorize.Net, 2Checkout, Skrill и т.д.

На странице **Настройки магазина** / **Прием платежей** в разделе **"Конфигурация"** вы найдете два раздела - **Онлайн методы** и **Оффлайн методы**:

![2.jpg]({{site.baseurl}}/attachments/ref_guGkzxGn/2.jpg)

Рядом с названием каждого способа оплаты в списке есть переключатель **"НЕАКТИВНЫЙ / АКТИВНЫЙ"**, с помощью которого можно активировать или деактивировать способ оплаты: 

**АКТИВНЫЙ** (зеленый индикатор) - способ оплаты доступен покупателям

**НЕАКТИВНЫЙ** (серый индикатор) - способ оплаты недоступен покупателям

![4.jpg]({{site.baseurl}}/attachments/ref_guGkzxGn/4.jpg)

Кнопка **"Конфигурировать"** под названием каждого способа оплаты ведет на страницу настроек данного способа оплаты:

![5.jpg]({{site.baseurl}}/attachments/ref_guGkzxGn/5.jpg)

## Создание нового способа оплаты

_Онлайн_ и _оффлайн_ способы оплаты создаются в магазине по-разному. 

### Онлайн способы оплаты

В X-Cart 5 все способы оплаты представляют собой отдельные устанавливаемые модули. В новом, только что созданном магазине несколько модулей оплаты уже установлены по умолчанию. На странице **"Мои модули"** можно посмотреть, какие модули установлены, и найти соответствующие способы оплаты на странице **Настройка магазина** / **Прием платежей**:

1.  На странице **Настройка магазина** / **Прием платежей** в разделе "Онлайн методы" нажмите кнопку **"Добавить способ оплаты"**. 

    ![6.jpg]({{site.baseurl}}/attachments/ref_guGkzxGn/6.jpg)

    Откроется диалоговое окно со списком способов оплаты.:

    ![7.jpg]({{site.baseurl}}/attachments/ref_guGkzxGn/7.jpg)

    Справа в списке указан статус каждого способа оплаты:

    *   For methods that are installed and enabled, the button Settings is provided. This button allows you to access the method settings page where you can adjust the method name, description and other configuration settings, as well as deactivate the method if necessary.
    *   For methods that are installed, but not enabled, the button Add is provided. You can use this button to add the method to your payment methods list and access the method settings page in one click. Note that after adding any online method with the Add button you will still need to configure it.
    *   For methods that are not installed, the button Install is provided. This button allows you to download from the Marketplace and install the payment module needed to enable the chosen payment method.

To start using a certain online payment method:

1.  Make sure that the payment module you require is installed and enabled. If so, you should be able to see the respective payment method on the Online methods list in your store's Payment settings section (**Store setup > Payment methods**).
2.  If the payment method is not on the Online methods list, click the **Add payment method** button at the top right-hand corner of the Online methods section. 
    
    ![]({{site.baseurl}}/attachments/6389794/xc5_paymentmethods_add_online_method_click.png)
3.  In the popup box that opens, select the section you require: _All payment methods_ or _PayPal all-in-one solutions_.
4.  Locate the payment method you require and click the **Add (or Install)** button opposite its name.
5.  Once the chosen method is added to your store's list of online payment methods, configure the method settings and enable it using the **INACTIVE/ACTIVE** switch.

That is all. The payment method is active and ready to use.






