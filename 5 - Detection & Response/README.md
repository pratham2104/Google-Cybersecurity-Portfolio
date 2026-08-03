# Detection & Response

**Scenario:** Incident handling and traffic analysis across a ransomware attack, a malware triage case, and hands-on IDS configuration.

**What I did:**
- Wrote an incident handler's journal for a healthcare clinic hit by ransomware delivered through a phishing attachment
- Performed packet-level traffic analysis using **Wireshark** and **tcpdump**
- Investigated a suspicious executable (`bfsvc.exe`) using **VirusTotal**, generating and cross-referencing its SHA256 hash to confirm malicious classification
- Wrote and tested a custom detection rule in **Suricata**, verifying it correctly flagged the target traffic pattern in the alert log
- Documented Indicators of Compromise (IOCs) using the Pyramid of Pain model

**Key finding:** The VirusTotal hash lookup confirmed `bfsvc.exe` as a known malicious payload disguised as a system file, delivered via a password-protected spreadsheet attachment, a real-world credential-bypass tactic (the password defeats email attachment scanning).

**Files:** `5.1` through `5.5`, plus `Indicators of compromise.md`
