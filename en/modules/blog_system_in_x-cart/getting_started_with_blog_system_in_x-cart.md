---
identifier: ref_iaEvngqO
updated_at: 2015-09-16 00:00
layout: article_with_sidebar
lang: en
title: 'Getting started with Blog System in X-Cart'
categories:
  - User manual

---


This guide assumes that the module Blog System in X-Cart has already been {% link "installed and enabled in your store" ref_fnsXhg2r %}.

To start using Blog System in X-Cart:

1.  Create a new MySQL user and a new MySQL database for WordPress. For security reasons, we recommend these to be separate from the ones used by X-Cart.
2.  In a web browser, open your X-Cart store's home page and click "Blog".  
    ![]({{site.baseurl}}/attachments/7505489/7602727.png?effects=drop-shadow)  

3.  The page that opens will allow you to install and configure WordPress using an installation wizard. The installation wizard includes two steps: at the first step, the latest version of WordPress will be downloaded to the** blog** directory within your X-Cart 5 directory (Make sure your X-Cart 5 directory has write permissions!); at the second step, WordPress will be configured and installed.
4.  Click the button **Start the installation**:  
    ![]({{site.baseurl}}/attachments/7505489/7602728.png?effects=drop-shadow)
5.  Wait for the installation wizard to complete the first step:  
    ![]({{site.baseurl}}/attachments/7505489/7602731.png?effects=drop-shadow)
6.  Once the first step is completed, click on "**click here**" to continue:  
    ![]({{site.baseurl}}/attachments/7505489/7602732.png?effects=drop-shadow)  
    A page will be opened in a new tab allowing you to specify the details of your WordPress MySQL database.
7.  Specify your WordPress MySQL database connection details and click **Submit** to continue:  
    ![]({{site.baseurl}}/attachments/7505489/7602733.png?effects=drop-shadow)  

    WordPress will create a file named **wp-config.php** and will write your MySQL connection details into it. A confirmation message will be displayed as shown below:   
    ![]({{site.baseurl}}/attachments/7505489/7602734.png?effects=drop-shadow)  
    Click **Run the install** to continue.  
    Note: If the **wp-config.php** file could not be created automatically, you should create it manually in your WordPress directory and paste the content from the textarea into it:  
    ![]({{site.baseurl}}/attachments/7505489/7602735.png?effects=drop-shadow)  

8.  On the next page you should enter the title of your blog, as well as the e-mail and password of your WordPress admin user:  
    ![]({{site.baseurl}}/attachments/7505489/7602736.png?effects=drop-shadow)  
    Click **Install WordPress**.
9.  On the Success page, click the **Log In** button to log in to the WordPress admin area.  

    ![]({{site.baseurl}}/attachments/7505489/7602737.png?effects=drop-shadow)  

10.  In the WordPress admin area, click the blog link at the top of the page to visit your blog page and make sure your blog page is displayed correctly:  
    ![]({{site.baseurl}}/attachments/7505489/7602738.png?effects=drop-shadow)  
    For example, if the "Default" skin is used in your X-Cart, the blog should look like this:  
    ![]({{site.baseurl}}/attachments/7505489/7602739.png?effects=drop-shadow)  

11.  Your store's visitors will be able to access your blog using the "Blog" link on your store's Primary menu:  
    ![]({{site.baseurl}}/attachments/7505489/7602727.png?effects=drop-shadow)  

    You will be able to access your WordPress admin area using the "Log in" / "Site Admin" link in the right column of your store's blog page (The link "Site Admin" is displayed when you are already signed in):  
    ![]({{site.baseurl}}/attachments/7505489/7602790.png?effects=drop-shadow)
12.  To adjust the way your blog appears in your X-Cart store, use the settings on the module settings page:  
    ![]({{site.baseurl}}/attachments/7505489/8719388.png?effects=drop-shadow)  

_Related pages:_

*   {% link "Blog System in X-Cart module installation" Blog-System-in-X-Cart-module-installation_7505491.html %}
*   {% link "Configuring the Blog System in X-Cart module" ref_96hR0CtD %}

## Attachments:

![](images/icons/bullet_blue.gif) [image11.png]({{site.baseurl}}/attachments/7505489/7602729.png) (image/png)  
![](images/icons/bullet_blue.gif) [image06.png]({{site.baseurl}}/attachments/7505489/7602730.png) (image/png)  
![](images/icons/bullet_blue.gif) [image11.png]({{site.baseurl}}/attachments/7505489/7602727.png) (image/png)  
![](images/icons/bullet_blue.gif) [image06.png]({{site.baseurl}}/attachments/7505489/7602728.png) (image/png)  
![](images/icons/bullet_blue.gif) [image05.png]({{site.baseurl}}/attachments/7505489/7602731.png) (image/png)  
![](images/icons/bullet_blue.gif) [image10.png]({{site.baseurl}}/attachments/7505489/7602732.png) (image/png)  
![](images/icons/bullet_blue.gif) [image07.png]({{site.baseurl}}/attachments/7505489/7602733.png) (image/png)  
![](images/icons/bullet_blue.gif) [image02.png]({{site.baseurl}}/attachments/7505489/7602734.png) (image/png)  
![](images/icons/bullet_blue.gif) [image04.png]({{site.baseurl}}/attachments/7505489/7602735.png) (image/png)  
![](images/icons/bullet_blue.gif) [image08.png]({{site.baseurl}}/attachments/7505489/7602736.png) (image/png)  
![](images/icons/bullet_blue.gif) [image00.png]({{site.baseurl}}/attachments/7505489/7602737.png) (image/png)  
![](images/icons/bullet_blue.gif) [image01.png]({{site.baseurl}}/attachments/7505489/7602738.png) (image/png)  
![](images/icons/bullet_blue.gif) [image09.png]({{site.baseurl}}/attachments/7505489/7602739.png) (image/png)  
![](images/icons/bullet_blue.gif) [wp_admin_access.png]({{site.baseurl}}/attachments/7505489/7602791.png) (image/png)  
![](images/icons/bullet_blue.gif) [wp_admin_access.png]({{site.baseurl}}/attachments/7505489/7602790.png) (image/png)  
![](images/icons/bullet_blue.gif) [wp_xc_conf_settings.png]({{site.baseurl}}/attachments/7505489/7602792.png) (image/png)  
![](images/icons/bullet_blue.gif) [xc5_blog_system_settings_link.png]({{site.baseurl}}/attachments/7505489/8719388.png) (image/png)