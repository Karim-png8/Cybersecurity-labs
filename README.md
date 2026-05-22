# 🛡️ Cybersecurity Labs

Welcome to my labs repository! Here, I document my hands-on experiments, network analysis, and security room walkthroughs that I perform myself.

## 📁 Repository Sections:
* **Network Security & Traffic Analysis:** Packet analysis labs using Wireshark and tcpdump.
* **TryHackMe Writeups:** Documentation and step-by-step solutions for security rooms (Defensive Operations).
* **Operating Systems & Tools:** Notes and summaries of Kali Linux commands and system security.
---

## 💻 Linux Command Line Interface (CLI) Basics Lab

This lab demonstrates foundational Linux commands executed via the terminal, focusing on text output, arithmetic evaluation, and environment management.

### Lab Screenshot
![Linux CLI Basics](./linux-cli-basics.png)

### 🛠️ Executed Commands Summary

| Command | Usage in Lab | Description | Output |
| :--- | :--- | :--- | :--- |
| **`echo`** | `echo hello` / `echo "Your karim"` | Prints the provided string or text to the standard output. | `hello` / `Your karim` |
| **`expr`** | `expr 32 - 8` | Evaluates arguments as an expression (Subtraction). | `24` |
| **`expr`** | `expr 3500 \* 12` | Evaluates arguments as an expression (Multiplication). | `42000` |
| **`clear`** | `clear` | Clears the terminal screen for a clean workspace. | *Clears Terminal* |
---

## 🛡️ 3. Linux Package Management & Network Security Lab (Suricata IDS/IPS)

In this security lab, I focused on advanced Linux package administration, system auditing, and deploying network security monitoring solutions using **Suricata** (Intrusion Detection and Prevention System).

### 🛠️ Detailed Tasks & System Auditing

#### 1. Advanced Package Queries via `apt`
* Used `apt list --installed` and `apt search` to audit security tools within the system.
* Executed detailed queries using `apt show` to verify package versions, maintainer logs, and source repositories before execution.

#### 2. Installing Suricata & Deploying Dependencies
* Installed the **Suricata** engine via elevated privileges to set up real-time packet capturing and threat detection:
  ```bash
  sudo apt-get update && sudo apt-get install suricata -y ### 📂 Full Lab Report & Walkthrough
* 📄 **[Click here to view the complete step-by-step Lab PDF](https://drive.google.com/file/d/1F6mIYlCDk2ctzzdinGAfIPDyiOfYOhxP/view?usp=drivesdk)**
