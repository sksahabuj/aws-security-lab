# AWS Security Lab - Production-Grade Cloud Security Monitoring

[![AWS](https://img.shields.io/badge/AWS-Cloud_Security-orange)](https://aws.amazon.com)
[![Python](https://img.shields.io/badge/Python-3.x-blue)](https://www.python.org)
[![Status](https://img.shields.io/badge/Status-In_Progress-yellow)]()

## 🎯 Project Overview

Building a comprehensive AWS security monitoring lab using CloudTrail, GuardDuty, Security Hub, and Config with Python-based automation for detection and response.

**Goal:** Demonstrate hands-on cloud security architecture skills by implementing production-grade security controls in AWS Free Tier environment.

## 🏗️ Architecture
```
┌─────────────────────────────────────────────────────────┐
│                     AWS Account                          │
│                                                          │
│  ┌──────────────┐    ┌──────────────┐   ┌────────────┐ │
│  │  CloudTrail  │───▶│  S3 Bucket   │◀──│   Lambda   │ │
│  │ (All Regions)│    │  (Logs)      │   │ (Analysis) │ │
│  └──────────────┘    └──────────────┘   └────────────┘ │
│         │                                      │         │
│         ▼                                      ▼         │
│  ┌──────────────┐    ┌──────────────┐   ┌────────────┐ │
│  │  GuardDuty   │───▶│ EventBridge  │──▶│    SNS     │ │
│  │  (Threats)   │    │   (Rules)    │   │  (Alerts)  │ │
│  └──────────────┘    └──────────────┘   └────────────┘ │
│                                                          │
│  ┌──────────────┐    ┌──────────────┐                  │
│  │Security Hub  │    │  AWS Config  │                  │
│  │(Aggregation) │    │ (Compliance) │                  │
│  └──────────────┘    └──────────────┘                  │
└─────────────────────────────────────────────────────────┘
```

## 📋 Implementation Phases

### ✅ Phase 1: Foundation (Week 1-2) - IN PROGRESS
- [x] AWS Free Tier account setup ✅ **[Feb 22, 2026](docs/task-01-aws-account-setup.md)**
- [x] IAM user with MFA configuration ✅ **[Feb 22, 2026](docs/task-01-aws-account-setup.md)**
- [ ] CloudTrail multi-region trail setup
- [ ] S3 bucket with encryption and versioning
- [ ] GuardDuty activation
- [ ] Security Hub enablement

### 🔄 Phase 2: Automation (Week 3-4) - PLANNED
- [ ] Python script for IAM security audit
- [ ] Automated S3 bucket security checks
- [ ] CloudTrail log analysis script
- [ ] Security finding aggregation

### 🔄 Phase 3: Detection (Week 5-6) - PLANNED
- [ ] Custom EventBridge rules for threat detection
- [ ] Lambda functions for automated response
- [ ] SNS alerting for critical findings
- [ ] Security dashboard creation

### 🔄 Phase 4: Advanced (Week 7-8) - PLANNED
- [ ] Custom CSPM tool development
- [ ] CIS Benchmark compliance checking
- [ ] Automated remediation workflows
- [ ] Security posture reporting

## 🛠️ Tech Stack

- **Cloud Platform:** AWS (Free Tier)
- **Security Services:** CloudTrail, GuardDuty, Security Hub, Config, IAM
- **Automation:** Python 3.x, Boto3, AWS Lambda
- **Alerting:** SNS, EventBridge
- **Storage:** S3 with encryption
- **Compliance:** CIS AWS Foundations Benchmark

## 📚 What I'm Learning

- AWS security service architecture and integration
- Python automation for cloud security tasks
- Detection engineering in cloud environments
- Security-as-Code principles
- Real-world CSPM implementation

## 🎓 Skills Demonstrated

✅ Cloud security architecture design  
✅ AWS security services configuration  
✅ Python scripting for security automation  
✅ Security logging and monitoring  
✅ Compliance framework implementation  
✅ Incident detection and response

## 📂 Repository Structure
```
aws-security-lab/
├── README.md
├── architecture/
│   └── diagrams/
├── scripts/
│   ├── iam_audit.py
│   ├── s3_security_check.py
│   └── cloudtrail_analyzer.py
├── terraform/  (future)
│   └── infrastructure/
├── docs/
│   ├── setup_guide.md
│   └── lessons_learned.md
└── findings/
    └── security_reports/
```

## 🚀 Quick Start

*Coming Soon: Detailed setup instructions once Phase 1 is complete*

# 📊 Current Status

**Started:** February 22, 2026  
**Current Phase:** Phase 1 - Foundation Setup  
**Completion:** 25%  
**Next Milestone:** CloudTrail + GuardDuty operational by March 1, 2026

**Recent Activity:**
- ✅ Feb 22, 2026: AWS account created with MFA security hardening
- ✅ Feb 22, 2026: IAM administrative user configured (security-conscious approach)
- 🔄 In Progress: CloudTrail logging configuration (Task 2)

**Security Note:** All account IDs and usernames redacted in public documentation per security best practices.


## 🔗 Related Projects

- [security-automation-scripts](../security-automation-scripts) - Python security tools
- [threat-detection-rules](../threat-detection-rules) - Detection rules for cloud
- [soc-to-cloud-security](../soc-to-cloud-security) - Learning journey documentation

---

*Part of my transition from SOC Operations to Cloud Security Engineering*  
*Building in public | Learning constantly | Documenting everything*

**Author:** SK Sahabuj Zaman | [GitHub](https://github.com/sksahabuj) | [Email](mailto:sksahabuj@gmail.com)
