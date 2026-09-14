# 🛡️ Network Honeypot for Attack Detection and Network Traffic Analysis

<p align="center">
  <strong>A Practical Cybersecurity Experiment for Controlled SSH Attack Detection, Network Traffic Analysis and Evidence Correlation</strong>
</p>

---

## 📌 Project Overview

This project implements a practical network honeypot laboratory designed to
observe and analyze controlled suspicious network activity in an isolated
environment.

The laboratory uses:

- 🐉 Kali Linux as the attack/test machine
- 🐧 Ubuntu Server as the honeypot host
- 🪤 Cowrie as the SSH honeypot
- 🔎 Nmap for controlled reconnaissance
- 🦈 Wireshark for packet-level network traffic analysis

Cowrie was configured to provide an SSH honeypot on TCP port `2222`.
The experiment combines Cowrie application/session logs with Wireshark
packet-level evidence to construct a coherent sequence of network activity.

> ⚠️ **Safety Notice:** This project was performed only in an isolated
> academic laboratory using project-owned virtual machines and laboratory
> test credentials. No public or third-party systems were targeted.

---

## 🎯 Aim

To design and experimentally evaluate a network honeypot for detecting and
analyzing controlled SSH-based reconnaissance and interaction.

---

## 🎯 Objectives

- Establish an isolated cybersecurity laboratory
- Configure Kali Linux and Ubuntu Server
- Deploy Cowrie as an SSH honeypot
- Monitor controlled SSH interaction
- Perform controlled Nmap reconnaissance
- Capture network traffic using Wireshark
- Analyze Cowrie text and JSON logs
- Correlate application-level and packet-level evidence
- Document security observations and findings

---

## 🏗️ Experimental Architecture

```text
┌─────────────────────┐
│   Kali Linux        │
│   Attack / Test     │
│                     │
│   Nmap              │
│   SSH Interaction   │
└──────────┬──────────┘
           │
           │ Controlled Network Activity
           ▼
┌─────────────────────┐
│   Ubuntu Server     │
│   Honeypot Host     │
│                     │
│   Cowrie SSH        │
│   TCP / 2222        │
└──────────┬──────────┘
           │
           ├──────────────────────┐
           ▼                      ▼
┌─────────────────────┐   ┌─────────────────────┐
│   Cowrie Logs       │   │   Wireshark         │
│                     │   │                     │
│ Authentication      │   │ TCP Handshake       │
│ Commands            │   │ SSHv2 Negotiation   │
│ Sessions             │   │ Encrypted Traffic   │
│ Source IP            │   │ Network Details    │
└──────────┬──────────┘   └──────────┬──────────┘
           │                         │
           └──────────┬──────────────┘
                      ▼
             ┌─────────────────┐
             │ Evidence        │
             │ Correlation     │
             │                 │
             │ Attack Timeline │
             │ Security        │
             │ Findings        │
             └─────────────────┘

🌐 Laboratory Network
 | Component     | Role                     |
| ------------- | ------------------------ |
| Kali Linux    | Attack/Test Machine      |
| Ubuntu Server | Honeypot Host            |
| Cowrie        | SSH Honeypot             |
| Nmap          | Network Reconnaissance   |
| Wireshark     | Network Traffic Analysis |
| VirtualBox    | Virtualization Platform  |


Lab Configuration
| Component           | Address / Configuration |
| ------------------- | ----------------------- |
| Kali Linux          | `10.208.147.204`        |
| Ubuntu Honeypot     | `10.208.147.139`        |
| Private Lab Network | `10.208.147.0/24`       |
| Cowrie SSH Listener | TCP `2222`              |
| Wireshark Interface | `eth0`                  |


🧰 Tools & Technologies
| Tool / Technology | Purpose                                       |
| ----------------- | --------------------------------------------- |
| 🖥️ VirtualBox    | Isolated virtual laboratory                   |
| 🐉 Kali Linux     | Controlled reconnaissance and SSH interaction |
| 🐧 Ubuntu Server  | Honeypot host                                 |
| 🪤 Cowrie         | Medium-interaction SSH/Telnet honeypot        |
| 🔎 Nmap           | Network and service reconnaissance            |
| 🦈 Wireshark      | Packet capture and traffic analysis           |
| 🐍 Python 3       | Cowrie runtime environment                    |
| 🐚 Linux Shell    | System and evidence collection                |


🔍 Attack / Activity Sequence

Reconnaissance
      ↓
TCP Connection to 2222
      ↓
TCP Three-Way Handshake
      ↓
SSHv2 Negotiation
      ↓
Key Exchange
      ↓
Authentication
      ↓
Interactive Commands
      ↓
Session Termination

📊 Evidence Correlation

             ┌──────────────────┐
             │      Nmap        │
             │  Reconnaissance  │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │     Cowrie       │
             │ Application /    │
             │ Session Evidence │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │    Wireshark     │
             │ Packet Evidence  │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Event Correlation│
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Security Findings│
             └──────────────────┘

📸 Project Evidence

Screenshots from the practical experiment will be organized here.

🖥️ Lab Environment

🪤 Cowrie Honeypot

🔐 Controlled SSH Interaction

🔎 Nmap Reconnaissance

🦈 Wireshark Traffic Analysis

📊 Log Analysis

🏗️ Experimental Architecture


🧪 Testing

The project was evaluated through controlled laboratory scenarios:

- Network connectivity testing
- Honeypot reachability testing
- SSH service verification
- Controlled SSH interaction
- Nmap reconnaissance
- Packet capture
- Log analysis
- Evidence correlation
All testing was restricted to the isolated academic laboratory.

📖 What I Learned

Through this project, I gained practical experience in:
- Network security
- Honeypot deployment
- SSH monitoring
- Network reconnaissance
- Packet capture
- Network traffic analysis
- Log analysis
- Event correlation
- Security evidence collection
- Attack-sequence analysis
- Linux administration
- Practical cybersecurity experimentation

⭐ Project Summary

Network Honeypot for Attack Detection and Network Traffic Analysis

A controlled cybersecurity laboratory demonstrating how honeypot-based
SSH monitoring, network reconnaissance, packet analysis and log correlation
can be combined to investigate suspicious network activity.
