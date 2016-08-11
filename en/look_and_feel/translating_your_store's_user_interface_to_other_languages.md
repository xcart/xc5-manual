---
identifier: ref_NH3w8sSS
updated_at: 2015-09-30 00:00
layout: article_with_sidebar
lang: en
title: 'Translating your store&#39;s user interface to other languages'
categories:
  - User manual

---

Once you download X-Cart from [www.x-cart.com](http://www.x-cart.com/) and install it on your server, you get a store builder with the user interface displayed in the English language. 

However, you can turn your X-Cart into a truly multi-language solution by installing language translation modules. For example, there are some language translations that you can download from X-Cart Marketplace, including:

*   Russian
*   French
*   German
*   Dutch
*   British English

Icon

If you want to translate X-Cart into some other language, contact us at {% link "developers@x-cart.com" mailto:developers@x-cart.com %}. We will explain how this can be done and how you can get money out of it.

To install a language translation module from X-Cart Marketplace:

1.  In your store's Admin area, select **Modules**, then click __View more addons in Marketplace__ to go to X-Cart Marketplace.
2.  Locate the translation you require. For example, enter "translation" in the search field to find all translation modules in the Marketplace:
    ![]({{site.baseurl}}/attachments/6389832/8716781.png?effects=drop-shadow)

3.  Install and activate the translations you require like you do with any other modules from the Marketplace. See {% link "Installing modules from the Marketplace" ref_Vn1mMUw9 %}.

As a result, the translation modules you have installed should appear in the Installed Modules section in your store's Admin area:

![]({{site.baseurl}}/attachments/6389832/8719384.png?effects=drop-shadow)

Once you have more than one languages installed and enabled, language selectors will be provided both in the Admin and Customer areas of your X-Cart store.

Admin area:

![]({{site.baseurl}}/attachments/6389832/8716779.png?effects=drop-shadow)

Customer area:

![]({{site.baseurl}}/attachments/6389832/8716780.png?effects=drop-shadow)

Try switching the language in either of the areas, and you should see at least some of the words and phrases on the page you are viewing translated to the selected language. For example, here's what the Modules page in the Admin area looks like after switching the language of the interface in Admin to German (Note the language code "DE" in the language selector):

![]({{site.baseurl}}/attachments/6389832/8719385.png?effects=drop-shadow)

You may notice that some texts and labels do not get translated when you switch the language selector. For example, in the screenshot above you can still see the module description and the link "View more addons in Marketplace" displayed in the English language - instead of German. Well, things like this happen pretty often. In fact, the module description is fetched from the Marketplace,so the translation module has no power over its translation. As to the "View more addons in Marketplace" link, the respective label simply does not have a value for the German language. If we compare our installed translations in the Languages section (**Store setup** > **Translations**), we will see that the English translation has more than twice as many labels than the German translation:

![]({{site.baseurl}}/attachments/6389832/8719455.png?effects=drop-shadow)

So it's only natural that a lot of things will not be translated automatically. Luckily, you can fix any text label lacking a translation in any of the installed languages by editing it manually. For example, to add a German translation for the link "View more addons in Marketplace", do the following:

1.  In the Languages section (**Store setup** > **Translations**) of the Admin area, select the **Edit labels** tab.
2.  Search for the label "View more addons in Marketplace":
    ![]({{site.baseurl}}/attachments/6389832/8719456.png?effects=drop-shadow)
    Now that we have found the label, we can see all the languages in which the label does not have a translation - the codes for these languages are greyed out (see the "DE" language code displayed in pale grey):
    ![]({{site.baseurl}}/attachments/6389832/8719457.png?effects=drop-shadow)
3.  Use the Global edit feature to add the translation you require. Be sure to save your changes.
    ![]({{site.baseurl}}/attachments/6389832/8719458.png?effects=drop-shadow)
    (More dtailed instructions for editing text labels and their translations can be found in the {% link "Editing text labels" ref_IyGxQ1DN#editing-text-labels %} section of this manual.)

That is all. After switching the language in your store's Admin area to "DE" you should be able to see the link text translated.

_Related pages:_

*   {% link "Switching the language in Admin area" ref_x5oSN86B %}
