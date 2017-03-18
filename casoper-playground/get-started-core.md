

# Get started with .NET Core for Azure developers

This tutorial will walk you through building and deploying a Microsoft Azure application using .NET Core on Windows, Linux, or Mac.  When finished, you'll have a web-based to-do application built in ASP.NET MVC Core, hosted as an Azure Web App, and using Azure DocumentDB for data storage.

## Prerequisites

* [.NET Core](https://www.microsoft.com/net/download/core)
* [Azure CLI 2.0](/cli/azure/install-az-cli2)
* [Git](https://www.git-scm.com/) command line client.
* A [Microsoft Azure subscription](https://azure.microsoft.com/free/)
* A [DocumentDB account](/azure/documentdb/documentdb-create-account) in your Azure subscription

## Downloading and running the application

First, get the sample code for this walkthrough and run it locally.

1. Clone the [sample code](https://github.com/CamSoper/dotnet-core-todo) from GitHub.
    
    ```bash
    git clone https://github.com/CamSoper/dotnet-core-todo
    ```

    Set your working directory to the sample directory.

    ```bash
    cd dotnet-core-todo
    ```

2. Edit **appsettings.json** with your DocumentDB information.  Look for the following properties:

    ```json
    "authKey": "FILLME",
    "endpoint": "FILLME",
    ```

    In the **authKey** property, replace **FILLME** with the either the primary or secondary access key for your DocumentDB account.  In the **endpoint** property, replace **FILLME** with your DocumentDB URI.  [Here's where to find your URI and access keys](/azure/documentdb/documentdb-manage-account#a-idkeysaview-copy-and-regenerate-access-keys).

    > [!IMPORTANT]
    > Make sure you're using a key from the **Read-Write** tab, not **Read-Only**.

3. Commit your changes to the local Git repository.

    ```bash
    git commit -a -m "Modified settings"
    ```

4. Restore the NuGet packages and run the application.

    ```bash
    dotnet restore
    dotnet run
    ```

The web application will be hosted in a local web server.  Follow the instructions on-screen to connect to it with your browser.  Note the the data you enter in the application is being stored in your DocumentDB account.  You can [view your data in the Azure portal](https://docs.microsoft.com/en-us/azure/documentdb/documentdb-view-json-document-explorer).

## Configure Azure App Service and deploy the web app

> [!IMPORTANT]
> This sample works in a Bash shell. For options on running Azure CLI scripts on Windows client, see [Using the Azure CLI on Windows](/azure/virtual-machines/virtual-machines-windows-cli-options).

1. Log in to Azure CLI 2.0 if you haven't already.

    ```bash
    az login
    ```

2. Start by generating a unique name for the web app.

    ```bash
    let randomNum=$RANDOM*$RANDOM
    webappname=todoApp$randomNum
    ```

3. Create a resource group.
    
    ```bash
    az group create --location westus2 --name myResourceGroup
    ```
    
4. Create an App Service plan.
    
    ```bash 
    az appservice plan create --name $webappname --resource-group myResourceGroup --sku FREE
    ```

5. Create the Web App.

    ```bash
    az appservice web create --name $webappname --resource-group myResourceGroup --plan $webappname
    ```

6. Set the account-level deployment credentials. 

    ```bash
    az appservice web deployment user set --user-name <desired user name> --password <desired password>
    ```

7. Configure the web app for deployment from local Git and get the repository URL.

    ```bash
    url=$(az appservice web source-control config-local-git --name $webappname --resource-group myResourceGroup --query url --output tsv)
    ```
8. Add the Azure remote to your local Git repository and push your code.  When prompted for password, use password that you specified earlier.
    
    ```bash
    git remote add azure $url
    git push azure master
    ```

9. Browse to the deployed web app.
    
    ```
    az appservice web browse --name $webappname --resource-group myResourceGroup
    ```

    Alternatively, you can manually use your browser to open `https://<web app name>.azurewebsites.net`.

## Next steps

* [Use Azure Active Directory for authentication in an ASP.NET web application](/azure/active-directory/develop/active-directory-devquickstarts-webapp-dotnet)
* [Build an Azure Web App using Azure SQL Database](/azure/app-service-web/web-sites-dotnet-get-started)
* [Try a .NET sample application with Azure Storage](/azure/storage/storage-samples-dotnet)


