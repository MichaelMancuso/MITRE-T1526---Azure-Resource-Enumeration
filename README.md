# MITRE-T1526---Azure-Resource-Enumeration
T1526 - Cloud Service Discovery - Red Team TTP Demo .DESCRIPTION     Enumerates Azure/M365 cloud services and resources within the tenant.     For authorized red team use only.
# 🔍 MITRE ATT&CK T1526 - Azure Resource Enumeration (PowerShell)

## 📌 Overview

This PowerShell script simulates **MITRE ATT&CK Technique T1526 – Cloud Service Discovery** by enumerating Azure and Entra ID resources within a tenant.

It is designed for:
- 🔴 Red Team exercises
- 🟣 Purple Team validation
- 🔵 SOC detection tuning

The script provides a **realistic attacker simulation** while also highlighting **defensive telemetry and detection opportunities**.

---

## ⚔️ Technique Mapping

- **MITRE ATT&CK**: T1526 – Cloud Service Discovery  
- **Tactic**: Discovery  
- **Platform**: Azure / Entra ID (M365)

---

## 🔧 Features

- ✅ Auto-installs required modules (`Az.Accounts`, `Az.Resources`)
- 🔐 Authenticates using `Connect-AzAccount`
- 🎯 Uses **Graph API via token reuse** (no SDK dependency)
- 📊 Enumerates:
  - Azure Subscriptions & Resource Groups
  - Entra ID Users & Groups
  - Service Principals & App Registrations
- ⚙️ Interactive execution (operator-driven)
- 🚨 Includes **SOC detection guidance**

---

## 📥 Requirements

- PowerShell 5.1+ or PowerShell Core
- Azure account with appropriate permissions
- Internet access for module installation

---

## 🚀 Usage

```powershell
.\T1526-Azure-Enumeration.ps1
