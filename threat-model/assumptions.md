
## Use Case
This platform provides private LLM inference for internal enterprise users.
It is intended to process potentially sensitive data including:
- Internal company IP
- PII (emails, names)
- Limited PHI (non-clinical)

## Constraints
- No prompts or outputs may leave the AWS account
- No public internet access to AI services
- All access must be authenticated, logged, and auditable
- The system must support incident response and access revocation

## Out of Scope
- Model training
- Fine-tuning
- Public-facing chatbot access
