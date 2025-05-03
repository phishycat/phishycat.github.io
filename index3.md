---
layout: default
title: SoC Home Lab: Defensive Simulation with Azure & Microsoft Sentinel
---

# SoC Home Lab: Defensive Simulation with Azure & Microsoft Sentinel

**Project Type:** Security Operations / Threat Detection & Response  
**Tools Used:** Microsoft Azure, Microsoft Defender for Endpoint, Microsoft Sentinel, MISP (Malware Information Sharing Platform)  
**Status:** In Progress  
**Tags:** `SoC`, `Microsoft Sentinel`, `Threat Intelligence`, `Defensive Security`, `SIEM`, `XDR`

---

## Project Overview

This project focuses on building a functional Security Operations Center (SoC) simulation within a home lab environment. The lab integrates Microsoft Azure’s security ecosystem with open-source threat intelligence sharing platforms to simulate real-world detection, investigation, and response scenarios.

The goal is to replicate the foundational capabilities of a modern SoC—using Microsoft Defender and Sentinel for telemetry and alerting, and MISP to enrich threat data with actionable intelligence.

---

## Objectives

- Establish a centralized detection and response environment using Microsoft Sentinel.
- Simulate common attack techniques (e.g., credential theft, lateral movement) to validate alert fidelity.
- Integrate MISP to enhance threat triage and analysis workflows.
- Explore the end-to-end lifecycle of incident response in a cloud-native security environment.

---

## Lab Architecture

The lab is designed to mirror a hybrid enterprise infrastructure and includes the following components:

- **Azure Active Directory (AAD):** Identity and access management for simulated users and services.
- **Windows 10/11 and Windows Server VMs:** Endpoint telemetry and attack surface simulation.
- **Microsoft Defender for Endpoint:** Provides EDR capabilities and feeds into Sentinel.
- **Microsoft Sentinel:** Serves as the SIEM/XDR platform, ingesting data from Defender, AAD, and other sources.
- **MISP Threat Intelligence Platform:** Installed on a local VM and connected to Sentinel for contextual enrichment of IOCs.

---

## Key Activities

1. **Deployment and Configuration**
   - Deployed Defender for Endpoint on virtual machines.
   - Connected Defender and AAD logs to Sentinel via data connectors.
   - Installed and configured MISP on Ubuntu Server and set up feeds.

2. **Telemetry and Log Collection**
   - Simulated user activity, suspicious behavior, and baseline operations.
   - Verified Defender alerts for lateral movement, PowerShell abuse, and credential access.
   - Ingested logs from Windows Event Forwarding and Azure Security Center.

3. **Detection Engineering**
   - Created custom Sentinel analytics rules for:
     - Unusual login locations
     - Suspicious command execution
     - Persistence via scheduled tasks

4. **Threat Intelligence Integration**
   - Ingested MISP feeds into Sentinel using a Python connector.
   - Enriched alerts with contextual data (threat actors, TTPs, malware families).

5. **Incident Response Simulation**
   - Used Sentinel Playbooks (Logic Apps) to automate responses (email alerts, device isolation).
   - Performed root cause analysis on simulated breaches.
   - Documented detection gaps and rule tuning process.

---

## Lessons Learned

- Gained hands-on experience configuring Microsoft Sentinel in a cloud-native lab environment.
- Learned how Defender integrates with Sentinel for multi-source detection correlation.
- Improved understanding of threat intelligence lifecycle and its operational value when triaged through a SIEM.
- Identified practical trade-offs between alert volume, noise reduction, and detection coverage.

---

## Next Steps

- Expand environment with Linux endpoints and cloud IaaS services to test cross-platform visibility.
- Incorporate MITRE ATT&CK tagging within Sentinel for coverage mapping.
- Build dashboards to visualize SoC metrics such as Mean Time to Detect (MTTD) and Mean Time to Respond (MTTR).
- Begin integrating honeypot telemetry and endpoint deception techniques into Sentinel ingestion pipeline.

---

## Ethical Considerations

All threat simulations were performed in an isolated lab environment using intentionally vulnerable or controlled systems. No live or production networks were involved. This project is intended purely for educational and professional development purposes.

---

## Resources and References

- [Microsoft Sentinel Documentation](https://learn.microsoft.com/en-us/azure/sentinel/)
- [Microsoft Defender for Endpoint](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/)
- [MISP Project](https://www.misp-project.org/)
- [Azure Security Center](https://learn.microsoft.com/en-us/azure/security-center/)
- [MITRE ATT&CK Framework](https://attack.mitre.org/)

