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
sudo nmap -sS -T4 -Pn -v 127.0.0.1

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

Port	Service	Description	Potential Risk
22	SSH	Secure Shell login	Brute-force attacks if weak credentials; check for auth keys
80	HTTP	Web server	Unpatched web apps can be vulnerable to RCE, XSS, SQLi
631	IPP	Internet Printing Protocol	May leak printer info; rarely needed on production servers
5432	PostgreSQL	Database server	Open DB port can expose data; ensure password enforcement
5900	VNC	Virtual Network Computing	Vulnerable to MITM or brute-force; use encryption/tunneling
6379	Redis	In-memory DB, cache	Redis has no auth by default; should not be exposed

🧪 Disclaimer
This scan was conducted in a controlled local environment for educational and research purposes. Do not scan external networks without proper authorization.
