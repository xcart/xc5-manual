---
identifier: ref_o5oJ0AFO
updated_at: 2016-01-14 00:00
layout: article_with_sidebar
lang: en
title: 'Removing the &quot;Powered by&quot; notice'
categories:
  - User manual

---


1.  Make sure the module **Theme Tweaker** is installed and enabled at your store. If not, {% link "install and activate it" ref_0fGEpvrh %}.
    ![]({{site.baseurl}}/attachments/6389847/8716763.png?effects=drop-shadow)
2.  Click **Look & Feel** in the main menu to go to the Layout section and select the** Custom CSS **tab there.
    ![]({{site.baseurl}}/attachments/6389847/8716764.png?effects=drop-shadow)
3.  Enable the **Use custom css** option.

4.  Insert the following CSS code into the field below:

    ```php
    .powered-by .powered-by-label {
        display: none;
    }
    ```

5.  Click **Save**.
    ![]({{site.baseurl}}/attachments/6389847/8716775.png?effects=drop-shadow)

6.  Check the results in the front end.

7.  If you need to remove the "Powered by" notice on the Mobile Mode, just go to **Mobile custom CSS** section, enable **Use mobile custom css** check-box, add the below code to the corresponding field,and click **Save**:

    ```php
    p.powered-by-label {
        display: none;
    }
    ```

    ![]({{site.baseurl}}/attachments/6389847/9437792.png?effects=drop-shadow)

## Attachments:

* [theme-tweaker-module.png]({{site.baseurl}}/attachments/6389847/6586544.png) (image/png)
* [look-and-feel-section.png]({{site.baseurl}}/attachments/6389847/6586545.png) (image/png)
* [custom-css-section.png]({{site.baseurl}}/attachments/6389847/6586546.png) (image/png)
* [custom-css-remove-powered-by.png]({{site.baseurl}}/attachments/6389847/6586547.png) (image/png)
* [xc5_theme_tweaker_module.png]({{site.baseurl}}/attachments/6389847/8716763.png) (image/png)
* [xc5_custom_css.png]({{site.baseurl}}/attachments/6389847/8716764.png) (image/png)
* [xc5_custom_css_save.png]({{site.baseurl}}/attachments/6389847/8716775.png) (image/png)
* [Mobile-custom-css-remove-powered-by.png]({{site.baseurl}}/attachments/6389847/9437792.png) (image/png)