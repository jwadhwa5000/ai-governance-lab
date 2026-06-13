# CrowdStrike Falcon — AI Governance & GRC Platform Profile

**Category:** Endpoint Security / AI-Powered Threat Detection  
**Relevance:** AI Model Security, Runtime Threat Detection, Compliance Evidence Generation  
**Target Sectors:** Financial Services, Federal, Healthcare  
**Portfolio Context:** FinServ Corp AI Governance Program — Platforms Layer

---

## What CrowdStrike Does

CrowdStrike Falcon is a cloud-native endpoint detection and response (EDR) platform that uses AI and machine learning models to detect, prevent, and respond to threats in real time. For AI governance practitioners, CrowdStrike is relevant at two levels:

1. **As a security control** — protecting the infrastructure where AI models run (endpoints, cloud workloads, pipelines)
2. **As an AI system itself** — its ML-based detection models are subject to the same governance requirements (bias, drift, explainability) that your AI governance program applies to internal models

---

## Core Capabilities Relevant to AI Governance

| Capability | Governance Relevance |
|---|---|
| AI-powered threat detection (Charlotte AI) | Vendor AI system requiring ISO 42001 due diligence |
| Endpoint Detection & Response (EDR) | Protects ML training infrastructure and model serving endpoints |
| Identity Threat Protection | Monitors non-human identities (NHI) and service accounts used by AI pipelines |
| Cloud Security (Falcon Horizon) | Secures AWS/Azure environments hosting AI workloads |
| Threat Intelligence (Falcon X) | Informs AI-specific threat modeling (model theft, adversarial attacks) |
| Audit Logs & Telemetry | Continuous compliance evidence for SOX ITGC, NIST AI RMF, ISO 42001 |

---

## AI Governance Framework Mapping

### ISO 42001 Alignment

| ISO 42001 Clause | CrowdStrike Control |
|---|---|
| **6.1 — Risk Assessment** | Falcon threat intelligence feeds inform AI-specific risk register |
| **8.4 — AI System Security** | EDR coverage of model training and inference endpoints |
| **9.1 — Monitoring** | Continuous telemetry on AI infrastructure access and anomalies |
| **A.6.2 — Data Security** | Protects training data pipelines from exfiltration or tampering |
| **A.8.3 — Incident Management** | Falcon's automated response integrated into AI incident playbooks |

### NIST AI RMF Alignment

| AI RMF Function | CrowdStrike Contribution |
|---|---|
| **GOVERN** | Vendor AI governance review of Charlotte AI (Falcon's own ML) |
| **MAP** | Threat mapping for AI-specific attack vectors (model inversion, poisoning) |
| **MEASURE** | Runtime monitoring metrics fed into AI risk dashboard |
| **MANAGE** | Automated containment of threats to AI infrastructure |

### NIST SP 800-53 Control Mapping

| Control Family | Relevant Controls | CrowdStrike Coverage |
|---|---|---|
| **SI — System Integrity** | SI-3, SI-4, SI-7 | Malware protection, monitoring, integrity verification |
| **IR — Incident Response** | IR-4, IR-5, IR-6 | Detection, response, and reporting automation |
| **AU — Audit & Accountability** | AU-2, AU-6, AU-12 | Continuous audit log generation and review |
| **IA — Identification & Authentication** | IA-4, IA-5 | Identity threat protection for AI service accounts |
| **CM — Configuration Management** | CM-7, CM-8 | Endpoint configuration baseline and inventory |

---

## AI-Specific Threat Scenarios CrowdStrike Addresses

**1. Model Theft / IP Exfiltration**  
Adversaries targeting model weights or training data via compromised endpoints. Falcon EDR detects lateral movement and unusual data access patterns on ML infrastructure.

**2. Training Data Poisoning**  
Unauthorized modification of data pipelines feeding production models. Falcon's file integrity monitoring and identity protection detect unauthorized access to data stores.

**3. Adversarial Infrastructure Attacks**  
Attacks targeting model serving infrastructure (inference APIs, GPU clusters). Falcon Cloud Security provides runtime protection for containerized AI workloads on AWS/Azure.

**4. Non-Human Identity Compromise**  
AI service accounts and pipeline credentials are high-value targets. Falcon Identity Protection monitors NHI behavior and flags anomalous access patterns.

---

## FinServ Corp Integration Architecture

```
AI Model Pipeline (AWS/Azure)
        ↓
CrowdStrike Falcon Sensor (endpoint coverage)
        ↓
Falcon Cloud → Telemetry & Alerts
        ↓
    ┌───────────────────────────┐
    │  ServiceNow IRM           │  ← Automated incident tickets
    │  Databricks               │  ← Anomaly detection enrichment  
    │  AI Governance Dashboard  │  ← Control health monitoring
    └───────────────────────────┘
```

**Integration Points:**
- **ServiceNow**: CrowdStrike alerts auto-create incidents and map to GRC controls via API
- **Databricks**: Falcon telemetry ingested for ML-based anomaly detection at scale
- **GitHub**: Falcon scans CI/CD pipeline runners for compromised build environments

---

## Vendor AI Governance Review (Charlotte AI)

CrowdStrike's own AI system (Charlotte AI) is subject to third-party AI governance review under FinServ Corp's vendor AI policy.

| Review Dimension | Assessment Notes |
|---|---|
| **Intended Use** | Security alert triage, threat summarization, analyst augmentation |
| **Training Data** | Proprietary threat intelligence corpus — vendor attestation required |
| **Explainability** | Alert rationale provided; full model explainability limited |
| **Bias Risk** | Low for security use case; monitor for false positive patterns by environment type |
| **Human Oversight** | Human-in-the-loop confirmed for high-severity response actions |
| **ISO 42001 Attestation** | Request vendor SOC 2 Type II + AI governance questionnaire annually |

---

## Compliance Evidence Generated

CrowdStrike automatically generates continuous evidence supporting:

- SOX ITGC (change management, access controls, monitoring)
- PCI-DSS 4.0 (requirement 10 — logging and monitoring)
- GLBA Safeguards Rule (technical safeguards for customer data)
- NIST CSF 2.0 (Detect and Respond functions)
- ISO 27001 Annex A (A.8.15 logging, A.8.16 monitoring)

All evidence streams via API to ServiceNow GRC for continuous control assurance — eliminating manual quarterly evidence collection.

---

## Interview Talking Points

> "CrowdStrike sits at an interesting intersection in my governance program — it's both a security control protecting our AI infrastructure and itself an AI system subject to our vendor governance process. I treat Charlotte AI the same way I treat any third-party model: I require explainability documentation, human oversight attestation, and annual review against our ISO 42001 vendor requirements. That dual lens — CrowdStrike as control and CrowdStrike as governed AI — is a good example of how mature AI governance has to think about the full ecosystem, not just internal models."

---

## References

- [CrowdStrike Falcon Platform Overview](https://www.crowdstrike.com/platform/)
- [Charlotte AI Documentation](https://www.crowdstrike.com/products/charlotte-ai/)
- NIST SP 800-53 Rev 5 — SI, IR, AU, IA, CM control families
- ISO/IEC 42001:2023 — Clauses 6, 8, 9, Annex A
- NIST AI RMF 1.0 — GOVERN, MAP, MEASURE, MANAGE functions

---

*Last updated: June 2026 | Owner: AI Governance & Cybersecurity Risk | FinServ Corp*
