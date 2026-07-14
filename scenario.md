# Scenario

During a cloud security review, Microsoft Defender for Cloud identified a potential attack path involving an Azure Virtual Machine.

The VM is exposed to the Internet and has a critical vulnerability. The VM also has a Managed Identity assigned to it, which has access to a Storage Account containing sensitive business data.

## Attack Path

**Internet-exposed VM → Critical vulnerability → Managed Identity → Storage Account → Sensitive data exposure**

## Initial Concern

If an attacker exploits the vulnerable VM, they may be able to use the VM's Managed Identity to access cloud resources without needing separate credentials.

This could allow unauthorised access to sensitive data stored in the Storage Account.

## Investigation Goal

The goal of this investigation is to determine:

- What resource is exposed
- What vulnerability exists
- What permissions the Managed Identity has
- What data could be accessed
- What business risk exists
- What remediation actions should be recommended

## Example Environment

| Resource | Example |
|---|---|
| Cloud platform | Microsoft Azure |
| Security tool | Microsoft Defender for Cloud |
| Asset type | Virtual Machine |
| Exposure | Public Internet |
| Identity | Managed Identity |
| Data target | Storage Account |
| Risk type | Attack path to sensitive data |

## Assumptions

This is a simulated lab scenario created for learning and portfolio purposes. No real customer data, live cloud environment, or production asset was used.
