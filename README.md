# Metasploitable2 Vulnerability Assessment

A structured vulnerability assessment conducted on a **Metasploitable 2** virtual machine, simulating a real-world security audit of a legacy system acquired by a fictional financial institution — **XYZ Financial Services**.

This project documents the full assessment process using industry-standard tools and frameworks, and is intended as both a learning resource and a professional reference for cybersecurity practitioners.

---

## 🎯 Objective

To identify, validate, and document security vulnerabilities in a legacy system, assess their risk levels, and recommend mitigations aligned with the **CIS Critical Security Controls (CIS Controls v8.1)**.

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| **Nmap** | Network enumeration and service discovery |
| **Nessus Essentials** | Automated vulnerability scanning |
| **FTP Client** | Manual validation of anonymous FTP access |
| **SSH Client** | Manual validation of weak SSH configuration |
| **psql** | Manual validation of default PostgreSQL credentials |
| **showmount** | NFS export enumeration |
| **iptables** | Firewall configuration review |

---

## 🖥️ Environment

| Component | Details |
|---|---|
| **Attacker Machine** | Kali Linux (192.168.56.102) |
| **Target Machine** | Metasploitable 2 (192.168.56.103) |
| **Network Type** | VirtualBox Host-Only Adapter |
| **Target OS** | Ubuntu 8.04 (End of Life) |

---

## 📁 Repository Structure

metasploitable2-assessment/

│

├── README.md                        # Project overview (this file)

├── report/

│   └── vulnerability-report.md     # Full formal vulnerability report

├── walkthrough/

│   ├── 01-setup.md                  # VM setup & network configuration

│   ├── 02-reconnaissance.md         # Nmap scan & asset discovery

│   ├── 03-nessus-scan.md           # Nessus setup & scan results

│   ├── 04-manual-validation.md      # Manual validation of findings

│   ├── 05-logging-firewall.md       # Logging & firewall review

│   └── 06-recommendations.md       # CIS Controls-based mitigations

└── screenshots/

└── README.md                    # Screenshot guide


---

## 🔍 Key Findings Summary

| Severity | Count | Examples |
|---|---|---|
| 🔴 Critical | 5 | Bind Shell Backdoor, VNC default password, SSL v2/v3 |
| 🟠 High | 3 | NFS world-readable, rlogin, Samba Badlock |
| 🟡 Medium | 4 | Unencrypted Telnet, TLS 1.0, SSL DROWN |
| 🟡 Low | 3 | Weak DH keys, X Server, ICMP disclosure |
| 🔵 Info | 55 | Service detections, multiple grouped issues |

---

## 📋 Compliance Framework

All recommendations are mapped to the **CIS Critical Security Controls v8.1**:
- CIS Control 2 — Inventory and Control of Software Assets
- CIS Control 4 — Secure Configuration for Assets
- CIS Control 6 — Access Control Management
- CIS Control 7 — Continuous Vulnerability Management
- CIS Control 8 — Audit Log Management

---

## ⚠️ Disclaimer

This assessment was conducted in a **controlled lab environment** using intentionally vulnerable software. All findings are documented for **educational purposes only**. Never perform security assessments on systems you do not own or have explicit written permission to test.

---

## 📄 Full Report

👉 [View the Full Vulnerability Report](report/vulnerability-report.md)

---

## 👤 Author

**[EUGEN-NYONGESA](https://github.com/EUGEN-NYONGESA)**  
Cybersecurity Analyst | Full-Stack Developer