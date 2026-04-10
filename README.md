# MITRE T1526 Azure-Resource-Enumeration 

https://www.linkedin.com/pulse/simulating-mitre-attck-t1526-azure-practical-red-vs-blue-mancuso-yag7c

T1526 - Cloud Service Discovery - Red Team TTP Demo .DESCRIPTION     Enumerates Azure/M365 cloud services and resources within the tenant.     For authorized red team use only.
# 🔍 MITRE ATT&CK T1526 - Azure Resource Enumeration (PowerShell)

# ðŸš€ MITRE ATT&CK T1526 â€“ Azure Resource Enumeration (PowerShell)

## Overview
Cloud attacks rarely start with exploitation â€” they start with **visibility**.

This PowerShell script simulates **MITRE ATT&CK T1526 â€“ Cloud Service Discovery** for Azure and Entra ID environments. 
It provides safe, read-only enumeration for Red, Blue, and Purple team exercises.

---

## MITRE ATT&CK Mapping

| Field | Value |
|------|------|
| Technique | T1526 |
| Name | Cloud Service Discovery |
| Tactic | Discovery |
| Platform | Azure / Entra ID |
| Use Case | Red / Blue / Purple Team |

---

## What the Script Does

This script enumerates:
- Azure subscriptions
- Resource groups
- Azure resources
- Entra ID users
- Groups
- Service principals
- App registrations

---

## Logical Enumeration Flow

![Enumeration Flow](https://raw.githubusercontent.com/MichaelMancuso/MITRE-T1526---Azure-Resource-Enumeration/main/images/azure-t1526-flow.png)

Authenticate to Azure  
â†“  
Retrieve Graph API Token  
â†“  
Enumerate Azure Resources  
â†“  
Enumerate Entra ID Users & Groups  
â†“  
Enumerate Service Principals  
â†“  
Map Tenant Attack Surface  

---

## Red vs Blue Detection Model

![Red vs Blue](https://raw.githubusercontent.com/MichaelMancuso/MITRE-T1526---Azure-Resource-Enumeration/main/images/red-blue-model.png)

RED TEAM â†’ Enumeration  
BLUE TEAM â†’ Detection  

---

## Safety

This script is read-only and does not:
- Modify resources
- Change permissions
- Create identities
- Deploy infrastructure

---

## GitHub Script

https://github.com/MichaelMancuso/MITRE-T1526---Azure-Resource-Enumeration/blob/main/MITRE%20T1526%20-%20Azure%20Resource%20Enumeration.ps1

---

## Author
Michael Mancuso


