# Module 12: Secrets, Keys, Certificates, and Secure Files

## Lesson Notes

Use Azure Key Vault for secrets, keys, and certificates. Apply least privilege, logging, expiry/rotation, and network controls. Prefer secretless managed identity or OIDC. Azure Pipelines secure files store sensitive deployment files; authorize only the required pipeline/job and remove files from agent workspaces. Prevent leakage through source, command arguments, logs, test output, artifacts, and container layers. Masking alone cannot guarantee safety.

## Lab Notes

Create a disposable vault and a harmless lab value:

```bash
az keyvault create --name <unique-vault> --resource-group <rg> --location <region>
az keyvault secret set --vault-name <unique-vault> --name lab-message --value "non-sensitive-value"
az keyvault secret show --vault-name <unique-vault> --name lab-message --query id --output tsv
```

Grant a test workload identity only the required read permission. Retrieve the value in a pipeline without printing it. In Azure Pipelines, upload a harmless dummy secure file, authorize only the lab pipeline, use it in one job, then verify it is not included in published artifacts or retained workspace. Remove lab values/files and revoke temporary permissions.

## Exercises

1. Inventory build, signing, deployment, and runtime secrets/keys/certificates with owner, consumer, scope, rotation, expiry, and audit.
2. Replace one stored credential with federation.
3. Write the response steps for a credential committed to a public repository.

## Verification

- Unauthorized identity cannot read the secret.
- Secret values do not appear in logs or artifacts.
- Secure file authorization and cleanup are understood and documented.
