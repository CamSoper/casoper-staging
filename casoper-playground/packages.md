---
title: .NET for Azure developers | Microsoft Docs
description: A full catalog of NuGet packages for Azure SDK for .NET
services: ''
documentationcenter: net
author: camsoper
manager: douge
editor: ''

ms.assetid: 4b8f8fe6-1b26-4bb4-9be9-6ae757a59e66
ms.service: multiple
ms.workload: na
ms.tgt_pltfrm: multiple
ms.devlang: net
ms.topic: article
ms.date: 12/22/2016
ms.author: casoper

---
# Azure NuGet Packages

Use the libraries in the .NET SDK for Azure to manage and consume Azure services in your applications.  

## Installation

### Visual Studio

If you're using Visual Studio, use the **NuGet Package Manager Console** to import the package into your project.

1. With your Visual Studio solution open, launch the console by clicking **Tools**, followed by **NuGet Packager Manager**, and then click **Package Manager Console**.  

    ![Package Manager Console](./media/packages/package-manager.png)

2. In the console window, use the **Install-Package** cmdlet to download and install the NuGet package.  For example, to include the latest version of the [Azure Resource Management Library](http://www.nuget.org/packages/Microsoft.Azure.Management.Resources) for .NET:

    ```powershell
    Install-Package Microsoft.Azure.Management.Resources -Pre 
    ``` 
    To use a specific version, include the version number like this:

    ```powershell
    Install-Package Microsoft.Azure.Management.Resources -Version 2.20.1-preview
    ``` 

### .NET Core

If you're using .NET Core with Visual Studio Code (or any other editor), edit your project.json file to add the package to the project dependencies.  This example uses a specific version of **Microsoft.Azure.Management.Resources**, but you can use [wildcards and comparison operators](https://docs.microsoft.com/dotnet/articles/core/tools/project-json#dependencies).

```json
{
  "version": "1.0.0-*",
  "buildOptions": {
    "debugType": "portable",
    "emitEntryPoint": true
  },
    "frameworks": {
        "netcoreapp1.1": {
            "dependencies": {
                "Microsoft.NETCore.App": {
                    "type": "platform",
                    "version": "1.1.0"
                }
            },
            "imports": "dnxcore50"
        }
    },
    "dependencies": {
        "Microsoft.Azure.Management.Resources": "2.20.1-preview"
    }
}
```

> [!WARNING]
> Be sure you're editing the top-level **dependencies** object, and not the framework dependencies.

## Packages

**Data** packages are used to **consume** Azure services in your .NET applications.  **Management** packages are used to **manage** resources in Azure.

Service | Data package | Management package
--------|--------------|-------------------
[Azure Resource Manager](https://docs.microsoft.com/azure/azure-resource-manager/) | | [Microsoft.Azure.Management.ResourceManager](https://www.nuget.org/packages/Microsoft.Azure.Management.ResourceManager)<br/>[Microsoft.Azure.Management.Fluent](https://www.nuget.org/packages/Microsoft.Azure.Management.Fluent)
[Azure Active Directory](https://docs.microsoft.com/azure/active-directory) | [Microsoft.IdentityModel.Clients.ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory) |
[Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/) | | [Microsoft.Azure.Management.Compute](https://www.nuget.org/packages/Microsoft.Azure.Management.Compute)
[Web Apps](https://docs.microsoft.com/azure/app-service-web) | | [Microsoft.Azure.Management.Websites](https://www.nuget.org/packages/Microsoft.Azure.Management.Websites)
[Storage](https://docs.microsoft.com/azure/storage/) | [WindowsAzure.Storage](http://www.nuget.org/packages/WindowsAzure.Storage) | [Microsoft.Azure.Management.Storage](https://www.nuget.org/packages/Microsoft.Azure.Management.Storage)
[HD Insight](https://docs.microsoft.com/azure/hdinsight/) | [Microsoft.Azure.Management.HDInsight.Job](http://www.nuget.org/packages/Microsoft.Azure.Management.HDInsight.Job) | [Microsoft.Azure.Management.HDInsight](https://www.nuget.org/packages/Microsoft.Azure.Management.HDInsight)
[Service Bus](https://docs.microsoft.com/azure/service-bus/) | [WindowsAzure.ServiceBus](https://www.nuget.org/packages/WindowsAzure.ServiceBus/) |
[Key Vault](https://docs.microsoft.com/azure/key-vault/) | [Microsoft.Azure.KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) | [Microsoft.Azure.Management.KeyVault](https://www.nuget.org/packages/Microsoft.Azure.Management.KeyVault)
[Batch](https://docs.microsoft.com/azure/batch/) | [Azure.Batch](https://www.nuget.org/packages/Azure.Batch) | [Microsoft.Azure.Management.Batch](https://www.nuget.org/packages/Microsoft.Azure.Management.Batch)
[Search](https://docs.microsoft.com/azure/search/) | [Microsoft.Azure.Search](https://www.nuget.org/packages/Microsoft.Azure.Search)
[Event Hubs](https://docs.microsoft.com/azure/event-hubs/) | [Microsoft.Azure.EventHub](https://www.nuget.org/packages/Microsoft.Azure.EventHub)
[Notification Hubs](https://docs.microsoft.com/azure/active-directory/) | [Microsoft.Azure.NotificationHubs](https://www.nuget.org/packages/Microsoft.Azure.NotificationHubs)<br/>[WindowsAzure.Messaging.Managed](https://www.nuget.org/packages/WindowsAzure.Messaging.Managed) | [Microsoft.Azure.Management.NotificationHubs](https://www.nuget.org/packages/Microsoft.Azure.Management.NotificationHubs)
[Data Lake Store](https://docs.microsoft.com/azure/data-lake-store/) | [Microsoft.Azure.Management.DataLake.Store](http://www.nuget.org/packages/Microsoft.Azure.Management.DataLake.Store) | [Microsoft.Azure.Management.DataLake.Store](https://www.nuget.org/packages/Microsoft.Azure.Management.DataLake.Store)
[Data Lake Analytics](https://docs.microsoft.com/azure/data-lake-analytics/) | [Microsoft.Azure.Management.DataLake.Analytics](http://www.nuget.org/packages/Microsoft.Azure.Management.DataLake.Analytics) | [Microsoft.Azure.Management.DataLake.Analytics](https://www.nuget.org/packages/Microsoft.Azure.Management.DataLake.Analytics)
[Service Bus Relay](https://docs.microsoft.com/azure/service-bus-relay/) | [Microsoft.Azure.Relay](https://www.nuget.org/packages/Microsoft.Azure.Relay)
[DocumentDB](https://docs.microsoft.com/azure/documentdb/) | [Microsoft.Azure.DocumentDB.Core](https://www.nuget.org/packages/Microsoft.Azure.DocumentDB.Core) | 
[IoT Hub](https://www.nuget.org/packages/Microsoft.Azure.DocumentDB.Core/) | [Microsoft.Azure.Devices](https://www.nuget.org/packages/Microsoft.Azure.Devices)<br/>[Microsoft.Azure.Devices.Client](https://www.nuget.org/packages/Microsoft.Azure.Devices.Client)
[DevTest Labs](https://docs.microsoft.com/azure/devtest-lab/) | | [Microsoft.Azure.Management.DevTestLabs](https://www.nuget.org/packages/Microsoft.Azure.Management.DevTestLabs)
[Redis Cache](https://docs.microsoft.com/azure/redis-cache/) | [StackExchange.Redis](https://www.nuget.org/packages/StackExchange.Redis/) | [Microsoft.Azure.Management.Redis](https://www.nuget.org/packages/Microsoft.Azure.Management.Redis)
[Media Services](https://docs.microsoft.com/azure/media-services/) | [windowsazure.mediaservices.extensions](https://www.nuget.org/packages/windowsazure.mediaservices.extensions) | [Microsoft.Azure.Management.Media](https://www.nuget.org/packages/Microsoft.Azure.Management.Media)
[Service Fabric](https://docs.microsoft.com/azure/service-fabric/) | [Microsoft.ServiceFabric](https://www.nuget.org/packages/Microsoft.ServiceFabric) | 
[Traffic Manager](https://docs.microsoft.com/azure/traffic-manager/) | | [Microsoft.Azure.Management.TrafficManager](https://www.nuget.org/packages/Microsoft.Azure.Management.TrafficManager)
[Cognitive Services](https://docs.microsoft.com/azure/cognitive-services/) | | [Microsoft.Azure.Management.CognitiveServices](https://www.nuget.org/packages/Microsoft.Azure.Management.CognitiveServices)
[DevTest Labs](https://docs.microsoft.com/azure/devtest-lab/) | | [Microsoft.Azure.Management.DevTestLabs](https://www.nuget.org/packages/Microsoft.Azure.Management.DevTestLabs)
[PowerBI Embedded](https://docs.microsoft.com/azure/power-bi-embedded/) | | [Microsoft.Azure.Management.PowerBIEmbedded](https://www.nuget.org/packages/Microsoft.Azure.Management.PowerBIEmbedded)
[Azure DNS](https://docs.microsoft.com/azure/dns/) | | [Microsoft.Azure.Management.Dns](https://www.nuget.org/packages/Microsoft.Azure.Management.Dns)
[Scheduler](https://docs.microsoft.com/azure/scheduler/) | | [Microsoft.Azure.Management.Scheduler](https://www.nuget.org/packages/Microsoft.Azure.Management.Scheduler)
[CDN](https://docs.microsoft.com/azure/cdn/) | | [Microsoft.Azure.Management.Cdn](https://www.nuget.org/packages/Microsoft.Azure.Management.Cdn)
[Logic Apps](https://docs.microsoft.com/azure/logic-apps/) | | [Microsoft.Azure.Management.Logic](https://www.nuget.org/packages/Microsoft.Azure.Management.Cdn)
[Virtual Network](https://docs.microsoft.com/azure/virtual-network/) | | [Microsoft.Azure.Management.Network](https://www.nuget.org/packages/Microsoft.Azure.Management.Network)
[Automation](https://docs.microsoft.com/azure/automation/) | | [Microsoft.Azure.Management.Automation](https://www.nuget.org/packages/Microsoft.Azure.Management.Automation)    
[Stream Analytics](https://docs.microsoft.com/azure/stream-analytics/) | | [Microsoft.Azure.Management.StreamAnalytics](https://www.nuget.org/packages/Microsoft.Azure.Management.StreamAnalytics)
[Data Factory](https://docs.microsoft.com/azure/data-factory/) | | [Microsoft.Azure.Management.DataFactories](https://www.nuget.org/packages/Microsoft.Azure.Management.DataFactories)