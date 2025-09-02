# Simple Botnet & Havoc C2 Lab

> ⚠️ Disclaimer: This project was developed **for academic purposes only** as part of the "Malware Mechanisms" course at UIT (University of Information Technology, VNUHCM).  
> All experiments were conducted in a **controlled lab environment**. Do not use any part of this project in real-world systems.

## 📌 Overview
This lab demonstrates how a simple botnet and a modern C2 (Command & Control) framework operate.  
The project consists of two main parts:
1. **Simple Botnet (Python)** – building a custom C2 server and bot agents communicating over TCP sockets.  
2. **Havoc C2 Framework** – deploying a red-team C2 platform to simulate advanced attacker techniques, payload generation, and EDR bypass.  

Through this lab, we practiced both **offensive** and **defensive** security concepts, including attack simulation, traffic analysis, and detection evasion.

## 🛠️ Features
- **Custom Botnet**
  - Implemented C2 server (`cnc.py`) and multiple bot clients (`bot.pyw`).
  - Supported basic commands (DDoS flood, UDP/TCP packets, HTTP requests).
  - Used `PING/PONG` keep-alive mechanism for bot health monitoring.

- **Havoc C2**
  - Deployed Havoc Teamserver, Client, and Demon agents.
  - Generated payloads (EXE, DLL, shellcode) with obfuscation techniques:
    - Indirect Syscalls
    - Stack Duplication
    - Sleep Obfuscation
    - AMSI & ETW patch
  - Configured **Domain Fronting** with AWS/Cloudflare for covert traffic.

- **Exploit Simulation**
  - Integrated EternalBlue exploit (`ms17_010`) into custom Havoc agent (Talon).
  - Demonstrated lateral movement and propagation across vulnerable hosts.

- **Traffic Analysis**
  - Captured botnet and C2 communication with **Wireshark**.
  - Identified encrypted traffic patterns, heartbeat packets, and task execution.
  - Stored analysis in `.pcapng` files.

## 🖥️ Lab Environment
- **Operating Systems**: Kali Linux, Windows 10, Windows 7 VM
- **Tools**: Python 3.10, Havoc Framework, Wireshark, VMware/VirtualBox
- **Network Setup**: Isolated virtual network with multiple VMs for attacker, C2 server, and victim machines.

## 📚 Learning Outcomes
- Understand the architecture of botnets and modern C2 frameworks.
- Gain hands-on experience with exploit payloads, AV/EDR evasion, and persistence techniques.
- Improve network forensics skills by analyzing C2 traffic.
- Balance both **red team (attack)** and **blue team (defense)** perspectives.

## 🚀 Usage
This repository contains:
- Source code for simple botnet (server & bots).
- Configuration scripts for Havoc framework setup.
- Documentation and lab report (PDF).  

To reproduce the lab:
1. Set up isolated VMs (do not connect to the internet).  
2. Deploy the C2 server and bots.  
3. Run payloads and monitor traffic via Wireshark.  
4. Review captured PCAP files and analysis report.  

---

👨‍💻 Author: **Tran Vy Khang**  
🎓 Course: Cơ chế hoạt động của mã độc – UIT, VNUHCM  
📅 Semester: 2024–2025
