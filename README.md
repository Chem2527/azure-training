# Azure-training

## 1.	Assigning roles at different scopes and Interpreting access assignments.

### Azure RBAC (Role-Based Access Control) allows you to assign roles at different scopes: 
```bash
•	Subscription Level (applies to everything inside the subscription)
•	Resource Group Level (applies to all resources in a specific resource group)
•	Resource Level (applies to a single resource)
```
## 2. Implement and manage azure Policy

Policy for creation of resources only in specified regions

```bash
{
  "properties": {
    "displayName": "Allowed Regions",
    "description": "This policy allows only specified regions for resources.",
    "policyRule": {
      "if": {
        "field": "location",
        "notIn": ["eastus"]
      },
      "then": {
        "effect": "deny"
      }
    }
  }
}
```
## 3. Configure resource locks
```bash
Create a lock for resource group then try to lock any resource or resource group.
```

## 4. Apply and manage tags on resources


```bash
{
  "properties": {
    "displayName": "Require Tags on Resources",
    "description": "This policy ensures that all resources are created with tags.",
    "policyRule": {
      "if": {
        "field": "tags",
        "exists": "false"
      },
      "then": {
        "effect": "deny"
      }
    }
  }
}
```
## 5. Manage resource groups

```bash
Create a rg and create few resources inside this and manage the rg by implementing locks, tags to rg,Migrating resources from one RG to other.
```

## 6. Manage costs by using alerts, budgets, and Azure Advisor recommendations
```bash
Have a walkthrough on cost explorer, how to set alerts, how to create budget alerts?
```

## 7. 	Configure management groups
```bash
Understand what a management group means and what it its hierarchy level.
```
## 8. Configure access to storage
```bash
Create a azure storage account & play withit.  
```
**Link for doownloading & installing azure cli**
```bash
( https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-windows?pivots=msi#install-or-update )
```

## 9. 	Configure Azure Storage firewalls and virtual networks

Use  Azure Storage firewalls and virtual networks in config of storage account and check whether from outside of vnet are we able to access the blobs,files,tables…  or not &  also check whether we can access within vnet or not.

![image](https://github.com/user-attachments/assets/682acb7f-4f0c-4a5d-9256-eee9fbf31704)
```bash
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash ## (It downloads and runs a script that installs the Azure Command-Line Interface (CLI) for Debian-based Linux distributions)
```
```bash
az storage container list --account-name <account name> --account-key <access key> ## (It retrieves and lists all the storage containers in the specified Azure Storage account by authenticating using the provided account name and access key)
```
```bash
az storage container create --name <name of container tht we wanna create> --account-name <storage acc. name> --account-key <access key>
```
```bash
az storage container list --account-name <account name> --account-key <access key>
```

## 10. Create and use shared access signature (SAS) tokens

**Create storage account and generate SAS and access the blobs using SAS in the below format**

```bash
https://<storage-account-name>.blob.core.windows.net/<container-name>/<blob-name>?<SAS-token>
```
## 11. Configure stored access policies

**Create storage account and create stored access policies  and generate SAS using stored access policies and access the blobs**

 **Access the blobs using below format**
 ```bash
https://<storage-account-name>.blob.core.windows.net/<container-name>/<blob-name>?<SAS-token>
```
## 12.	Manage access keys

**Rotate keys for every 3 months or 1 year for security purpose and after rotation check whether we are able to view or access the same.**

```bash
az storage blob list --account-name <storage account name> --container-name <container name> --account-key <access key>
```

