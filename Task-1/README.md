# Task 1 - Network Discovery and Scanning

Hello there 👋

## 📌 Task Overview

This is **Task 1** from my internship at **Elevate Labs**.  
The objective was to discover active hosts on my local network and identify open ports using `nmap`.

---

## ✅ Steps I Followed

I completed this task by following the steps below:

1. **Operating System Used**: Kali Linux (which comes with `nmap` pre-installed).
2. **Checked My Subnet**:
   - Used the command: `ifconfig`  
   - Found my IP and subnet (e.g., `192.168.46.0/24`)
3. **Performed Nmap Scan**:
   - Used this command:
     ```bash
     nmap -sS -sC -sV -T4 -p- 192.168.46.0/24
     ```
   - Explanation of flags:
     - `-sS`: SYN scan
     - `-sC`: Run default scripts
     - `-sV`: Detect service version
     - `-p-`: Scan all 65535 ports
     - `-T4`: Speed up the scan

---

## 💻 Findings

- **Live Hosts Detected**:  
  `192.168.46.39`, `192.168.46.101`, `192.168.46.102`, `192.168.46.234`

- **Open Ports**:
  - `192.168.46.101`:
    - `53/tcp` – `dnsmasq 2.51` *(VULNERABLE)*
  - `192.168.46.102`:
    - `7680/tcp` – Unknown service (`pando-pub?`)
  - `192.168.46.39`:
    - `7680/tcp` – Unknown service (`pando-pub?`)

> All findings are saved in `summary1.txt` and `Task1.txt` files.

---

## 🛠️ Tools Used

- `nmap`
- Kali Linux terminal
- `ifconfig` to find IP and subnet

---

## 📚 What I Learned

- How to identify the subnet using `ifconfig`
- How to perform a full TCP port scan using `nmap`
- Use of different `nmap` flags (`-sS`, `-sC`, `-sV`, `-p-`)
- How to interpret scan results and identify vulnerable services
- Improved my understanding of network scanning and recon phase in penetration testing

---

## 📄 Files Included

- `Task 1.pdf`: Task description provided by Elevate Labs
- `summary1.txt`: Summary of open ports and live hosts
- `Task1.txt`: Full `nmap` scan output

---

✅ *This completes Task 1.*
