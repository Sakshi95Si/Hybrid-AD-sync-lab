# Entra ID Connect Sync – Setup, Configuration & Troubleshooting Lab

## Objective

This project demonstrates how to integrate an on-premises Active Directory with Azure Active Directory using **Azure AD Connect Sync**. It focuses on the complete lifecycle — from installation and configuration to running sync operations and resolving common synchronization issues — within a home lab environment designed to replicate a hybrid identity setup.

> 🔗 *For underlying Local AD lab detailed foundational setup, please refer (https://github.com/Sakshi95Si/AD-Domain_Lab).*

---

## Tools & Technologies

- **Windows Server (2019)** – Domain Controller and AAD Connect host
- **Azure Active Directory (AAD)**
- **Entra Connect Sync** – Microsoft’s identity synchronization tool
- **PowerShell** – For advanced configuration and sync control
- **Event Viewer & Sync Service Manager** – Diagnostics and monitoring

---

## Implementation Summary

### Entra Connect Installation & Configuration

- Downloaded and installed the latest Entra ID Connect build
- Performed **custom installation** to enable:
  - Organizational Unit (OU) filtering
  - Password Hash Synchronization (PHS)
  - Optional features like group writeback and device writeback

### Sync Operations

- Verified prerequisites such as DNS resolution, AD schema state, and account permissions
- Scoped sync to specific OUs to test selective object syncing
- Performed:
  - Initial sync
  - Delta sync
  - Full sync using GUI and PowerShell
- Validated results using Azure AD portal and local AD tools

### Troubleshooting Scenarios

- Simulated and resolved:
  - UPN mismatches
  - Attribute sync failures
  - DNS and connectivity issues
- Utilized:
  - Synchronization Service Manager
  - PowerShell diagnostics (`Start-ADSyncSyncCycle`, `Get-ADSyncConnectorRunStatus`)
  - Event Viewer logs for granular insight
- Reviewed sync rule precedence and Metaverse object state

---

## Key Learnings

- Deep understanding of how AAD Connect bridges on-prem and cloud identities
- Sync rule customization and staging mode practices
- Hands-on troubleshooting using real logs and sync behavior
- Importance of consistent identity attributes and DNS reliability
- Improved PowerShell scripting for AAD Connect operations

---

## Outcomes

- Working hybrid identity model in a lab setup
- Configured selective OU sync between local AD and Azure AD
- Defined repeatable sync and troubleshooting workflows
- Ready for future enhancements like Seamless SSO, Pass-through Auth, or Hybrid Exchange setups

---
