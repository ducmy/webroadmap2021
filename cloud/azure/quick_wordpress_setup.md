# Quick setup wordpress container on Azure

## 1. Login to azure
```bash
az login
```

## 2. Clone

```bash
git clone https://github.com/Azure-Samples/multicontainerwordpress
```

## 3. Setup Resource & App in Azure
```bash
az group create --name myResourceGroup --location "East Asia"
```
```json
{
  "id": "/subscriptions/82680dce-b2f1-4245-a932-9e44b68b15ee/resourceGroups/myResourceGroup",
  "location": "eastasia",
  "managedBy": null,
  "name": "myResourceGroup",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null,
  "type": "Microsoft.Resources/resourceGroups"
}

```
