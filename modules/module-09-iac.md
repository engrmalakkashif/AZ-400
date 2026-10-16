# Module 09: IaC and Environment Configuration

## Lesson Notes

IaC is versioned, reviewed, validated, and deployed through automation. Run lint/policy checks and plan/what-if on PRs, gate apply, protect state/credentials, and detect drift. ARM/Bicep provision Azure resources. Azure Automation State Configuration and Azure Machine Configuration enforce desired state. Configuration-management tools configure software/hosts. Azure Deployment Environments provides governed self-service environments from catalogs/templates with policy, quota, and cleanup.

## Lab Notes

Create `main.bicep` for a disposable Storage account:

```bicep
param storageAccountName string
param location string = resourceGroup().location

resource storage 'Microsoft.Storage/storageAccounts@2023-05-01' = {
  name: storageAccountName
  location: location
  sku: { name: 'Standard_LRS' }
  kind: 'StorageV2'
  properties: {
    supportsHttpsTrafficOnly: true
    minimumTlsVersion: 'TLS1_2'
  }
}
```

With an approved disposable subscription/resource group, build, validate, inspect, deploy, and clean up:

```bash
az bicep build --file main.bicep
az deployment group validate --resource-group <rg> --template-file main.bicep --parameters storageAccountName=<unique-name>
az deployment group what-if --resource-group <rg> --template-file main.bicep --parameters storageAccountName=<unique-name>
az deployment group create --resource-group <rg> --template-file main.bicep --parameters storageAccountName=<unique-name>
az group delete --name <rg> --yes --no-wait
```

Design an Azure Deployment Environments catalog with project/environment types, access, quotas, policy, expiry, cost owner, and cleanup. Compare provisioning an Azure resource with configuring software inside a VM.

## Exercises

1. Design PR validation, approval, apply, drift detection, and rollback for IaC.
2. Compare Bicep/ARM, Azure Machine Configuration, Automation State Configuration, and a configuration-management tool for distinct use cases.
3. Define dev/test/prod parameters and secrets/state handling.

## Verification

- What-if matches intended changes before apply.
- Credentials/state are protected and lab resources are deleted.
- Self-service environments have governance, ownership, and expiry.
