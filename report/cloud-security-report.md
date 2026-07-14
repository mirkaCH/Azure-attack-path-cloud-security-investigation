# Cloud Security Investigation Report

## Executive Summary

Microsoft Defender for Cloud identified a potential attack path involving a publicly exposed Azure Virtual Machine, a critical vulnerability, an assigned Managed Identity, and access to a Storage Account containing potentially sensitive data.

This creates a high-risk cloud security issue because the attacker may be able to move from initial compromise of the VM to unauthorised access to sensitive storage data.

## Finding

A publicly exposed Azure Virtual Machine with a critical vulnerability has a Managed Identity that can access a Storage Account containing potentially sensitive data.

## Evidence

The identified attack path includes:

- Internet-exposed Azure Virtual Machine
- Critical vulnerability affecting the VM
- Managed Identity assigned to the VM
- Managed Identity permissions to access a Storage Account
- Potential exposure of sensitive business data

## Risk

If an attacker exploits the vulnerable VM, they may be able to use the VM's Managed Identity to access the Storage Account.

This could result in:

- Unauthorised data access
- Data exfiltration
- Lateral movement
- Compliance risk
- Business impact
- Reputational damage

## Priority

**High**

## Recommendation

The organisation should:

- Restrict public exposure of the VM.
- Patch or mitigate the critical vulnerability.
- Review and reduce Managed Identity permissions.
- Apply least privilege access.
- Review Storage Account permissions and data sensitivity.
- Enable logging and monitoring.
- Investigate recent access activity.
- Monitor for suspicious authentication or storage access events.

## Conclusion

This issue should be prioritised because it represents a realistic cloud attack path from an internet-facing vulnerable asset to sensitive data access.

The risk is higher because the exposure, vulnerability, identity permissions, and data access are connected.
