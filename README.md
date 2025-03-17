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
