# 🔍 Nmap TCP SYN Scan on Localhost

This repository contains the results and analysis of an `nmap` scan conducted on the localhost IP address. The primary objective of this scan is to identify open TCP ports using a **TCP SYN scan**, and assess potential security risks associated with the exposed services.

---

## 📌 Table of Contents

- [About the Project](#about-the-project)
- [Scan Command Used](#scan-command-used)
- [Scan Results](#scan-results)
- [Security Risk Analysis](#security-risk-analysis)

---

## ✅ About the Project

**Nmap (Network Mapper)** is an open-source tool for network exploration and security auditing. This project focuses on scanning the localhost using the TCP SYN scan (`-sS`), which is known for being stealthy and effective in identifying open ports without establishing a full TCP connection.

---

## ⚙️ Prerequisites

- Operating System: Linux
- Nmap version 7.90 or higher recommended
sudo nmap -sS -T4 -Pn -v 10.81.197.101

  10.81.197.101	Target IP (localhost)

📄 Scan Results (Example Output)
text
Starting Nmap 7.94 ( https://nmap.org ) at 2025-08-04 10:00 UTC
Nmap scan report for localhost (10.81.197.101/24)
Host is up (0.00013s latency).
Not shown: 994 closed ports
PORT     STATE SERVICE
53/tcp   open  DOMAIN

🔐 Security Risk Analysis

Oldest version of dnsmasq like 2.45 may have vulnerablties. Attackers may exploit these to:
	- Perform DNS cache poisoning
	- Execute remote code
	- Leak system information
	- If port 53 is exposed to the public internet, it increases the risk.

COMMAN OPEN PORT RISK ANALYSIS:
	 - Someone might get in without permission ( unauthorized access )
	 - You might be giving away info without realising it like ( sensitive data's )
	 - Old or Weak software might be running if a service on a open port hasn't update properly
it might be exposed easily by the attackers


🧪 Disclaimer:

This scan was conducted in a controlled local environment for educational and research purposes. Do not scan external networks without proper authorization.
