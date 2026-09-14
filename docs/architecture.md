# Architecture

## System Architecture

The Threat Intelligence Correlation & Alert Prioritisation Assistant follows a three-layer architecture: Data Layer, Processing Layer, and Output Layer.

flowchart TD
    A[SIEM Alerts] --> D[Data Layer]
    B[Satellite Feeds] --> D
    C[Cyber Sensors] --> D
    E[Intelligence Reports] --> D

    D --> F[Data Normalisation]
    F --> G[Threat Correlation Engine]
    G --> H[MITRE ATT&CK Mapping]
    H --> I[ML-based False Positive Filtering]
    I --> J[Alert Prioritisation]
    J --> K[BLUF Report Generation]
    K --> L[Analyst Dashboard]
    K --> M[Command Team]

---

### 2. Components

Replace the **Components** section with:

```markdown
## Components

| Component | Technology / Approach | Responsibility |
|---|---|---|
| Data Ingestion | Multi-source connectors | Collect alerts and threat intelligence from SIEM, satellite feeds, cyber sensors, and intelligence reports |
| Normalisation Layer | Unified data schema | Convert different source formats into a common structure |
| Correlation Engine | Rule-based / intelligent correlation | Identify relationships between alerts and detect coordinated attack patterns |
| Threat Intelligence Layer | Threat intelligence enrichment | Enrich alerts with relevant threat context |
| MITRE ATT&CK Mapper | MITRE ATT&CK framework | Classify attacker techniques and standardise threat assessment |
| ML Filtering | Machine learning | Reduce false positives and identify genuine threats |
| Alert Prioritisation | Risk and severity scoring | Rank threats according to their importance and contextual risk |
| BLUF Generator | Automated report generation | Produce concise, prioritised intelligence for analysts and commanders |
| Dashboard / Output | Operational dashboard | Present alerts, reports, and actionable intelligence |

## Data Flow

1. Alerts and intelligence are collected from SIEM platforms, satellite feeds, cyber sensors, and intelligence reports.
2. Incoming information is normalised into a unified data structure.
3. The correlation engine cross-references alerts from different sources to identify related events and coordinated attack patterns.
4. Threat information is enriched and attacker techniques are mapped to the MITRE ATT&CK framework.
5. Machine-learning based filtering helps reduce false positives and identify genuine threats.
6. Correlated threats are prioritised according to severity and contextual risk.
7. The system generates actionable alerts and Bottom Line Up Front (BLUF) reports.
8. Analysts and command teams receive prioritised intelligence and investigation recommendations.

## Security Considerations

- Threat intelligence and security alerts should be handled as sensitive operational data.
- API keys, credentials, and other secrets should be stored in environment variables or a secure secrets manager and should never be committed to Git.
- Access to dashboards and threat intelligence data should be restricted to authorised users.
- Input data should be validated and normalised before processing.
- Audit logging should be used to track important system and analyst actions.

## Scalability Notes

The architecture is designed to support high-volume multi-source threat intelligence processing. The proposed platform targets operational environments capable of handling 10,000+ alerts per day without performance degradation.

The modular architecture allows additional threat feeds, sensors, intelligence sources, and processing capabilities to be integrated as the threat landscape evolves.

The phased implementation roadmap starts with the core correlation engine and SIEM connector, followed by sensor and data-collector integration, and finally ML-based filtering and MITRE ATT&CK mapping.