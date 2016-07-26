---
identifier: ref_LMCQeIrv
updated_at: 2014-03-17 00:00
layout: article_with_sidebar
lang: en
title: 'Setting up Google Login for your store'
categories:
  - User manual

---


To add the Google Login feature to your X-Cart store site, complete the following steps:

1.  Create OAuth2 client ID for your store site (See {% link "Creating OAuth2 client ID" ref_LMCQeIrv %}).
2.  Obtain your Google Client ID and Google Client secret and enter them on the "Social Login" module settings page in your X-Cart store's Admin area (See {% link "Configuring the Social Login module: Google" Setting-up-Google-Login-for-your-store_7504602.html %})

# Creating OAuth2 client ID 

To create OAuth2 client ID for your store:

1.  Go to the [Google Developers Console](https://console.developers.google.com).
2.  Select **Create Project**:
    ![]({{site.baseurl}}/attachments/7504602/7602326.png?effects=drop-shadow)
    A popup titled "New Project" will be displayed:
    ![]({{site.baseurl}}/attachments/7504602/7602327.png?effects=drop-shadow)
3.  In the "New Project" popup, enter a project name and a project ID, or accept the defaults, and select **Create**. The project ID is an identifier that you select when you create the project, and it is used only within the Developers Console. A project ID is unique and cannot be changed, so choose an ID that you'll be comfortable using for the lifetime of the project.
    For example, we chose to create a project "X-Cart 5" and kept the default Project ID:
    ![]({{site.baseurl}}/attachments/7504602/7602328.png?effects=drop-shadow)
    After you have clicked **Create**, Google will create the new project. The screen will reflect this activity:
    ![]({{site.baseurl}}/attachments/7504602/7602329.png?effects=drop-shadow)
    Once the process is completed, you should see a screen with your project ID and project number. The project number is yet another way to identfy your project; it is assigned by the Google Developers Console.
4.  In the sidebar on the left, select **APIs & auth**:
    ![]({{site.baseurl}}/attachments/7504602/7602332.png?effects=drop-shadow)

    Then select **Credentials**:
    ![]({{site.baseurl}}/attachments/7504602/7602334.png?effects=drop-shadow)

5.  On the page that opens, select **Create New Client ID**:
    ![]({{site.baseurl}}/attachments/7504602/7602336.png?effects=drop-shadow)
    This displays a popup titled "Create Client ID":
    ![]({{site.baseurl}}/attachments/7504602/7602337.png?effects=drop-shadow)
6.  In the "Create Client ID" popup:
    1) Select _Web application_ for the **Application type**.
    2) In the **Authorized redirect URI** box, enter the redirect URI for your store site (Simply copy and paste the URI from the Google Login setup instructions on your store's "Social Login" module settings page).
    3) Click **Create Client ID**.
    ![]({{site.baseurl}}/attachments/7504602/7602339.png?effects=drop-shadow)
    The Client ID will be created. 
7.  In the sidebar on the left, select **Consent screen**:
    ![]({{site.baseurl}}/attachments/7504602/7602345.png?effects=drop-shadow)
    Use the settings on this page to configure the consent screen for your project (That is what users will see when they click a Google Login widget on your store site for the first time and are asked to allow your store to access their information on Google). For the **Product name** field, use your store's name so users can easily identify your application.

# Configuring the Social Login module: Google

1.  On the Credentials page of your project in the [Google Developers Console](https://console.developers.google.com/), locate the section** Client ID for web applications** and note or copy the two pieces of information: Client ID and Client secret:
    ![]({{site.baseurl}}/attachments/7504602/7602341.png?effects=drop-shadow)

2.  Open a separate browser tab or window for the X-Cart Admin interface so you can copy and paste the Client ID and Client secret values.
3.  In the Installed Modules section of your X-Cart store’s Admin area (**Extensions** >** Installed modules**), locate the entry for the Social Login module and click the **Settings **link below it:
    ![]({{site.baseurl}}/attachments/7504575/7602322.png?effects=drop-shadow)
    This opens the "Social Login" module settings page:
    ![]({{site.baseurl}}/attachments/7504575/7602315.png?effects=drop-shadow)
4.  Scroll down to the Google section of the page and enter your Client ID and Client secret values:
    ![]({{site.baseurl}}/attachments/7504602/7602344.png?effects=drop-shadow)

5.  Click the **Submit** button near the bottom of the page to save the changes.
    The Google Login feature should now be enabled.

_Related pages:_

*   {% link "Social Login" ref_IapN8lJ8 %}
*   {% link "Setting up Facebook Login for your store" ref_vpEKPoyM %}

## Attachments:

* [google_create_project.png]({{site.baseurl}}/attachments/7504602/7602326.png) (image/png)
* [google_my_project.png]({{site.baseurl}}/attachments/7504602/7602330.png) (image/png)
* [google_xcart5_project.png]({{site.baseurl}}/attachments/7504602/7602331.png) (image/png)
* [google_creating_project1.png]({{site.baseurl}}/attachments/7504602/7602329.png) (image/png)
* [google_my_project.png]({{site.baseurl}}/attachments/7504602/7602327.png) (image/png)
* [google_xcart5_project.png]({{site.baseurl}}/attachments/7504602/7602328.png) (image/png)
* [google_apis_n_auth.png]({{site.baseurl}}/attachments/7504602/7602332.png) (image/png)
* [google_credentials.png]({{site.baseurl}}/attachments/7504602/7602333.png) (image/png)
* [google_credentials0.png]({{site.baseurl}}/attachments/7504602/7602335.png) (image/png)
* [google_credentials0.png]({{site.baseurl}}/attachments/7504602/7602334.png) (image/png)
* [google_new_client_id.png]({{site.baseurl}}/attachments/7504602/7602336.png) (image/png)
* [google_app_type0.png]({{site.baseurl}}/attachments/7504602/7602338.png) (image/png)
* [google_app_type0.png]({{site.baseurl}}/attachments/7504602/7602337.png) (image/png)
* [google_create_client_id_button.png]({{site.baseurl}}/attachments/7504602/7602340.png) (image/png)
* [google_create_client_id_button.png]({{site.baseurl}}/attachments/7504602/7602339.png) (image/png)
* [google_client_id_secret.png]({{site.baseurl}}/attachments/7504602/7602342.png) (image/png)
* [google_client_id_secret.png]({{site.baseurl}}/attachments/7504602/7602343.png) (image/png)
* [google_client_id_secret.png]({{site.baseurl}}/attachments/7504602/7602341.png) (image/png)
* [google_entered_settings.png]({{site.baseurl}}/attachments/7504602/7602344.png) (image/png)
* [google_consent_screen.png]({{site.baseurl}}/attachments/7504602/7602346.png) (image/png)
* [google_consent_screen.png]({{site.baseurl}}/attachments/7504602/7602345.png) (image/png)