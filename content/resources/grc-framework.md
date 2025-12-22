---
title: "Framework Tata Kelola IT (GRC)"
description: "Framework komprehensif untuk membangun tata kelola IT yang sustainable"
date: 2025-12-12
---

## Framework Tata Kelola IT (GRC) untuk Utilitas Air

Saya mengembangkan framework ini setelah membantu puluhan PDAM setup atau improve governance structure mereka. Yang saya pelajari adalah: governance bukan "one-size-fits-all". PDAM besar membutuhkan struktur formal dengan council meetings; PDAM kecil bisa dengan approach lebih lean. Yang penting adalah clarity tentang roles, accountability, dan decision-making—regardless dari formality level.

Framework GRC (Governance, Risk & Compliance) yang kuat adalah fondasi untuk operasi IT yang reliable, efficient, dan compliant. Panduan ini provides practical framework yang dapat diadopt atau disesuaikan oleh PDAM dalam developing IT governance structure mereka—sesuai dengan ukuran, kompleksitas, dan maturity level organisasi.

### Framework Structure Overview

```
GOVERNANCE (Struktur & Accountability)
├── IT Strategy & Governance Council
├── Roles & Responsibilities (RACI matrix)
├── Decision-making Authority & Escalation
├── Performance Metrics & Reporting

RISK MANAGEMENT (Identifikasi & Mitigation)
├── Risk Assessment Process
├── Risk Registry & Monitoring
├── Mitigation Planning & Execution
├── Risk Reporting to Board

COMPLIANCE (Regulation & Policies)
├── Regulatory Requirements Mapping
├── Policy Development & Communication
├── Compliance Verification & Audit
├── Incident Management & Reporting
```

### 1. GOVERNANCE: Struktur & Accountability

#### 1.1 IT Governance Council Establishment

**Composition:**
- Chief Executive Officer (chair)
- Chief Information Officer (CIO) / Head of IT
- Finance Director (untuk budget oversight)
- Operations Director (untuk operational technology)
- Risk Manager (untuk risk oversight)

**Responsibility:**
- Approve IT strategy & major investments
- Review quarterly IT performance & risks
- Approve policies & major decisions
- Accountability untuk IT effectiveness

**Meeting frequency:** Quarterly minimum (dapat lebih frequent jika high-risk initiatives)

#### 1.2 RACI Matrix (Roles & Responsibilities)

Create clear matrix untuk major IT decisions:

| Decision/Activity | CEO | CIO | Finance | Operations | IT Team |
|---|---|---|---|---|---|
| IT Strategy approval | A | R | C | C | C |
| Major system procurement | A | R | A | C | C |
| Budget approval | A | R | R | C | I |
| Security policy update | A | C | I | R | R |
| System maintenance window | I | R | I | A | R |
| Incident response | A | R | I | C | R |

*A = Accountable (decision maker); R = Responsible (execute); C = Consult (input); I = Inform (notification)*

#### 1.3 Decision-making Authority Framework

**Clear escalation untuk berbagai decisions:**

| Decision Type | Authority | Approval Level | Timeline |
|---|---|---|---|
| IT operational decisions | CIO | No approval needed | As needed |
| Budget allocation <Rp 100 juta | CIO | CIO approval | Monthly review |
| Budget allocation Rp 100-1 milyar | CFO | Finance Director | Quarterly |
| Budget allocation >Rp 1 milyar | CEO | CEO approval | Annual planning |
| System selection (new) | CIO | CIO + Finance approval | Per project |
| Policy change | CIO | IT Council approval | Quarterly |
| Vendor contract >Rp 500 juta | Procurement | CEO + CFO approval | Per contract |

#### 1.4 Performance Metrics & Reporting

**Key IT metrics untuk reporting ke board:**

- **Availability:** System uptime % (target: 99% untuk critical, 95% untuk standard)
- **Incident Resolution:** Mean time to resolve (MTTR) average days
- **User Satisfaction:** Help desk satisfaction score (target: >80%)
- **Budget Execution:** Actual spend vs approved budget %
- **Project Completion:** On-time delivery %; Budget variance
- **Security Posture:** Vulnerabilities identified & remediated timely
- **Compliance Status:** Audit findings; remediation status
- **Staff Turnover:** IT team retention %; vacancy rate

**Report frequency:** Quarterly to board; monthly to CIO/management team

### 2. RISK MANAGEMENT: Identifikasi & Mitigation

#### 2.1 Risk Assessment Process

**Frequency:** Annual comprehensive; quarterly update untuk high-risk items

**Assessment steps:**
1. **Identify:** List semua IT-related risks (system failure, data breach, vendor failure, staff turnover, compliance violation, etc.)
2. **Assess:** Evaluate probability (likelihood) & impact (consequence) untuk each risk
3. **Prioritize:** Rank risks berdasarkan risk score (probability × impact)
4. **Plan mitigation:** Develop action untuk reduce probability atau impact
5. **Monitor:** Track mitigation progress & residual risk level

#### 2.2 Risk Registry Template

| Risk ID | Risk Description | Probability | Impact | Risk Score | Current Status | Mitigation Action | Owner | Target Date |
|---|---|---|---|---|---|---|---|---|
| R001 | ERP system failure impacting billing | Medium | High | 15 | Active | Upgrade to cloud ERP + backup procedures | CIO | Jun 2026 |
| R002 | Data breach (customer data) | Low | Critical | 12 | Planning | Implement encryption + access control | Security | Mar 2026 |
| R003 | IT staff turnover | High | Medium | 12 | Monitoring | Competency development + retention bonus | HR | Ongoing |
| R004 | Compliance violation (UU PDP) | Medium | High | 15 | In Progress | Privacy policy implementation | Legal/IT | Jun 2026 |

#### 2.3 Mitigation Strategies (The 4 T's)

For each significant risk, choose mitigation strategy:

1. **Treat (Reduce)** — Take action untuk reduce probability or impact
   - Example: Conduct cybersecurity training untuk reduce phishing risk
   - Example: Implement backup system untuk reduce failure impact

2. **Tolerate (Accept)** — Accept the risk jika mitigation cost higher than potential loss
   - Example: Accept low-probability disaster scenario jika recovery cost is prohibitive

3. **Transfer (Outsource)** — Transfer risk ke third party (e.g., insurance, vendor)
   - Example: Cyber insurance untuk reduce financial impact dari data breach
   - Example: Cloud provider service level agreement untuk transfer availability risk

4. **Terminate (Avoid)** — Eliminate risk by discontinuing activity
   - Example: Discontinue legacy system jika becoming too risky
   - Example: Stop using vendor jika security posture unacceptable

### 3. COMPLIANCE: Regulation & Policies

#### 3.1 Regulatory Requirements Mapping

Create matrix antara applicable regulations dan IT domain:

| Regulation | IT System Impact | Responsibility | Deadline | Status |
|---|---|---|---|---|
| UU PDP 2022 | Customer data privacy | IT + Legal | Sept 2025 | In Progress |
| BSSN Cybersecurity | Security standards | IT + OT | 2026 | Planning |
| UU Air Bersih 2019 | Service quality SOP | Operations + IT | Dec 2025 | In Progress |
| Audit BPK/BPKP | IT audit readiness | IT + Finance | Ongoing | Continuous |

#### 3.2 Policy Development Checklist

Essential policies untuk IT governance:

- [ ] IT Strategy & Governance policy (overall framework)
- [ ] IT Security policy (access control, password, encryption)
- [ ] Data protection & privacy policy (UU PDP compliance)
- [ ] Vendor management policy (selection, contract, monitoring)
- [ ] Software licensing policy (legal compliance, audit)
- [ ] Backup & disaster recovery policy (business continuity)
- [ ] Change management policy (system changes process)
- [ ] Incident management policy (breach, outage response)
- [ ] Cloud computing policy (jika using cloud services)
- [ ] Remote access policy (VPN, security requirement)

**For each policy:**
- Write clear, concise statement
- Specify roles & responsibilities
- Define implementation procedure
- Identify owner & review frequency (minimum annual)

#### 3.3 Compliance Verification & Audit

**Internal audit checklist (quarterly):**
- [ ] Review policy compliance (sample audit trail)
- [ ] Check access control (appropriate permissions)
- [ ] Verify system configuration (security settings)
- [ ] Test disaster recovery procedures (actual recovery test)
- [ ] Review incident logs (appropriate response)
- [ ] Check vendor compliance (contract adherence)

**External audit (annual):**
- Engage independent auditor untuk comprehensive compliance assessment
- Address audit findings dengan formal remediation plan
- Report results to board & regulator

### 4. Implementation Roadmap

**Phase 1 (Month 1-3):** Foundation
- [ ] Establish IT Governance Council (meets monthly initially)
- [ ] Create RACI matrix untuk major decisions
- [ ] Develop initial policy framework
- [ ] Conduct risk assessment (identify top 20 risks)

**Phase 2 (Month 4-9):** Implementation
- [ ] Finalize & communicate all policies
- [ ] Implement policy enforcement mechanisms
- [ ] Set up risk monitoring process
- [ ] Establish compliance audit procedures

**Phase 3 (Month 10-12):** Optimization
- [ ] First annual review & refresh
- [ ] Optimize processes based on lessons learned
- [ ] Expand metrics & reporting
- [ ] Plan for continuous improvement

### 5. Quick Self-assessment

**Rate your current state (1=Non-existent, 5=Mature):**

| Element | Current | Target |
|---|---|---|
| IT Governance Council | __ | 4 |
| Clear roles & responsibilities | __ | 4 |
| IT strategy alignment | __ | 4 |
| Risk assessment process | __ | 4 |
| Policy documentation | __ | 4 |
| Compliance audit | __ | 4 |
| Performance reporting | __ | 4 |

**Total score:** Calculate average. If <3, GRC development should be high priority.

---

*Framework ini provide starting point; setiap PDAM should customize based pada size, maturity, regulatory requirement, dan specific risk profile. Consider engaging external advisor untuk first-time implementation.*
