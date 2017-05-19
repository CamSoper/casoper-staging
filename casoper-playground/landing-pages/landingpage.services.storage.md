---
title: Install Azure libraries for .NET
description: Import Azure Management Libraries for .NET into your project
keywords: Azure, .NET, SDK, API, NuGet
author: camsoper
ms.author: casoper
manager: douge
ms.date: 05/08/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: dotnet
ms.service: multiple
ms.assetid:
---

# Azure Storage libraries

## Overview

Read and write objects and table data to [Azure Storage](https://docs.microsoft.com/azure/storage/) from your .NET applications. Define and send messages with queues and mount shared filesystems to share data between applications.

## Import the libraries

### Visual Studio 

In the [Package Manager](../dotnet-sdk-azure-install.md) window, use the following cmdlet:

```powershell
Install-Package WindowsAzure.Storage
``` 

### .NET Core

Execute the following command in your project directory:

```bash
dotnet add package WindowsAzure.Storage
```

## Samples

Explore [sample .NET code and applications](https://azure.microsoft.com/resources/samples/?platform=dotnet).
   
<h2 class="accented">Namespaces</h2>
<table class="nameValue">
    <tr id="Microsoft_Azure_Management_Storage" data-moniker=" azure-dotnet azuremgmtstorage-6.2.0-preview ">
        <td colspan="2">
            <span class="lang-csharp"><a class="xref" href="../../microsoft.azure.management.storage?view=azure-dotnet" data-linktype="relative-path">Microsoft.Azure.Management.Storage</a></span>
        </td>
    </tr>
    <tr id="Microsoft_Azure_Management_Storage_Fluent" data-moniker=" azure-dotnet azuremgmtstorage-fluent-1.0.0 ">
        <td colspan="2">
            <span class="lang-csharp"><a class="xref" href="../../microsoft.azure.management.storage.fluent?view=azure-dotnet" data-linktype="relative-path">Microsoft.Azure.Management.Storage.Fluent</a></span>
        </td>
    </tr>
    <tr id="Microsoft_Azure_Management_Storage_Fluent_Models" data-moniker=" azure-dotnet azuremgmtstorage-fluent-1.0.0 ">
        <td colspan="2">
            <span class="lang-csharp"><a class="xref" href="../../microsoft.azure.management.storage.fluent.models?view=azure-dotnet" data-linktype="relative-path">Microsoft.Azure.Management.Storage.Fluent.Models</a></span>
        </td>
    </tr>
    <tr id="Microsoft_Azure_Management_Storage_Fluent_StorageAccount_Definition" data-moniker=" azure-dotnet azuremgmtstorage-fluent-1.0.0 ">
        <td colspan="2">
            <span class="lang-csharp"><a class="xref" href="../../microsoft.azure.management.storage.fluent.storageaccount.definition?view=azure-dotnet" data-linktype="relative-path">Microsoft.Azure.Management.Storage.Fluent.StorageAccount.Definition</a></span>
        </td>
    </tr>
    <tr id="Microsoft_Azure_Management_Storage_Fluent_StorageAccount_Update" data-moniker=" azure-dotnet azuremgmtstorage-fluent-1.0.0 ">
        <td colspan="2">
            <span class="lang-csharp"><a class="xref" href="../../microsoft.azure.management.storage.fluent.storageaccount.update?view=azure-dotnet" data-linktype="relative-path">Microsoft.Azure.Management.Storage.Fluent.StorageAccount.Update</a></span>
        </td>
    </tr>
    <tr id="Microsoft_Azure_Management_Storage_Models" data-moniker=" azure-dotnet azuremgmtstorage-6.2.0-preview ">
        <td colspan="2">
            <span class="lang-csharp"><a class="xref" href="../../microsoft.azure.management.storage.models?view=azure-dotnet" data-linktype="relative-path">Microsoft.Azure.Management.Storage.Models</a></span>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage</a></span>
        </td>
        <td>
        <p>Types common to all Storage services. Classes include CloudStorageAccount, StorageException, OperationContext, and other non-service-specific types.</p>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_Analytics" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.analytics?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.Analytics</a></span>
        </td>
        <td>
        <p>Analytics service client classes.</p>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_Auth" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.auth?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.Auth</a></span>
        </td>
        <td>
        <p>Authentication and credential classes used for encapsulating multiple forms of access.</p>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_Auth_Protocol" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.auth.protocol?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.Auth.Protocol</a></span>
        </td>
        <td>
        <p>Authentication handler classes that support SharedKey and SharedKeyLite for signing requests.</p>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_Blob" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.blob?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.Blob</a></span>
        </td>
        <td>
        <p>Blob service types, stream wrappers, utility classes, and client-side encryption modules.</p>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_Blob_Protocol" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.blob.protocol?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.Blob.Protocol</a></span>
        </td>
        <td>
        <p>Blob service protocol layer types and helpers such as Request Factory and Response Parsers.</p>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_Core" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.core?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.Core</a></span>
        </td>
        <td>
        <p>General helper modules such as UriQueryBuilder, SasQueryBuilder, and special purpose stream wrappers.</p>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_Core_Auth" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.core.auth?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.Core.Auth</a></span>
        </td>
        <td>
        <p>General authentication helper modules such as SharedKey canonicalizers.</p>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_DataMovement" data-moniker=" azure-dotnet azurestoragedatamovement-0.5.0 ">
        <td colspan="2">
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.datamovement?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.DataMovement</a></span>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_File" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.file?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.File</a></span>
        </td>
        <td>
        <p>File service types, stream wrappers, and utility classes.</p>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_File_Protocol" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.file.protocol?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.File.Protocol</a></span>
        </td>
        <td>
        <p>File service protocol layer types and helpers such as FileRequest and Response Parsers.</p>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_Queue" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.queue?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.Queue</a></span>
        </td>
        <td>
        <p>Queue service types, stream wrappers, and utility classes.</p>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_Queue_Protocol" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.queue.protocol?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.Queue.Protocol</a></span>
        </td>
        <td>
        <p>Queue service protocol layer types and helpers such as QueueRequest and Response Parsers.</p>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_RetryPolicies" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.retrypolicies?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.RetryPolicies</a></span>
        </td>
        <td>
        <p>Default RetryPolicy implementations and the IRetryPolicy interface.</p>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_Shared_Protocol" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.shared.protocol?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.Shared.Protocol</a></span>
        </td>
        <td>
        <p>General protocol layer constants and common service-property types.</p>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_Table" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.table?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.Table</a></span>
        </td>
        <td>
        <p>Table service types and utility classes.</p>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_Table_DataServices" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.table.dataservices?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.Table.DataServices</a></span>
        </td>
        <td>
        <p>Legacy Table service implementation based on the WCF Data Services client.</p>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_Table_Protocol" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.table.protocol?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.Table.Protocol</a></span>
        </td>
        <td>
        <p>Table service protocol layer types and helpers such as TableRequest and Response Parsers.</p>
        </td>
    </tr>
    <tr id="Microsoft_WindowsAzure_Storage_Table_Queryable" data-moniker=" azure-dotnet azurestorage-8.1.1 ">
        <td>
            <span class="lang-csharp"><a class="xref" href="../../microsoft.windowsazure.storage.table.queryable?view=azure-dotnet" data-linktype="relative-path">Microsoft.WindowsAzure.Storage.Table.Queryable</a></span>
        </td>
        <td>
        <p>Types supporting the IQueryable interface.</p>
        </td>
    </tr>
</table>