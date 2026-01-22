# Foundational LLM Prompt Security Controls

This document defines a small set of **foundational AI security controls**
focused on mitigating prompt and context-related risks in LLM systems.

These controls represent a **minimum defensible baseline** and are intentionally
limited in number. They are designed to be:
- High impact
- Technically feasible
- Auditable
- Applicable across industries

They should be applied proportionately based on risk and use case.

## AI-SEC-01: Prompt Injection Protection

**Objective**  
Prevent unauthorized override of system instructions and safety constraints.

**Control Statement**  
LLM systems shall implement mechanisms to detect and prevent prompt injection
attempts, including instruction override, role reassignment, and policy bypass
patterns.

**Risk Addressed**  
- Direct prompt injection  
- Instruction override and role hijacking  

**Evidence Expectations**
- Prompt filtering or detection rules
- Logs of blocked or flagged injection attempts
- Periodic review and tuning records

  ## AI-SEC-02: Context Isolation for Untrusted Content

**Objective**  
Ensure untrusted external content does not influence system instructions or
control logic.

**Control Statement**  
LLM systems shall logically separate system instructions from untrusted content,
including documents, retrieved data, and user-supplied context, to prevent
indirect prompt injection.

**Risk Addressed**  
- Indirect prompt injection via RAG, documents, or tools  

**Evidence Expectations**
- Context handling or sanitization logic
- Documentation of trusted vs untrusted content sources
- Testing demonstrating isolation effectiveness

  ## AI-SEC-03: Output Data Leakage Prevention

**Objective**  
Prevent unintended disclosure of sensitive, confidential, or regulated data
through LLM outputs.

**Control Statement**  
LLM systems shall implement output inspection and filtering to detect and prevent
the disclosure of sensitive data, including personal data, credentials, and
confidential information.

**Risk Addressed**  
- Data exfiltration via prompts or chained interactions  

**Evidence Expectations**
- Output filtering or DLP mechanisms
- Records of blocked or redacted responses
- Incident handling and escalation procedures
