---
identifier: ref_vpEKPoyM
updated_at: 2016-05-16 00:00
layout: article_with_sidebar
lang: en
title: 'Setting up Facebook Login for your store'
categories:
  - User manual

---


To add the "Login with Facebook" feature to your X-Cart store site, complete the following steps:

1.  Create and configure a new App on Facebook (See {% link "Creating a Facebook App" ref_vpEKPoyM %}).
2.  Obtain your Facebook App ID and App Secret and enter them on the "Social Login" module settings page in your X-Cart store's Admin area (See {% link "Configuring the Social Login module: Facebook" Setting-up-Facebook-Login-for-your-store_7504575.html %})

# Creating a Facebook App

To create an App for Facebook login:

1.  Go to the [Apps page](https://developers.facebook.com/apps) of the developers section of Facebook and sign in with your Facebook username and password.
2.  Select + **Add a New App**:
    ![]({{site.baseurl}}/attachments/7504575/9439746.png?effects=drop-shadow)
    A popup titled "Add a New App" will be displayed.
    ![]({{site.baseurl}}/attachments/7504575/9439747.png?effects=drop-shadow)
3.  In the popup, select the _Website_ option:
    ![]({{site.baseurl}}/attachments/7504575/9439748.png?effects=drop-shadow)

4.  The popup will be closed, and you will be allowed to either choose an existing app or enter a name for a new app:
    ![]({{site.baseurl}}/attachments/7504575/9439749.png?effects=drop-shadow)

5.  Enter a name for your new app (for the sake of example, we'll use the name "X-Cart 5", but you can use a different name). Click **Create New Facebook App ID**:
    ![]({{site.baseurl}}/attachments/7504575/9439750.png?effects=drop-shadow)

    This opens a popup where you can provide your basic app information. 
    ![]({{site.baseurl}}/attachments/7504575/9439752.png?effects=drop-shadow)

6.  Enter a name for your App into the **Display Name** field (this will be the user-facing name of your App; using your store name is recommended). In the **Contact Email** field, provide a valid email address (will be used for important communication about your app). Select the category "**Apps for Pages**". Click **Create App ID**.
    ![]({{site.baseurl}}/attachments/7504575/9439751.png?effects=drop-shadow)

    This will create the app and start a wizard that will help you to complete your app configuration.
    ![]({{site.baseurl}}/attachments/7504575/9439781.png?effects=drop-shadow)

7.  At the step "Setup SDK", scroll down the page and enter your site  URL:
    ![]({{site.baseurl}}/attachments/7504575/9439783.png?effects=drop-shadow)
8.  Click **Next** to go to the next step.
    ![]({{site.baseurl}}/attachments/7504575/9439784.png?effects=drop-shadow)

9.  Scroll to the page top and use the **My Apps** drop-down menu next to your user icon to select the app you have just created:
    ![]({{site.baseurl}}/attachments/7504575/9439785.png?effects=drop-shadow)
    The app details are opened in the Dashboard:
    ![]({{site.baseurl}}/attachments/7504575/9439786.png?effects=drop-shadow)
10.  As your app is now in **development** mode, to go live with your app, you need to switch the mode to **live**. To do so, click the **App Review** tab and use the switch in the section titled "**Make <your app name> public?**" to make your app available to the general public:
    ![]({{site.baseurl}}/attachments/7504575/9439787.png?effects=drop-shadow)
    Confirm your request:
    ![]({{site.baseurl}}/attachments/7504575/9439788.png?effects=drop-shadow)
    Your app will be published:
    ![]({{site.baseurl}}/attachments/7504575/9439789.png?effects=drop-shadow)
    That is all. Your Facebook App has been configured.

# Configuring the Social Login module: Facebook

Once you have created and configured your Facebook App, you will need to obtain two pieces of information: your Facebook App ID and App Secret. These will need to be entered in X-Cart so the module can connect to the App you created on Facebook and generate the Facebook login widget code correctly.

The Facebook App ID and App Secret can be found on the **Settings** page for your App (You will need to click the **Show** button and enter your password to reveal the App Secret):

![]({{site.baseurl}}/attachments/7504575/9439790.png?effects=drop-shadow)

We recommend opening your X-Cart Admin interface in a separate browser tab or window so you can copy and paste the App ID and App Secret values from Facebook to X-Cart.

To configure the module:

1.  In the Installed Modules section of your X-Cart store’s Admin area, locate the entry for the Social Login module and click the **Settings **link below it:
    ![]({{site.baseurl}}/attachments/7504575/9439791.png?effects=drop-shadow)
    This opens the "Social Login" module settings page:
    ![]({{site.baseurl}}/attachments/7504575/9439792.png?effects=drop-shadow)
2.  On the "Social Login" module settings page, complete the **Facebook App ID/API Key** and **Facebook App Secret** fields with the Facebook App ID and App Secret values you obtained on Facebook. 
3.  Click the **Submit** button near the bottom of the page to save the changes.
    ![]({{site.baseurl}}/attachments/7504575/9439793.png?effects=drop-shadow)
    The "Login with Facebook" feature should now be enabled.

_Related pages:_

*   {% link "Social Login" ref_IapN8lJ8 %}
*   {% link "Setting up Google Login for your store" ref_LMCQeIrv %}

## Attachments:

* [apps.png]({{site.baseurl}}/attachments/7504575/7602302.png) (image/png)
* [create_new_app1.png]({{site.baseurl}}/attachments/7504575/7602303.png) (image/png)
* [step1.jpg]({{site.baseurl}}/attachments/7504575/7602304.jpg) (image/jpeg)
* [create_new_app.png]({{site.baseurl}}/attachments/7504575/7602305.png) (image/png)
* [create_new_app2.png]({{site.baseurl}}/attachments/7504575/7602306.png) (image/png)
* [dashboard.png]({{site.baseurl}}/attachments/7504575/7602307.png) (image/png)
* [settings.png]({{site.baseurl}}/attachments/7504575/7602308.png) (image/png)
* [platform.png]({{site.baseurl}}/attachments/7504575/7602309.png) (image/png)
* [step1-settings.jpg]({{site.baseurl}}/attachments/7504575/7602310.jpg) (image/jpeg)
* [website.png]({{site.baseurl}}/attachments/7504575/7602311.png) (image/png)
* [website1.png]({{site.baseurl}}/attachments/7504575/7602312.png) (image/png)
* [app_secret.png]({{site.baseurl}}/attachments/7504575/7602313.png) (image/png)
* [app_secret1.png]({{site.baseurl}}/attachments/7504575/7602314.png) (image/png)
* [facebook_settings.png]({{site.baseurl}}/attachments/7504575/7602315.png) (image/png)
* [facebook_login_setup.png]({{site.baseurl}}/attachments/7504575/7602316.png) (image/png)
* [sl_modules_list.png]({{site.baseurl}}/attachments/7504575/7602322.png) (image/png)
* [status-and-review-to-yes.png]({{site.baseurl}}/attachments/7504575/8355856.png) (image/png)
* [xc5_sociallogin_new_app.png]({{site.baseurl}}/attachments/7504575/9439746.png) (image/png)
* [xc5_sociallogin_new_app1.png]({{site.baseurl}}/attachments/7504575/9439747.png) (image/png)
* [xc5_sociallogin_new_app2.png]({{site.baseurl}}/attachments/7504575/9439748.png) (image/png)
* [xc5_sociallogin_new_app3.png]({{site.baseurl}}/attachments/7504575/9439749.png) (image/png)
* [xc5_sociallogin_new_app4.png]({{site.baseurl}}/attachments/7504575/9439750.png) (image/png)
* [xc5_sociallogin_new_app6.png]({{site.baseurl}}/attachments/7504575/9439751.png) (image/png)
* [xc5_sociallogin_new_app5.png]({{site.baseurl}}/attachments/7504575/9439752.png) (image/png)
* [xc5_sociallogin_new_app7.png]({{site.baseurl}}/attachments/7504575/9439782.png) (image/png)
* [xc5_sociallogin_new_app7.png]({{site.baseurl}}/attachments/7504575/9439781.png) (image/png)
* [xc5_sociallogin_new_app8.png]({{site.baseurl}}/attachments/7504575/9439783.png) (image/png)
* [xc5_sociallogin_new_app9.png]({{site.baseurl}}/attachments/7504575/9439784.png) (image/png)
* [xc5_sociallogin_new_app10.png]({{site.baseurl}}/attachments/7504575/9439785.png) (image/png)
* [xc5_sociallogin_new_app11.png]({{site.baseurl}}/attachments/7504575/9439786.png) (image/png)
* [xc5_sociallogin_new_app12.png]({{site.baseurl}}/attachments/7504575/9439787.png) (image/png)
* [xc5_sociallogin_new_app13.png]({{site.baseurl}}/attachments/7504575/9439788.png) (image/png)
* [xc5_sociallogin_new_app14.png]({{site.baseurl}}/attachments/7504575/9439789.png) (image/png)
* [xc5_sociallogin_new_app15.png]({{site.baseurl}}/attachments/7504575/9439790.png) (image/png)
* [xc5_sociallogin_module_settings.png]({{site.baseurl}}/attachments/7504575/9439791.png) (image/png)
* [xc5_sociallogin_facebook_settings.png]({{site.baseurl}}/attachments/7504575/9439792.png) (image/png)
* [xc5_sociallogin_facebook_settings_submit.png]({{site.baseurl}}/attachments/7504575/9439793.png) (image/png)