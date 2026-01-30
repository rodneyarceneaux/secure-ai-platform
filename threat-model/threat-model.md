## Threat Model (STRIDE)

### Spoofing
Risk: Unauthorized users invoking the model  
Mitigation:
- IAM authentication
- VPC endpoint restrictions
- No public endpoints

### Tampering
Risk: Prompt injection or malicious prompt manipulation  
Mitigation:
- Lambda prompt inspection
- Input validation
- Rejection of high-risk patterns

### Repudiation
Risk: Users deny submitting prompts  
Mitigation:
- CloudTrail data events
- Request ID logging
- Immutable logs

### Information Disclosure
Risk: Sensitive data leaks via prompts or outputs  
Mitigation:
- PII detection
- Encryption with CMKs
- No internet egress

### Denial of Service
Risk: Prompt flooding / token abuse  
Mitigation:
- API rate limiting
- Usage quotas
- Monitoring for spikes

### Elevation of Privilege
Risk: IAM role misuse to access AI services  
Mitigation:
- IAM condition keys
- Session tags
- Least privilege
