---
identifier: ref_IyGxQ1DN
updated_at: 2015-09-17 00:00
layout: article_with_sidebar
lang: en
title: 'Managing texts labels in your store'
categories:
  - User manual

---

Different people may prefer different words for the same meaning. For example, that part of an online store where a user stores the items they picked before paying for them - is it a "shopping cart", a "shopping basket" or a "shopping bag"? In X-Cart, we prefer to call it a "shopping cart", but we understand that some people will want to use a different name. So we made it possible to change almost any word or phrase in your X-Cart store's user interface.

Just a few words on how it works. In X-Cart 5 text pieces like names of sections of the user interface, various notes, comments and error messages are all stored as text labels. A text label has a name by which it can be referenced from the template or program code and one or more "translations". A translation is a value of the label defined for a specific language. When a text piece needs to be displayed on a page, X-Cart selects the respective text label from the database and determines which of its translations needs to be displayed - according to the language that is currently selected for viewing the page. If, for some reason, the value of the label for the selected language is missing, the label value for the default language is displayed. If the label value for the default language is missing as well, the label name is displayed.

So, when you need to edit an existing text piece from your store's user interface, you need to identify the text label that stores this text piece as a value, and then edit this value. If your store uses multiple languages, you may also need to check if a similar change needs to be made for the values of this label in the other languages. For more info on how to edit a label value, see [Editing text labels](#editing-text-labels).

Also, if you need your store to display some text piece for which currenty no text label exists, you can add a new text label for this text piece directly from your store's Admin area. For more info, see [Adding new text labels](#adding-new-text-labels).

## Editing text labels

Let us show how to edit text labels in X-Cart. For example, we want to change the wording of the phrase "Your shopping cart" shown in the snapshot below so it says "Your shopping bag":

![]({{site.baseurl}}/attachments/6389836/7602756.png?effects=drop-shadow)

Let's do it:

1.  In your store's Admin area, go to the **Translations** section (**Store setup > Translations**):
    ![]({{site.baseurl}}/attachments/6389836/8716739.png?effects=drop-shadow)
2.  Switch to the **Edit labels** tab:
    ![]({{site.baseurl}}/attachments/6389836/8716740.png?effects=drop-shadow)
3.  If your store uses more than one language, select the language for which the text label needs to be edited. In our example, we will edit the phrase "Your shopping cart" for the English language. On the following snapshot, the English language is already selected:
    ![]({{site.baseurl}}/attachments/6389836/8716741.png?effects=drop-shadow)
    **Note**: If you need to edit the same phrase in more than one languages, just select any one of them.

    Use search to find the phrase you want to edit. Note that this search is case-sensitive. We need to find the phrase "Your shopping cart", so we simply paste it into the search box and click **Search**:
    ![]({{site.baseurl}}/attachments/6389836/8716742.png?effects=drop-shadow)
    The list of search results (if any) will be provided below:
    ![]({{site.baseurl}}/attachments/6389836/8716743.png?effects=drop-shadow)
    If you get no search results, it means that either you are searching in a wrong language or the label does not exist. If necessary, you can add the missing label by following the instructions in the [Adding new text labels](#adding-new-text-labels) section.

4.  Review the search results to find the phrase you need to edit. If none of the phrases in the results list exactly match the phrase you searched for, do not worry: the items in the list of search results are text labels, and what you see in the list are their names. Their values are concealed from view and have yet to be revealed. To view the value of any text label, hover your cursor over the respective entry in the list of search results; an _Edit_ link will be revealed:
    ![]({{site.baseurl}}/attachments/6389836/8716744.png?effects=drop-shadow)
    Click on the Edit link; this will expand a section where you will be able to view/edit the value of the selected text label:
    ![]({{site.baseurl}}/attachments/6389836/8716745.png?effects=drop-shadow)
5.  Edit the text label value as you require. In our example, we will need to edit the last two labels in the search results list (the first one is used for the case when the cart contains a single item, the second one - when the cart contains multiple items). So we replace the word "cart" with the word "bag" in both the text label values:
    ![]({{site.baseurl}}/attachments/6389836/8716746.png?effects=drop-shadow)
    Note that if you need to edit the same phrase in more than one languages, you can use a special section that will help you to edit all the translations of the phrase simultaneously. To access this section, click on the Global edit icon:
    ![]({{site.baseurl}}/attachments/6389836/8716747.png?effects=drop-shadow)
    The section where you can edit text labels for multiple languages looks as follows:
    ![]({{site.baseurl}}/attachments/6389836/8716748.png?effects=drop-shadow)

6.  After making the changes you require, click **Save changes**.
    The text labels will be updated. 

Now you can check the results in the store's front end. In our case, we should be able to see the phrase "Your shopping bag" instead of "Your shopping cart":

![]({{site.baseurl}}/attachments/6389836/7602764.png?effects=drop-shadow)

## Adding new text labels

To add a new text label:

1.  In your store's Admin area, go to the **Translations** section (**Store setup > Translations**).
2.  Switch to the **Edit labels** tab.
3.  Click the **Add new label** button:
    ![]({{site.baseurl}}/attachments/6389836/8719095.png?effects=drop-shadow)
     A window titled **Create label** pops up:
    ![]({{site.baseurl}}/attachments/6389836/8719096.png?effects=drop-shadow)
4.  Use the form in the **Create label** popup window to enter the new label information (a label name and any translations of the label you require).

5.  Click the **Save changes** button. The new label will be created.
