# Evidence: Storage Account Access Risk

## Finding

The VM's Managed Identity has access to a Storage Account.

## Evidence

The assigned identity has permissions that may allow access to storage data.

## Security Concern

Storage Accounts may contain sensitive business data, customer data, logs, reports, backups, or configuration files.

## Risk

If the VM is compromised, the attacker may use the Managed Identity to access or exfiltrate data from the Storage Account.

## Validation Steps

- Review the sensitivity of the Storage Account data.
- Check RBAC permissions assigned to the Managed Identity.
- Confirm whether the identity requires access to the Storage Account.
- Review Storage Account logging.
- Check for unusual access patterns.
- Confirm whether public access is disabled.
- Confirm whether encryption and data protection controls are enabled.

## Analyst Note

Storage risk should be assessed based on data sensitivity, access permissions, exposure, and monitoring coverage.
