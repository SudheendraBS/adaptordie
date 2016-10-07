# Lab 2 - Exposing the API through Apigee Edge

In this lab, you will create an API Proxy inside of Apigee Edge using the Management UI. You can access the Management UI by visiting <a href="https://enterprise.apigee.com" target="_blank">https://enterprise.apigee.com</a>

If you do not have an Apigee account, please go back to the *Getting Started* section of the [project overview page](README.md) and follow the instructions there to get your account set up.

Once you have accessed the Management UI, you should see a Dashboard page that looks similar to this:

![Management Dashboard](management-ui.png)

# Creating the API Proxy

From the Management UI dashboard, select the APIs -> API Proxies option from the main menu at the top of the page. 

![APIs Menu](apis-menu.png)

This will take you to a list of all the *API Proxies* that have been created in your Apigee Edge instance (called an organization in Apigee terminology). 

![API Proxy List](proxies-list.png)

API Proxies are the building blocks for creating APIs in Apigee Edge. Create a new API Proxy now by clicking on the *+ API Proxy* button 

![New API](new-proxy.png)

This will launch the API Proxy creation wizard:

![New API Wizard](proxy-wizard.png)

Select the first option *Reverse proxy (most common)* and click on the *Use OpenAPI* button. This will bring up a dialog box asking you for a URL that points to your OpenAPI specification. 

![New API OpenAPI](proxy-openapi.png)

In the URL field, enter the same URL that you used to import the API specification in API Studio: <a href="http://playground.apistudio.io/0f9aeab1-9b21-4091-9f7b-b46322ae28ce/spec" target="_blank">http://playground.apistudio.io/0f9aeab1-9b21-4091-9f7b-b46322ae28ce/spec</a> Then click the *Apply* button.

You should now see the OpenAPI document URL correctly specified on the screen:

![New API OpenAPI](api-proxy-after-openapi.png)

Click the blue *Next* button at the bottom right to continue.

The next page you will see allows you to customize the name and description of your API as well as the URI pattern that Apigee Edge will use to associate an incoming API call with your new proxy. In this case, any API calls which have a base path starting with `/adventures` will be handled by this proxy. 

![New API Details](proxy-details.png)

You do not need to modify any of these values. Click the blue *Next* button at the bottom right of your screen to continue.

The next screen will allow you to configure the resources in your OpenAPI specification that you would like to expose through your new API Proxy.

![New API Flows](proxy-flows.png)

You do not need to modify any of these values. Click the blue *Next* button at the bottom right of your screen to continue.

The next screen will allow you to configure security on your new API Proxy:

![New API Flows](proxy-security.png)

The default setting is to implement OAuth security for your API, however for the purposes of this lab we are going to change this setting to use the *Pass through (none)* option:

![New API Passthrough](proxy-passthrough.png)

Ensure your settings are exactly as specified in the above image, then click the blue *Next* button at the bottom right of your screen to continue.



