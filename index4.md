---
layout: default
title: Network Attached Storage Server with Docker for Security Lab Environments
---

# Network Attached Storage Server with Docker for Security Lab Environments

**Project Type:** NAS / Containerization / Security Lab  
**Tools Used:** TrueNAS SCALE, Docker, Kali Linux, Docker Scout, Vulnerable Machines (DVWA, Metasploitable)  
**Status:** Completed  
**Tags:** `NAS`, `Docker`, `Self-Hosted`, `Kali Linux`, `CTF`, `Cybersecurity`, `Infrastructure`

---

## Project Overview

This project focuses on transforming a dedicated machine into a **Network Attached Storage (NAS) server** running **Docker containers** for self-hosted security tools, training environments, and vulnerable instances. The system serves as a centralized resource for learning, experimentation, and secure file storage within a home lab setting.

By combining **TrueNAS SCALE** with **Docker**, I created an efficient, modular infrastructure that supports multiple containerized tools such as Kali Linux, Docker Scout, and purposefully vulnerable applications like DVWA and Metasploitable.

---

## Objectives

- Deploy a stable and expandable NAS server using TrueNAS SCALE.
- Host isolated, reproducible Docker environments for security experimentation.
- Enable on-demand access to tools like Kali Linux for penetration testing.
- Support persistent storage, logs, and datasets within the NAS for long-term use.
- Provide a secure space for developing, analyzing, and testing Dockerfiles and custom configurations.

---

## Hardware & Software

- **Base System:** Repurposed gaming PC (1TB SSD, 16GB RAM, AMD CPU)
- **OS:** TrueNAS SCALE (Debian-based NAS operating system with native Docker & Kubernetes support)
- **Docker Containers Hosted:**
  - Kali Linux (CLI and GUI access)
  - DVWA (Damn Vulnerable Web App)
  - Metasploitable 2
  - Docker Scout (for image analysis and vulnerability scanning)
  - Custom containers built from personal Dockerfiles

---

## Features & Configuration

- **Docker Integration:** Managed through TrueNAS SCALE’s native Apps interface and CLI for full container lifecycle control.
- **Data Volumes:** Persistent volumes mapped to the NAS storage pool for tools, logs, and vulnerable machine states.
- **Networking:** Isolated virtual bridges for inter-container communication; restricted outbound traffic for vulnerable containers.
- **Access:** SSH-enabled Kali container with GUI access via RDP/VNC; reverse proxy available for HTTP-based apps.
- **Resource Allocation:** Fine-tuned CPU and RAM limits to prevent container sprawl from affecting NAS performance.

---

## Use Cases

- **Penetration Testing Labs:** Use Kali + DVWA + Metasploitable to replicate common attack chains and practice exploits.
- **Image Vulnerability Analysis:** Run Docker Scout to audit base images and identify vulnerable packages in Dockerfiles.
- **Custom Image Development:** Build and test hardened container environments for deployment in other parts of my homelab.
- **Backup and Archive:** Secure, centralized storage for Pwnagotchi logs, PCAPs, screenshots, and research documentation.

---

## Lessons Learned

- Gained experience in managing Docker containers at scale with persistent storage and network isolation.
- Learned how to configure and optimize TrueNAS for mixed workloads (file storage + compute).
- Improved understanding of system resource allocation and security boundaries in containerized environments.
- Explored vulnerability scanning workflows using Docker Scout and other automated tools.

---

## Future Improvements

- Implement access control with Vaultwarden and 2FA for sensitive services.
- Integrate Grafana + Prometheus for system monitoring and container health metrics.
- Expand Kubernetes use to test container orchestration across workloads.
- Add ZFS snapshots and automated backup workflows for disaster recovery.

---

## Ethical Considerations

All vulnerable machine deployments are contained within a private, air-gapped network. No live systems were targeted. This project is for educational and research purposes only.

---

## References

- [TrueNAS SCALE Documentation](https://www.truenas.com/docs/scale/)
- [Docker Documentation](https://docs.docker.com/)
- [Kali Linux Docker Hub](https://hub.docker.com/r/kalilinux/kali-linux-docker)
- [Docker Scout Overview](https://docs.docker.com/scout/)
- [DVWA GitHub](https://github.com/digininja/DVWA)

