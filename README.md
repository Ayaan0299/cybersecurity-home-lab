# [![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=800&size=30&duration=1500&pause=1000&color=36BCF7&width=1000&lines=CYBERSECURITY+HOME+LAB+%7C+NETWORK+RECONNAISSANCE;FIREWALL+DEFENSE+%7C+TRAFFIC+ANALYSIS;RED+TEAM+%7C+BLUE+TEAM+OPERATIONS)](https://git.io/typing-svg)

<p align="center">
  <img src="https://img.shields.io/badge/Kali%20Linux-Attacker-red?style=for-the-badge">
  <img src="https://img.shields.io/badge/Ubuntu-Target-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/Wireshark-Packet%20Analysis-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Nmap-Reconnaissance-green?style=for-the-badge">
  <img src="https://img.shields.io/badge/UFW-Firewall-yellow?style=for-the-badge">
</p>

# Cybersecurity Home Lab: Network Reconnaissance, Firewall Defense & Traffic Analysis

## 📑 Table of Contents

- [Overview](#overview)
- [Lab Architecture](#lab-architecture)
- [Setting Up the Environment](#-setting-up-the-environment)
- [Performing Network Scans](#-performing-network-scans)
- [Defending Ubuntu with UFW Firewall](#-defending-ubuntu-with-ufw-firewall)
- [Analyzing Traffic with Wireshark](#-analyzing-traffic-with-wireshark)
- [Skills Developed](#-skills-developed)
- [Key Takeaways](#-key-takeaways)

---

## Overview

I built a cybersecurity home lab to practice both attacking and defending systems.

The lab uses Kali Linux as the attacker and Ubuntu as the target. Both machines run in VirtualBox on a NAT network, creating a safe and isolated environment for security testing without impacting production systems.

<img src="https://github.com/user-attachments/assets/c4fe6943-e5db-4693-884b-c09de8fb7f1c" width="700">

---

## Lab Architecture

```text
┌─────────────────┐
│   Kali Linux    │
│   Attacker VM   │
└────────┬────────┘
         │
         │ NAT Network
         │
┌────────▼────────┐
│     Ubuntu      │
│    Target VM    │
└─────────────────┘

Tools Used:
• Nmap
• Wireshark
• Metasploit
• UFW Firewall
• VirtualBox
```

---

## 🖥 Setting Up the Environment

On Ubuntu, I updated the system and installed essential tools such as:

- build-essential
- git
- curl
- wget

I also identified the VM's IP address using:

```bash
ip a
```

On Kali Linux, I updated the operating system and installed:

- Nmap
- Wireshark
- Metasploit Framework

This created a realistic environment for testing offensive and defensive security techniques.

---

## 🔍 Performing Network Scans

From Kali Linux, I performed reconnaissance using:

```bash
nmap -A <Ubuntu-IP>
```

This identified:

- Open ports
- Running services
- Service versions
- Operating system information

For example, FTP services were identified on open ports.

This phase simulates how attackers gather information before attempting exploitation.

<img src="https://github.com/user-attachments/assets/a5fcfdc0-c32b-4814-aac2-26805f7d82df" width="700">

---

## 🛡 Defending Ubuntu with UFW Firewall

To strengthen the target system, I configured Ubuntu's Uncomplicated Firewall (UFW).

### Security Controls Implemented

- Allowed SSH access
- Restricted access to Kali Linux only
- Blocked unauthorized connections
- Reduced attack surface

Example commands:

```bash
sudo ufw allow ssh
sudo ufw allow from <Kali-IP>
sudo ufw enable
```

This allowed safe testing while maintaining strong network controls.

<img src="https://github.com/user-attachments/assets/ecbabc96-fe8c-4be0-b312-bff36d363de2" width="700">

---

## 📊 Analyzing Traffic with Wireshark

Wireshark was used on Ubuntu to capture and analyze network traffic generated during reconnaissance and testing activities.

Key observations included:

- SYN packets
- SYN-ACK packets
- RST packets
- TCP handshakes
- Connection attempts

This provided insight into how network communication occurs and how security events appear at the packet level.

<img src="https://github.com/user-attachments/assets/2c0fb4d4-d4d8-4224-889d-0d466b695636" width="700">

---

## 🎯 Skills Developed

### Red Team Skills

- Network reconnaissance
- Service enumeration
- Attack surface identification
- Nmap scanning techniques

### Blue Team Skills

- Firewall configuration
- Network monitoring
- Traffic analysis
- Security hardening

### Technical Skills

- Linux administration
- Virtualization
- TCP/IP networking
- Wireshark packet analysis
- Security troubleshooting

---

## 🔑 Key Takeaways

This project provided practical experience in both offensive and defensive cybersecurity operations.

Key lessons learned:

- How attackers gather intelligence during reconnaissance
- How firewalls reduce attack exposure
- How network traffic reveals attack activity
- How packet analysis supports investigations
- How virtualization enables safe cybersecurity testing

The lab strengthened my understanding of networking fundamentals, Linux administration, security monitoring, and defensive controls while providing hands-on experience with industry-standard security tools.
