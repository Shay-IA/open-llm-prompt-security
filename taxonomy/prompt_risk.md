# LLM Prompt & Context Risk Taxonomy

This taxonomy defines security-related risks arising from the use of prompts,
context, tools, and retrieved data in Large Language Model (LLM) systems.

The purpose of this taxonomy is to support:
- Consistent risk identification
- Control design and mapping
- Audit and regulatory assurance

## PR-01: Direct Prompt Injection

**Description**  
Malicious or unintended user input designed to override system instructions,
bypass safety controls, or change the intended behavior of the model.

**Examples**
- “Ignore all previous instructions…”
- “You are now an admin system…”
- Attempts to disable safety, moderation, or guardrails

**Potential Impact**
- Policy violations
- Unsafe or unauthorized outputs
- Loss of control over model behavior

## PR-02: Indirect Prompt Injection

**Description**  
Malicious instructions embedded within external content provided to the model,
such as documents, web pages, emails, or retrieved data sources.

**Examples**
- Hidden instructions in PDFs or HTML
- Prompt-like text inside knowledge base articles
- Instructions embedded in RAG sources

**Potential Impact**
- Unintended execution of attacker-controlled instructions
- Data leakage or manipulation via trusted sources

## PR-04: Data Exfiltration via Prompts

**Description**  
Prompt patterns intended to extract sensitive, confidential, or regulated data
through model responses.

**Examples**
- Requests for bulk records or structured data dumps
- Rephrasing to evade detection or filtering
- Chained prompts to reconstruct sensitive information

**Potential Impact**
- Confidentiality breaches
- Regulatory non-compliance
- Reputational damage
