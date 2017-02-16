---
title: Get started with Azure development in .NET | Microsoft Docs
description: Learn how to start working with Azure and .NET.
services: ''
documentationcenter: net
author: camsoper
manager: douge
editor: ''

ms.assetid: d23ec730-3046-485b-bb98-145de49bfe40
ms.service: multiple
ms.workload: na
ms.tgt_pltfrm: multiple
ms.devlang: net
ms.topic: article
ms.date: 02/13/2016
ms.author: casoper

---

# Get started with Azure development in .NET

**\<INTRODUCTION\>**

## Visual Studio

**\<STEPS TO CREATE NEW PROJECT AND CONSUME NUGET PACKAGE\>**

## Other environments

**\<STEPS TO CREATE NEW PROJECT AND CONSUME NUGET PACKAGE\>**

## Authentication

## Set up authentication

Register your application with Azure Active Directory so your app can read and modify resources in Azure. This example uses the [Azure CLI 2.0](https://docs.microsoft.com/en-us/cli/azure/install-az-cli2) , but you
can also [create the service principal via the web portal](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-create-service-principal-portal).

### Create a service principal

Create a service principal to let your application authenticate with without directly using your account. Service principals let you authenticate apps without directly using 
 user accounts and identities. 

2. Log in using the Azure CLI 2.0 with `az login`. 
3. List the subscriptions for your account with `az account list`.
4. Select the subscription for your service principal to access with `az account set --subscription <subscription name>`. 
5. Create the service principal with `az ad sp create-for-rbac -n "AzureMgmtDemo" --role contributor --output json`. Copy the output from this command to a safe place as it has information you'll need to use to authenticate your app with Azure.

### Authenticate with a credential file

In this example we will create a properties file with the service principal information and use that to authenticate our app.

Create an auth.properties in your src/main/resources folder in your Maven project in Eclipse. 
Right-click the **resources** folder and select **New File**, enter auth.propeties in the **File name:** field, then select OK.

Enter the following properties into this file:

```
subscription=########-####-####-####-############
client=########-####-####-####-############
key=XXXXXXXXXXXXXXXX
tenant=########-####-####-####-############
managementURI=https\://management.core.windows.net/
baseURL=https\://management.azure.com/
authURL=https\://login.windows.net/
graphURL=https\://graph.windows.net/
```

Update this property file with the following changes:

- subscription = use the *id* value from `az account list`
- client = use the *appId* value from the output taken from the service principal created in the previous step
- key = use the *password* value from the service principal creation output
- tenant - use the *tenant* value from the service principal creation output

## Create the application

Create a new class in the src/main/java path in Eclipse (Right click the path, select **New** > **Class**). Enter AzureMgmtDemo in the **Name:** field and select the option to create
a main method under **Which method stubs would you like to create?**. Leave the rest of the options as is and select **Finish**. 

Eclipse will open the class file for editing. Enter the following code into the file:

```java
import com.microsoft.azure.management.compute.VirtualMachine;
import com.microsoft.azure.management.Azure;
import com.microsoft.azure.PagedList;
import java.lang.ClassLoader;
import java.io.File;

public class AzureMgmtDemo {

	public static void main(String[] args) {
		
		try {
			
			final String resourceGroup = "MY_RESOURCE_GROUP";
			
            // authenticate the app with Azure using the properties file created earlier
            ClassLoader classLoader = Thread.currentThread().getContextClassLoader();
            File authfile = new File(classLoader.getResource("auth.properties").getFile());
			Azure azure = Azure.authenticate(authfile).withDefaultSubscription();
			
            // get a list of VMs running in the Azure resource group passed on the command line
			PagedList<VirtualMachine> vmlist = azure.virtualMachines().listByGroup(resourceGroup);
			
			for(VirtualMachine vm : vmlist) {
				if (vm != null) {
					// write VM information to system out
					System.out.println("Found virtual machine " + vm.name() 
				        + " with size " + vm.size() + " in resource group " + resourceGroup 
						+ " with state " + vm.provisioningState());
				}
			}
		}			
		catch (Exception e){
			System.err.println("Error listing virtual machines in resource group " 
			    + resourceGroup + " : " + e.getMessage());
		}
	}
}
```

Update the value of the resourceGroup variable to a resource group in your subscription. Save your changes to the source code.

## Run the code 

Run the code by selecting the Run button in Eclipse (  , shortcut Ctrl+F11) or from the **Run** > **Run** menu. The output from the application will display in the **Console** window.

```text
[pool-84-thread-1] INFO com.microsoft.aad.adal4j.AuthenticationAuthority - [Correlation ID: 3c2c9e37-5aec-482d-9a9b-6e5e6dd7db9b] Instance discovery was successful
Found virtual machine myAzureVM with size Standard_DS1_v2 in resource group myazresgroup with state Succeeded
```

## Learn more

See the How-Tos for detailed samples on [managing virtual machines]() , [connecting to a Azure SQL database]() 