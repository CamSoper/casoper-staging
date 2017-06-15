---
title: Azure for .NET developers - Tutorials, API Reference | Microsoft Docs
description: Tools, SDKs, tutorials, and samples to help you create and deploy .NET apps to Azure.
keywords: Azure, .NET, SDK, API, NuGet
author: camsoper
ms.author: casoper
manager: douge
layout: LandingPage
ms.date: 05/08/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: dotnet
ms.service: multiple
---

# Azure for .NET developers

<ul class="panelContent">
    <li> 
        <div class="cardSize">
            <div class="cardPadding">
                <div class="card">
                    <div class="cardText">
                        <a href="dotnet-tools.md">
                            <h2>Tools</h2>
                            <span>Download Azure tools and plugins.</span>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </li>
    <li>
        <div class="cardSize">
            <div class="cardPadding">
                <div class="card">
                    <div class="cardText">
                        <a href="dotnet-sdk-azure-install.md">
                            <h2>Libraries</h2>
                            <span>Use services and manage Azure resources.</span>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </li>
</ul>

## Manage Azure resources

Import the [Azure management libraries for .NET](dotnet-sdk-azure-install.md) to manage your Azure resources with an easy-to-use [fluent API](dotnet-sdk-azure-concepts.md). 

```csharp
var windowsVM = azure.VirtualMachines.Define(windowsVmName)
    .WithRegion(Region.USEast)
    .WithNewResourceGroup(rgName)
    .WithNewPrimaryNetwork("10.0.0.0/28")
    .WithPrimaryPrivateIPAddressDynamic()
    .WithNewPrimaryPublicIPAddress(publicIpDnsLabel)
    .WithPopularWindowsImage(KnownWindowsVirtualMachineImage.WindowsServer2012R2Datacenter)
    .WithAdminUsername(username)
    .WithAdminPassword(password)
    .WithSize(VirtualMachineSizeTypes.StandardD3V2)
    .Create();
 ```

[Get started with the Azure management libraries for .NET](dotnet-sdk-azure-get-started.md)

## Five-minute quickstarts
Create and deploy an app using your favorite tools in five minutes.
<ul>
   <li><a href="dotnet-quickstart-vs.md">Visual Studio</a></li>
   <li><a href="dotnet-quickstart-xplat.md">Command line</a></li>
</ul>

## Tutorials and samples

Complete walkthroughs for app creation and deployment.

<ul>
    <li><a href="/azure/sql-database/sql-database-connect-query-java">SQL Database</a></li>
    <li><a href="/azure/app-service-web/app-service-web-tutorial-java-mysql">MySQL</a></li>
    <li><a href="/azure/documentdb/documentdb-java-application">CosmosDB</a></li>
    <li><a href="/azure/storage/storage-java-how-to-use-blob-storage">Azure Storage</a></li>
</ul>
