# MITRE T1526 Azure-Resource-Enumeration 

https://www.linkedin.com/pulse/simulating-mitre-attck-t1526-azure-practical-red-vs-blue-mancuso-yag7c

T1526 - Cloud Service Discovery - Red Team TTP Demo .DESCRIPTION     Enumerates Azure/M365 cloud services and resources within the tenant.     For authorized red team use only.
# 🔍 MITRE ATT&CK T1526 - Azure Resource Enumeration (PowerShell)

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
Retrieve Graph API Token  
Enumerate Azure Resources  
Enumerate Entra ID Users & Groups  
Enumerate Service Principals  
Map Tenant Attack Surface  

---

## Red vs Blue Detection Model

![Red vs Blue](https://raw.githubusercontent.com/MichaelMancuso/MITRE-T1526---Azure-Resource-Enumeration/main/images/red-blue-model.png)

RED TEAM - Enumeration  
BLUE TEAM - Detection  

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

# MITRE ATT&CK T1526 - Azure Resource Enumeration (PowerShell)

## Overview

Cloud attacks rarely start with exploitation. They start with visibility.

This PowerShell script simulates MITRE ATT&CK technique T1526 (Cloud Service Discovery) for Azure and Entra ID environments. 
It performs safe, read-only enumeration to support Red, Blue, and Purple team exercises.

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

This script safely enumerates:

- Azure subscriptions
- Resource groups
- Azure resources
- Entra ID users
- Groups
- Service principals
- App registrations
- Tenant identity surface

---

## Logical Enumeration Flow

![Enumeration Flow](https://raw.githubusercontent.com/MichaelMancuso/MITRE-T1526---Azure-Resource-Enumeration/main/images/azure-t1526-flow.png)

```
Authenticate to Azure
        |
        v
Retrieve Graph API Token
        |
        v
Enumerate Azure Resources
        |
        v
Enumerate Entra ID Users & Groups
        |
        v
Enumerate Service Principals
        |
        v
Map Tenant Attack Surface
```

---

## Red vs Blue Detection Model

![Red vs Blue](https://raw.githubusercontent.com/MichaelMancuso/MITRE-T1526---Azure-Resource-Enumeration/main/images/red-blue-model.png)

```
RED TEAM                     BLUE TEAM
---------                    ----------
Enumeration Script  -->      Audit Logs
Graph API Calls     -->      API Monitoring
Identity Discovery  -->      Alert Rules
Resource Listing    -->      Anomaly Detection
```

---

## Safety

This script is read-only and does NOT:

- Modify resources
- Change permissions
- Create identities
- Deploy infrastructure
- Attempt privilege escalation

It only performs read operations using supported Azure and Graph APIs.

---

## Red Team Value

- Rapid tenant reconnaissance
- Identity mapping
- Service principal discovery
- Resource footprint visibility
- Attack surface awareness

---

## Blue Team Value

Running this script helps defenders answer:

- Do we detect bulk enumeration?
- Are Graph API calls monitored?
- Can we distinguish admin vs attacker behavior?
- Are service principals audited?
- Do we alert on discovery patterns?

---

## Purple Team Workflow

```
Red Team runs enumeration
        |
        v
Blue Team monitors telemetry
        |
        v
Detection gaps identified
        |
        v
SIEM rules updated
        |
        v
Exercise repeated
```

---

## GitHub Script

https://github.com/MichaelMancuso/MITRE-T1526---Azure-Resource-Enumeration/blob/main/MITRE%20T1526%20-%20Azure%20Resource%20Enumeration.ps1

---

## Author

Michael Mancuso

---

## Disclaimer

This script is intended for authorized security testing only.
Do not run against environments without proper approval.

