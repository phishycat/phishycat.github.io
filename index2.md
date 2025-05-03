---
layout: default
title: 🐾 Wi-Fi Security Exploration with Pwnagotchi
---

# 🐾 Wi-Fi Security Exploration with Pwnagotchi

**Project Type:** Wireless Security / Embedded Systems  
**Tools Used:** Pwnagotchi, Raspberry Pi Zero W, hcxdumptool, hashcat, GPS plugin  
**Status:** Ongoing  
**Tags:** `Wi-Fi`, `Security Research`, `Pentesting`, `Reinforcement Learning`

---

## Project Overview

This project explores **Wi-Fi security vulnerabilities** through the lens of a lightweight, AI-powered platform called [Pwnagotchi](https://pwnagotchi.ai/). Inspired by Tamagotchi-style digital pets, the Pwnagotchi uses *Reinforcement Learning* to improve its ability to capture WPA2 handshakes from wireless access points.

My goal was to build one from scratch, use it in a **controlled and ethical lab environment**, and evaluate its potential as a learning tool for real-world wireless security practices.

---

## Why Pwnagotchi?

As a cybersecurity professional in training, I wanted a hands-on way to:

- Understand how **WPA2 handshakes** are transmitted and captured.
- Experiment with **packet injection**, **deauthentication**, and **PMKID capture**.
- Build and debug a small-scale embedded system running Linux.
- Evaluate how automation and AI can be applied to penetration testing workflows.

I also wanted to explore ethical hacking from a responsible perspective — using **only authorized networks** — and document the process for others learning in similar environments.

---

## Hardware & Setup

- **Raspberry Pi Zero W** (with OTG USB hub)
- **Waveshare 2.13” e-ink display**
- **TP-Link TL-WN722N** Wi-Fi adapter (for packet injection)
- **Power source:** 2000mAh LiPo battery + Adafruit PowerBoost 1000C
- **Custom 3D printed enclosure** (optional, STL linked below)

### Software:

- Pwnagotchi v1.5.3 firmware (based on Raspbian Lite)
- Custom plugin for network logging
- `hcxdumptool`, `hcxpcapngtool` for packet conversion
- `hashcat` for post-capture WPA2 cracking (in lab)

---

##  What I Did

All tests were conducted on my own Wi-Fi networks or simulated lab environments.

### Key Experiments:
- **Captured PMKID and 4-way handshakes** using both passive and active scanning.
- **Measured signal quality** and handshake success rates based on device placement and antenna orientation.
- **Logged AP signal strength with GPS plugin** (on mobile test runs).
- **Evaluated learning behavior** over time via the Pwnagotchi UI and logs.
- **Created custom plugin** that logs AP SSIDs with timestamped signal strength to a CSV for offline visualization.

---

##  Results

| Test | Location | Avg. Handshake Time | Capture Rate | Notes |
|------|----------|---------------------|---------------|-------|
| Passive | Home lab | ~3.1 min | High | No interference |
| Active (Deauth) | Simulated env | ~1.5 min | Very High | Confirmed deauth effectiveness |
| Mobile test (carried) | Neighborhood test box | Varies | Moderate | Reflected dynamic AP discovery |

- **Deauthentication + PMKID capture** was more effective on older routers.
- **Antenna position** significantly impacted success rate in noisy 2.4GHz bands.
- **Power consumption** was lower than expected; ~3.5 hours on battery alone.

---

##  What I Learned

- Practical knowledge of **802.11 protocols**, especially handshake mechanics.
- Improved skills in **packet analysis** and **data conversion for hashcat**.
- Debugging embedded Linux systems and managing headless configurations.
- Ethical hacking principles and responsible disclosure guidelines.

---

##  Ethics & Legality

All experiments were run on my own network or in simulated lab conditions. No third-party access points were targeted, and no unauthorized deauthentication or packet sniffing was performed.

I strictly followed the principles of ethical hacking, and this project is documented for educational purposes only.

---

## 📁 Resources

- [Pwnagotchi Documentation](https://pwnagotchi.ai/)
- [hcxdumptool GitHub](https://github.com/ZerBea/hcxdumptool)
- [hashcat WPA2 cracking](https://hashcat.net/wiki/)
- [My Custom Plugin](../assets/plugins/network-logger.py)
- [STL for Enclosure](../assets/case/pwnagotchi_case_v2.stl)

---

## 🚀 What's Next
