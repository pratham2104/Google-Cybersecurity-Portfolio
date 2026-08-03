# Assets, Threats & Vulnerabilities

**Scenario:** A set of exercises covering asset classification, risk scoring, and threat modeling across different mock organizations (a home network, a regional bank, a social media company, an e-commerce firm, and a hospital).

**What I did:**
- Built a home-network asset inventory and assigned sensitivity levels (restricted/confidential/etc.)
- Created a risk register for a bank, scoring risks like business email compromise and unencrypted customer records by likelihood × severity
- Documented a real-world data-leak pattern (over-broad folder access leading to an accidental external share) and mapped it to the least-privilege control failure
- Wrote a vulnerability assessment for an e-commerce company's publicly exposed MySQL database, following NIST SP 800-30
- Analyzed a social-engineering scenario (a planted USB drive at a hospital) from the attacker's perspective
- Built a full **PASTA threat model** for a mock sneaker marketplace app, mapping business objectives to attack surfaces

**Key finding:** In the PASTA exercise, SQL, not the encryption layer, came out as the highest-priority attack surface, since a compromised database undermines every control built on top of it.

**Files:** `4.1` through `4.7`
