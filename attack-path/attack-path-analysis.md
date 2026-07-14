# Attack Path Analysis

![Attack Path Overview](../assets/azure-attack-path-overview.png)

## Attack Path Summary

The identified attack path is:

1. The Azure Virtual Machine is exposed to the Internet.
2. The VM contains a critical vulnerability.
3. The VM has a Managed Identity assigned.
4. The Managed Identity has access to a Storage Account.
5. The Storage Account may contain sensitive business data.

## Why This Matters

This is a high-risk attack path because it combines multiple security weaknesses:

- External exposure
- Exploitable vulnerability
- Cloud identity permissions
- Access to sensitive data

Individually, each issue may represent a security risk. Combined together, they create a realistic path for an attacker to move from initial access to data exposure.

## Possible Attacker Flow

An attacker could:

1. Discover the public VM through scanning or exposed cloud assets.
2. Exploit the critical vulnerability.
3. Gain access to the VM.
4. Request or abuse the VM's Managed Identity token.
5. Access the Storage Account using the identity permissions.
6. Read or exfiltrate sensitive data.

## Risk Level

**High**

## Reason

The attack path involves an internet-facing asset, a critical vulnerability, cloud identity permissions, and access to sensitive data.

## Security Principle

Cloud security risk should be assessed by looking at how issues connect together, not only by reviewing each finding in isolation.
