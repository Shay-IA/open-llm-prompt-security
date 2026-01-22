# Control to Risk Mapping

This document provides traceability between the AI security controls defined in
this repository and the AI risk taxonomy.

The purpose of this mapping is to support:
- Risk assessments
- Control coverage analysis
- Audit and assurance activities

This mapping is not intended to imply one-to-one coverage. Multiple controls may
address a single risk, and a single control may mitigate multiple risks.

---

## AI-SEC-01: Prompt Injection Protection

**Mapped Risks**
- PR-01: Direct Prompt Injection
- PR-03: Instruction Override & Role Hijacking


## AI-SEC-02: Context Isolation for Untrusted Content

**Mapped Risks**
- PR-02: Indirect Prompt Injection


## AI-SEC-03: Output Data Leakage Prevention

**Mapped Risks**
- PR-04: Data Exfiltration via Prompts
