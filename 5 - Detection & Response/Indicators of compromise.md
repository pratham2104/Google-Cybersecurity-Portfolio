# Pyramid of Pain

Not all **Indicators of Compromise (IoCs)** are equal in the value they provide to security teams. It’s important for security professionals to understand the different types of indicators of compromise so they can quickly and effectively **detect and respond** to threats.

To address this, **security researcher David J. Bianco** created the concept of the **Pyramid of Pain**, which aims to improve how IoCs are used in **incident detection and response**.

---

## Overview

The **Pyramid of Pain** is a triangle divided into six tiers, each representing a type of indicator of compromise and its **corresponding level of difficulty** for attackers when defenders block it.

The model illustrates the relationship between **types of IoCs** and the **“pain”** attackers experience when their activities are detected and mitigated.

Blocking indicators higher in the pyramid causes **greater disruption** to attackers and makes it **harder** for them to continue their operations.

---
<img width="1343" height="710" alt="image" src="https://github.com/user-attachments/assets/57d189c3-f25c-4bae-acbe-0d2485c3ea29" />


## Levels of the Pyramid

| Level | Indicator Type | Description | Difficulty for Attackers |
|:------|:----------------|:-------------|:--------------------------|
| **1. Hash Values** | Unique identifiers corresponding to known malicious files. | Hashes provide specific references to malware or intrusion files. | 🟢 *Easy* – attackers can quickly change or recompile malware. |
| **2. IP Addresses** | Internet Protocol addresses (e.g., `192.168.1.1`). | Used to identify the source or destination of network traffic. | 🟢 *Easy* – attackers can switch to new IPs easily. |
| **3. Domain Names** | Web addresses (e.g., `www.google.com`). | Used to identify malicious servers or phishing sites. | 🟡 *Moderate* – attackers can register new domains but takes more effort. |
| **4. Network Artifacts** | Observable evidence found in network protocols (e.g., User-Agent strings). | Created during malicious activity in network communications. | 🟠 *Challenging* – requires attackers to modify their tools or patterns. |
| **5. Host Artifacts** | Evidence created on a compromised host system. | Includes file names, registry keys, or processes created by malware. | 🔵 *Hard* – attackers must alter malware behavior significantly. |
| **6. Tools** | Software used by attackers (e.g., **John the Ripper** for password cracking). | These tools enable various stages of an attack. | 🔴 *Very Hard* – losing access to familiar tools slows them down. |
| **7. Tactics, Techniques, and Procedures (TTPs)** | Describes attacker **behavior patterns**. | - **Tactics**: high-level goals of the attack. <br> - **Techniques**: methods used to achieve the goals. <br> - **Procedures**: step-by-step implementation details. | ⚫ *Extremely Hard* – forcing attackers to change core behaviors is most painful. |

---

## Key Takeaways

- **Indicators of Compromise (IoCs)** and **Indicators of Attack (IoAs)** are critical for identifying and responding to incidents.  
- The **Pyramid of Pain** helps security professionals understand the **value and difficulty** of different IoCs.  
- The higher an indicator is on the pyramid, the **more effective** it is at disrupting malicious activity.  
- Targeting and blocking **TTPs** causes the **most pain** for attackers, forcing them to redesign their operations.  

---

**Source:** [David J. Bianco — *The Pyramid of Pain*](http://detect-respond.blogspot.com/2013/03/the-pyramid-of-pain.html)
