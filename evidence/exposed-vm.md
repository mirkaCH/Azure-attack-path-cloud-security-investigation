# Evidence: Internet-Exposed Virtual Machine

## Finding

The Azure Virtual Machine is exposed to the Internet.

## Evidence

The VM has a public IP address and allows inbound access from external sources.

## Security Concern

Internet-facing resources are more exposed to scanning, brute-force attempts, exploitation attempts, and automated attacks.

## Risk

If the VM is vulnerable or misconfigured, an attacker may attempt to gain unauthorised access.

## Validation Steps

- Confirm whether the VM has a public IP address.
- Review Network Security Group inbound rules.
- Check whether administrative ports such as SSH (22) or RDP (3389) are exposed.
- Confirm whether public access is required for business purposes.
- Check whether the VM is protected by Azure Bastion, VPN, Just-in-Time VM access, or firewall rules.

## Analyst Note

Public exposure is not always wrong. However, public exposure becomes high risk when combined with administrative access, known vulnerabilities, weak identity controls, or access to sensitive data.
