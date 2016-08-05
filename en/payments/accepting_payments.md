---
identifier: ref_Jq6Bsdrt
updated_at: 2014-03-28 00:00
layout: article_with_sidebar
lang: en
title: 'Accepting payments'
categories:
  - User manual

---

To accept payments from buyers, you need to enable one or more payment methods for your store. Payment methods are managed via the **Payment methods** section (**Store setup > Payments**):

![]({{site.baseurl}}/attachments/6389794/7602367.png?effects=drop-shadow)

In this section, you can:

*   [view your store’s list of payment methods](#viewingyour-stores-payment-methods-list);
*   [add new payment methods](#adding-payment-methods);
*   [edit the settings of existing payment methods](#editing-existing-payment-methods);
*   [change the availability of specific payment methods](#enabling--disabling-payment-methods);
*   [delete payment methods](#deleting-payment-methods).

# Viewing your store's payment methods list

X-Cart supports two types of payment methods:

1.  _Offline_ payment methods (methods that allow customers to check out without submitting payment information). For example, Phone Ordering, Check, Wire Transfer, etc.
2.  _Online_ payment methods (methods that allow customers to enter their payment information online, so you automatically receive the payment via the respective payment system). For example, Paypal, Authorize.Net, 2Checkout, Skrill, etc.

On the **Payment methods** page, offline payment methods can be found in the section **Offline methods**:

![]({{site.baseurl}}/attachments/6389794/7602370.png?effects=drop-shadow)

online payment methods - in the sections **Accepting credit cards online** and **Alternative payment methods**:

![]({{site.baseurl}}/attachments/6389794/7602369.png?effects=drop-shadow)

(The **Accepting credit cards online** section is intended for methods allowing users to pay using their credit card; for example, Paypal Advanced or Paypal Website Payments Pro. The **Alternative payment methods** section is for methods that support other types of payment; for example, Paypal Express Checkout, where customers can pay using their Paypal account).

On the snapshot above, the sections **Accepting credit cards online** and  **Alternative payment methods** do not have any methods listed in them - because the methods yet have to be added. 

The status of the On/Off control to the left of each method's name reflects the availability of the method to customers:

![]({{site.baseurl}}/attachments/6389794/7602383.png?effects=drop-shadow)

![]({{site.baseurl}}/attachments/7503950/7602222.jpg)(green icon) = the method is available on the storefront;
![]({{site.baseurl}}/attachments/7503950/7602223.png)(gray icon) = the method is not available (not visible to customers).

The Gear icon ![]({{site.baseurl}}/plugins/servlet/confluence/placeholder/unknown-attachment "gear_icon.png")opposite each payment method's name allows you to access the method's settings:

![]({{site.baseurl}}/attachments/6389794/7602384.png?effects=drop-shadow)

# Adding payment methods

How you add a new payment method for your store depends on whether this method will be an _online_ or an _offline_ one.

#### **Online payment methods:**

All online payment methods in X-Cart 5 are implemented as installable modules. Typically, a newly installed X-Cart store will have some payment modules already installed. You can check what modules are installed at your store via the **Installed Modules** section  (**Extensions > Installed modules**). 

To start using a certain online payment method:

1.  Make sure that the payment module you require is installed and enabled. If the payment module you need is not on your store's **Installed Modules** list, try searching X-Cart's Marketplace: you may be able to install the module you require from there. See {% link "Installing modules from the Marketplace" ref_Vn1mMUw9 %}.
2.  Go to the **Payment methods** section (**Store setup > Payments**) and see if the method you require is already listed on either the **Accepting credit cards online** or the **Alternative payment methods** section. If not, add it: 
    1.  In the appropriate section (**Accepting credit cards online** or **Alternative payment methods** - depending on the type of method you require), click the **Add payment method** button:
        ![]({{site.baseurl}}/attachments/6389794/6586421.png?effects=drop-shadow)
        A popup titled **Add payment method** will be opened.
    2.  In the **Add payment method** popup, locate the payment method you require and click the **Choose** button opposite its name:
        ![]({{site.baseurl}}/attachments/6389794/6586428.png?effects=drop-shadow)
        The chosen method will be added to your store's list of online payment methods. A page with the settings of the new payment method will be opened:
        ![]({{site.baseurl}}/attachments/6389794/7602371.png?effects=drop-shadow)
3.  Use the settings on the page to configure the payment method. Once you're done, be sure to save the changes. The settings will be saved, and you will be redirected back to the **Payment methods** page.
4.  On the **Payment methods** page, enable the payment method you have added and configured (Use the On/Off control opposite the payment method name. The green icon means that the payment method is enabled and available to buyers).

That is all. The payment method is enabled and ready to use.

#### **Offline payment methods:**

In a newly installed X-Cart store, the **Offline methods** section on the **Payment methods** page already contains some pre-configured offline payment methods. If needed, you can [edit](#editing-existing-payment-methods) them, or add more offline methods.

To add a new offline payment method:

1.  In the the **Offline methods** section of the **Payment methods** page (**Store setup > Payments**), click **Add payment method**:
    ![]({{site.baseurl}}/attachments/6389794/7602386.png?effects=drop-shadow)
    A popup allowing you to enter the details of the new payment method will be opened:
    ![]({{site.baseurl}}/attachments/6389794/7602387.png?effects=drop-shadow)
2.  Enter a name, instructions and description for the new method. HTML tags are allowed in the **Payment instructions** and **Description** fields.
3.  Click **Add**. The payment method details will be saved, and you will be redirected back to the **Payment methods** page.
4.  On the **Payment methods** page, enable the payment method you have added and configured (Use the On/Off control opposite the payment method name. The green icon means that the payment method is enabled and available to buyers).

That is all. The payment method is enabled and ready to use.

# Editing existing payment methods

It is possible to edit previously added payment methods.

To edit an existing method:

1.  On the **Payment methods** page (**Store setup > Payments**), locate the payment method that needs to be edited and click on the gear icon opposite its name.
    This opens the page with the payment method's settings.
    ![]({{site.baseurl}}/attachments/6389794/7602388.png?effects=drop-shadow)
2.  Edit the settings. 
3.  Click **Update** to save the changes.

The payment method settings will be updated.

# Enabling / Disabling payment methods

You can change the availability of a payment method by switching the On/Off control to the left of its name.

# Deleting payment methods

To remove a payment method from your store's payment methods list, click on the Trash icon ![]({{site.baseurl}}/attachments/7503950/8718936.png) opposite its name.