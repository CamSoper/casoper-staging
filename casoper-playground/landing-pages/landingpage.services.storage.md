---
title: <Azure Service>
description: Use the Azure libraries for Java to interact with <Azure Service>
keywords: Azure, .NET, SDK, API, <Azure Service>
author: camsoper
ms.author: casoper
manager: douge
ms.date: <date>
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: dotnet
ms.service: <service_metadata>

# <Azure Service>

## Overview

<Single paragraph that describes the things you can add to an application by using the libraries associated with this service. Link to concepts content if you need to go into more detail instead of explaining it in place.>

Read and write objects and table data to [Azure Storage](https://docs.microsoft.com/azure/storage/) from your .NET applications. Define and send messages with queues and mount shared filesystems to share data between applications.>

## Import the libraries

### Visual Studio 

In the [Package Manager](https://docs.microsoft.com/dotnet/azure/dotnet-sdk-azure-install?view=azure-dotnet) window, use the following cmdlet:

```powershell
Install-Package WindowsAzure.Storage
``` 

### .NET Core

Execute the following command in your project directory:

```bash
dotnet add package WindowsAzure.Storage
```
## Example usage

<Sample code for a common task. It does have to "work" if put into an IDE, but don't show the boilerplate variable declarations and other bookeeping that's obvious. Focus on readable code that does somethingt useful for the core scenario for the service. Link to concept content as needed sparingly.>

The following code writes a new file to an existing blob storage container using a provided [storage connection string](https://docs.microsoft.com/azure/storage/storage-configure-connection-string).

## Samples
Table that includes all relevant repos in the Azure-Samples group for the service and language. Link to the ACOM samples page at the end filtered for the language.

| | |
|--|--|
| [Get started with Azure Blob Storage in .NET](https://azure.microsoft.com/resources/samples/storage-blob-dotnet-getting-started/) | Create, read, update, restrict access, and delete files and objects in Azure Storage. |
| [Get started with Azure Queue Storage in .NET](https://azure.microsoft.com/resources/samples/storage-queue-dotnet-getting-started/) | Insert, peek, retrieve and delete messages from Azure Storage queues. | 

Explore [more sample .NET code and applications](https://azure.microsoft.com/resources/samples/?platform=dotnet).
