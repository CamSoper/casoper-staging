

# Get started with .NET for Azure developers

This tutorial will walk you through building and deploying an ASP.NET application to Microsoft Azure using Visual Studio.  When finished, you'll have deployed the application to Azure Web Apps with an Azure SQL Database back end.

## Prerequisites

* [Visual Studio 2017](https://www.visualstudio.com/downloads/) with the following [workloads](/visualstudio/install/modify-visual-studio):
    * ASP.NET and web development
    * Azure development
* [SQL Server 2016 Express LocalDB](https://msdn.microsoft.com/en-us/library/hh510202.aspx)

    >[!TIP]
    >This can be installed with Visual Studio 2017 as part of the **.NET desktop development** workload. 
* A [Microsoft Azure subscription](https://azure.microsoft.com/free/)


## Downloading and running the application

First, let's get the sample code for this walkthrough and run it locally.

1. Download the sample code.  You can [get it from GitHub](https://github.com/Azure-Samples/documentdb-dotnet-todo-app), or if you have the [git command line client](https://git-scm.com/), clone it to your local machine with the following command:

    ```cmd
    git clone https://github.com/Azure-Samples/documentdb-dotnet-todo-app
    ```

2. Open **todo.sln** in Visual Studio.

3. Open **Web.config** in the web project.  Look for the following keys in the `<appSettings>` element:

    ```xml
    <add key="endpoint" value="FILLME" />
    <add key="authKey" value="FILLME" />
    ```

    In the **endpoint** key, replace **FILLME** with your DocumentDB URI.  In the **authKey** key, replace **FILLME** with the either the primary or secondary access key for your DocumentDB account.  [Here's where to find your URI and access keys](/azure/documentdb/documentdb-manage-account#a-idkeysaview-copy-and-regenerate-access-keys).

    > [!IMPORTANT]
    > Make sure you're using a key from the **Read-Write** tab, not **Read-Only**.

4. Press **F5** to restore the project's NuGet packages, build the project, and run it locally.

The web application should run locally in your browser.  Note the the data you enter in the application is being stored in your DocumentDB account.  You can [view your data in the Azure portal](https://docs.microsoft.com/en-us/azure/documentdb/documentdb-view-json-document-explorer).

## Deploying the application as an Azure Web App

You've successfully built an application that uses Azure services like DocumentDB.  Next, we'll deploy our web application to the cloud.

> [!IMPORTANT]
> Be sure you're signed into Visual Studio with the same account your Azure subscription is associated with.

1. In Visual Studio Solution Explorer, right-click on the project name and select **Publish...**

2. Using the Publish dialog, select **Microsoft Azure App Service**, select **Create New**, and then click **Publish**

3. Complete the Create App Service dialog as follows:

    * Enter a unique **Web App Name**.  This will be part of the URL for your app.
    * Select the Azure **Subscription** you're deploying to.  We recommend using the same subscription you used for DocumentDB, but it's not required.
    * Select or create a **Resource Group** for your web application. Again, using the same one you used for DocumentDB is recommended.
    * Select or create an **App Service Plan** to determine the pricing your your application.  Here's [more information about App Service Plans](/azure/app-service/azure-web-sites-web-hosting-plans-in-depth-overview).

4. Click **Create** to deploy the application.  When deployment is complete, a browser will open with your deployed application.

## Next steps

* [Use Azure Active Directory for authentication in an ASP.NET web application](/azure/active-directory/develop/active-directory-devquickstarts-webapp-dotnet)
* [Build an Azure Web App using Azure SQL Database](/azure/app-service-web/web-sites-dotnet-get-started)
* [Try a .NET sample application with Azure Storage](/azure/storage/storage-samples-dotnet)


