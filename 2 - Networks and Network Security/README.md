# Networks and Network Security

Five incident investigations, each built around packet-level traffic analysis.

| File | Scenario | Finding |
|---|---|---|
| 2.1 | Customers can't reach a website; DNS queries failing | tcpdump showed repeated ICMP "port 53 unreachable" errors — DNS server down or blocked, isolated using UDP/port/timestamp analysis |
| 2.2 | Travel agency website times out under load | Wireshark log showed a flood of TCP SYN packets from a single IP with no completing ACK — a SYN flood (DoS), diagnosed via the three-way-handshake pattern |
| 2.3 | Site defaced and users redirected to a spoofed domain | Traced the incident through tcpdump: brute-forced admin login → injected JavaScript → redirect to a fake domain. Recommended MFA on admin panels |
| 2.4 | Social media company data breach | Identified four hardening gaps (shared passwords, default admin credentials, no firewall rules, no MFA) and prioritized fixes by implementation frequency |
| 2.5 | DDoS via ICMP flood knocks out internal network for 2 hours | Full NIST CSF response plan (Identify/Protect/Detect/Respond/Recover) built around the incident, including firewall rate-limiting and IDS/SIEM recommendations |

**Files:** `2.1` through `2.5`
