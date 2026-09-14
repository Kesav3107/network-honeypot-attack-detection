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
