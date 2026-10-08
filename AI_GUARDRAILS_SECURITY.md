# AI Guardrails and Security

## Mandatory design principle

Model guardrails are not a security boundary. Deterministic authorization, tenant isolation, input validation, secret isolation and audit controls must exist outside the model.

## Required topics

- Prompt and indirect prompt injection.
- Jailbreak resistance and adversarial evaluation.
- PII detection, redaction and privacy.
- Tool authorization and privilege boundaries.
- Human approval for high-risk actions.
- RAG document poisoning and retrieval-time ACLs.
- Secret protection and model supply-chain risk.
- Output validation, unsafe content filtering and hallucination checks.
- OWASP Top 10 for LLM applications and agentic AI attacks.
- AWS Bedrock Guardrails and monitoring.

## Required tests

- Injection through document content and model tool arguments.
- Cross-tenant retrieval and unauthorized source access.
- PII leakage in prompts and structured outputs.
- Excessive tool permissions and data exfiltration.
- False-positive evaluation for benign requests.
- Audit trace completeness and secret redaction.
