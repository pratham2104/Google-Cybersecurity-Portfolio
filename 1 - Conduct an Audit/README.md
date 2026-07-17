# Conduct an Audit

**Scenario:** Internal security audit for Botium Toys, a small US-based toy retailer scaling into international e-commerce, with a focus on payment processing and EU compliance.

**What I did:** Built a full controls-and-compliance assessment covering asset inventory, a 14-point controls checklist, and compliance checks against PCI DSS, GDPR, and SOC 1/2. Mapped every gap back to the NIST CSF "Identify" function and scored overall risk.

**Key finding:** Risk score 8/10 (high). No encryption on stored card data, no IDS, no backups or disaster-recovery plan, and no least-privilege model, meaning any employee could access cardholder and customer PII. Recommended RBAC, encryption at rest and in transit, IDS deployment, and formal DR planning.

**Files:** `1.1 - Security Audit.md`
