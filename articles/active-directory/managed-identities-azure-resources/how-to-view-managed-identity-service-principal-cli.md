---
title: How to view the service principal of a managed identity using Azure CLI
description: Step-by-step instructions for viewing the service principal of a managed identity using Azure CLI.
services: active-directory
documentationcenter: ''
author: daveba
manager: mtillman
editor: ''

ms.service: active-directory
ms.component: msi
ms.devlang: na
ms.topic: conceptual
ms.tgt_pltfrm: na
ms.workload: identity
ms.date: 11/29/2018
ms.author: daveba
---

# View the service principal of a managed identity using Azure CLI

Managed identities for Azure resources provides Azure services with an automatically managed identity in Azure Active Directory. You can use this identity to authenticate to any service that supports Azure AD authentication without having credentials in your code. 

In this article, you learn how to view the service principal of a managed identity using Azure CLI.

## Prerequisites

- If you're unfamiliar with managed identities for Azure resources, check out the [overview section](overview.md).
- If you don't already have an Azure account, [sign up for a free account](https://azure.microsoft.com/free/).
- Enable [system assigned identity on a virtual machine](/azure/active-directory/managed-identities-azure-resources/qs-configure-portal-windows-vm#system-assigned-managed-identity) or [application](/azure/app-service/app-service-managed-service-identity#adding-a-system-assigned-identity).
- To run the CLI script examples, you have three options:
    - Use [Azure Cloud Shell](../../cloud-shell/overview.md) from the Azure portal (see next section).
    - Use the embedded Azure Cloud Shell via the "Try It" button, located in the top right corner of each code block.
    - [Install the latest version of the Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli) if you prefer to use a local CLI console and sign in to Azure using `az login`
 
[!INCLUDE [cloud-shell-try-it.md](../../../includes/cloud-shell-try-it.md)]

## View the service principal

This following command demonstrates how to view the service principal of a VM or application with managed identity enabled. Replace `<VM or application name>` with your own values. 

```azurecli-interactive
az ad sp list --display-name <VM or application name>
```

## Next steps

For more information on managing Azure AD service principals using Azure CLI, see [az ad sp](/cli/azure/ad/sp).


