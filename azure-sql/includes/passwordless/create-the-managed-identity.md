---
author: bobtabor-msft
ms.author: rotabor
ms.date: 06/01/2023
ms.service: azure-sql-database
ms.topic: include
ms.custom: generated
---

Create a user-assigned managed identity using the Azure portal or the Azure CLI. Your application uses the identity to authenticate to other services.

# [Azure portal](#tab/azure-portal-create)

1. At the top of the Azure portal, search for *Managed identities*. Select the **Managed Identities** result.
1. Select **+ Create** at the top of the **Managed Identities** overview page.
1. On the **Basics** tab, enter the following values:
    * **Subscription**: Select your desired subscription.
    * **Resource group**: Select your desired resource group.
    * **Region**: Select a region near your location.
    * **Name**: Enter a recognizable name for your identity, such as *MigrationIdentity*.
1. Select **Review + create** at the bottom of the page.
1. When the validation checks finish, select **Create**. Azure creates a new user-assigned identity.

After the resource is created, select **Go to resource** to view the details of the managed identity.

:::image type="content" source="../../database/media/passwordless-connections/create-managed-identity-portal-small.png" lightbox="../../database/media/passwordless-connections/create-managed-identity-portal.png" alt-text="A screenshot showing how to create a managed identity using the Azure portal.":::
    
# [Azure CLI](#tab/azure-cli-create)

Use the [az identity create](/cli/azure/identity#az-identity-create) command to create a user-assigned managed identity:

```azurecli
az identity create --name MigrationIdentity --resource-group <resource-group>
```

---
