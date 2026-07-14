# Evidence: Managed Identity Risk

## Finding

The VM has a Managed Identity assigned.

## Evidence

The Managed Identity is associated with the VM and may have permissions to access other Azure resources.

## Security Concern

Managed Identities are useful because they allow Azure resources to access other services without storing credentials. However, if a VM is compromised, an attacker may attempt to abuse the identity assigned to that VM.

## Risk

If the identity has excessive permissions, an attacker who compromises the VM may be able to access additional cloud resources.

## Validation Steps

- Identify the Managed Identity assigned to the VM.
- Review RBAC role assignments.
- Check which resources the identity can access.
- Confirm whether permissions follow least privilege.
- Remove unnecessary permissions.
- Check whether the identity has access to sensitive resources.
- Review recent identity and access activity.

## Analyst Note

Managed Identity is not a vulnerability by itself. The risk depends on what the identity can access and whether the resource using it can be compromised.
