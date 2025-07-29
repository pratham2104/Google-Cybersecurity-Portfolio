# Controls and Compliance Assessment  

## Case Study  
Botium Toys is a small U S–based company that designs and sells toys. One building houses the headquarters, storefront, and warehouse, but the firm’s fast-growing e-commerce presence now serves customers worldwide. The IT manager has ordered an internal security audit to gauge compliance and resilience as the company scales, with special focus on payment processing and business in the European Union.  

---

## Botium Toys: Scope, Goals, and Risk-Assessment Report  

| **Section** | **Details** |
|-------------|-------------|
| **Scope** | The entire security program including all hardware, software, data, networks, and physical premises. |
| **Goals** | 1) Inventory assets and existing controls  <br>2) Complete a controls & compliance checklist  <br>3) Pinpoint gaps and recommend fixes. |
| **Current Assets** | • On-prem equipment and employee devices  <br>• Retail inventory (store & warehouse)  <br>• Core systems: accounting, telecom, DB, security, e-commerce, inventory  <br>• Internet access & internal LAN  <br>• Data storage/retention  <br>• Legacy, end-of-life systems requiring human oversight |
| **Risk Description** | Weak asset management and several missing controls leave Botium Toys out of step with US and international regulations. |
| **Control Best Practices** | First NIST-CSF function **Identify** must be strengthened: enumerate, classify, and assign business impact to every asset. |
| **Risk Score (1-10)** | **8** (high). Deficient controls/compliance raise the chance of fines or service disruption. |
| **Key Findings** | • All employees can access card-holder and customer PII/SPII <br>• No encryption on stored/processed card data <br>• No least-privilege or separation-of-duties model <br>• Firewall and antivirus in place; IDS absent <br>• No backups or disaster-recovery plan <br>• EU breach-notification plan exists; privacy policies written and enforced <br>• Password policy exists but is weak; no central password-management system <br>• Physical locks, CCTV, and fire-safety systems are functional |

---

## Controls Assessment Checklist  

**Does Botium Toys currently have this control in place?**

| **Yes / No / ?** | **Control** | **Explanation** |
|:---:|---|---|
| **No** | Least Privilege | All employees can reach customer data; privileges must be restricted. |
| **No** | Disaster-Recovery Plan | No documented DR plan business continuity at risk. |
| **Yes** | Password Policies | A policy exists but requirements are minimal and need strengthening. |
| **No** | Separation of Duties | Single users can complete end-to-end sensitive tasks. |
| **Yes** | Firewall | Deployed and rule-set maintained by IT. |
| **No** | Intrusion-Detection System (IDS) | No IDS/IPS to alert on malicious traffic. |
| **No** | Backups | No offline or off-site backups of critical data. |
| **Yes** | Antivirus Software | Installed and regularly monitored by IT. |
| **Yes** | Manual Monitoring for Legacy Systems | Legacy platforms are watched, but the schedule is ad-hoc. |
| **No** | Encryption | Card data is stored and transmitted unencrypted. |
| **No** | Password-Management System | No centralized vault to enforce complexity and rotation. |
| **Yes** | Locks (Office / Storefront / Warehouse) | Physical doors and display cases are secured. |
| **Yes** | CCTV Surveillance | Cameras cover sales floor, warehouse, and entrances. |
| **Yes** | Fire Detection / Prevention | Alarms and sprinklers operational; routine maintenance needed. |

---

## Compliance Checklist  

### Payment Card Industry Data Security Standard (PCI DSS)

| **Yes / No / ?** | **Best Practice** | **Explanation** |
|:---:|---|---|
| **No** | Only authorized users access card data | Cardholder info viewable by any employee. |
| **No** | Card data stored / processed / transmitted securely | Data stored locally without segmentation. |
| **No** | Encryption at every touch-point | No encryption in storage or transit. |
| **No** | Secure password-management policies | Weak complexity rules; no centralized enforcement. |

### General Data Protection Regulation (GDPR)

| **Yes / No / ?** | **Best Practice** | **Explanation** |
|:---:|---|---|
| **No** | EU customer data kept private / secure | Same broad access issue as PCI data. |
| **Yes** | 72-hour breach-notification plan | Documented plan exists. |
| **No** | Data classified and inventoried | Assets not formally catalogued. |
| **Yes** | Privacy policies & procedures enforced | Policies written and communicated to staff. |

### System and Organization Controls (SOC 1 / SOC 2)

| **Yes / No / ?** | **Best Practice** | **Explanation** |
|:---:|---|---|
| **No** | User-access policies established | No formal role-based access model. |
| **No** | Sensitive data (PII/SPII) kept confidential | Unrestricted access to PII/SPII. |
| **Yes** | Data integrity assured | IT monitors data consistency and validity. |
| **Yes** | Data available to authorized users | Systems generally available, but access too broad. |

---

## Recommendations  

1. **Enforce Least Privilege & Separation of Duties** – create role-based access controls and approval workflows.  
2. **Encrypt Payment Data** – apply full-disk and in-transit encryption to all card-holder information.  
3. **Deploy IDS/IPS & Centralized Logging** – enable real-time detection and response.  
4. **Institute Disaster-Recovery & Off-Site Backups** – define RPO/RTO targets and test regularly.  
5. **Strengthen Authentication** – adopt MFA, raise password complexity, and roll out a managed password vault.  
6. **Comprehensive Asset Inventory** – classify, tag, and map controls to each asset for GDPR/SOC compliance.  
7. **Formalize Legacy-System Maintenance** – schedule patching/monitoring and plan phased replacement.  

---
