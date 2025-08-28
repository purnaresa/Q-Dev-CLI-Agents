# Q Developer CLI Agent for Security Engineers

This specialized Q Developer CLI agent is designed for security engineers working with AWS environments. It provides focused capabilities for security configuration review, problem remediation, and security investigation workflows.

## Agent Capabilities

### Security Configuration Review
- IAM policy analysis and recommendations
- Security group and NACL configuration assessment
- S3 bucket security posture evaluation
- KMS key management and encryption analysis
- VPC security configuration review

### Problem Remediation
- Automated security finding remediation scripts
- Compliance violation fixes
- Security baseline enforcement
- Configuration drift correction
- Access control remediation

### Security Investigation
- CloudTrail log analysis for security events
- GuardDuty finding investigation
- Security Hub finding correlation
- Access pattern analysis
- Incident response support

## Supported AWS Services

The agent has pre-configured access to key AWS security services:

- **Identity & Access Management**: IAM, Access Analyzer
- **Security Services**: Security Hub, GuardDuty, Inspector, Detective, Macie
- **Compliance & Governance**: Config, CloudTrail, Organizations, Control Tower
- **Data Protection**: KMS, Secrets Manager, Systems Manager
- **Infrastructure Security**: EC2, VPC, S3
- **Monitoring & Support**: Trusted Advisor, Support API

## Usage Examples

### Security Configuration Review
```bash
q chat --agent security-engineer-agent
> Review the IAM policies in my account for overprivileged access
> Analyze S3 bucket configurations for public access risks
> Check security group rules for overly permissive access
```

### Problem Remediation
```bash
q chat --agent security-engineer-agent
> Remediate Security Hub findings for CIS AWS Foundations Benchmark
> Fix GuardDuty findings related to cryptocurrency mining
> Implement least privilege access for IAM roles
```

### Security Investigation
```bash
q chat --agent security-engineer-agent
> Investigate suspicious API calls in CloudTrail logs
> Analyze GuardDuty findings for potential security incidents
> Correlate Security Hub findings across multiple accounts
```

## File Structure

```
security-engineer-agent/
├── README.md                          # This file
├── security-engineer-agent.json       # Agent configuration
├── security-playbooks/               # Security response playbooks
├── compliance-frameworks/            # Compliance framework definitions
├── security-baselines/              # Security baseline configurations
├── incident-response/               # Incident response procedures
└── remediation-templates/           # Automated remediation templates
```

## Security Best Practices

The agent is configured with security-first principles:

- **Least Privilege Access**: Only essential AWS services are permitted
- **Read-Only by Default**: Most operations are read-only unless explicitly required
- **Audit Trail**: All actions are logged and traceable
- **Secure File Operations**: File write access is restricted to security-specific directories
- **Command Restrictions**: Only security-relevant commands are permitted

## Creating the Agent

To create this Q Developer agent using the configuration file:

1. **Create agent from configuration**:
   ```bash
   q agent create --from-file security-engineer-agent.json
   ```

2. **Verify agent creation**:
   ```bash
   q agent list
   ```

## Getting Started

1. Load the agent: `q chat --agent security-engineer-agent`
2. Begin with a security assessment: "Perform a comprehensive security review of my AWS account"

## Integration with Security Tools

The agent supports integration with popular security tools:

- **Checkov**: Infrastructure as Code security scanning
- **cfn-lint**: CloudFormation template validation
- **Prowler**: AWS security assessment tool
- **AWS CLI**: Native AWS service interactions
- **jq**: JSON processing for API responses

This agent empowers security engineers to efficiently manage AWS security posture while maintaining proper access controls and audit capabilities.
