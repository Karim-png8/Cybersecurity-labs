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

# Linux APT Commands Guide

This repository contains a reference guide for managing network security tools using the **APT (Advanced Package Tool)** package manager in Linux.

---

## 📋 Table of Contents
1. [Suricata Commands](#1-suricata-commands)
2. [Tcpdump Commands](#2-tcpdump-commands)
3. [Package Verification](#3-package-verification)
4. [External References](#4-external-references)
### 📁 Full Lab Report & Walkthrough
* 📄 **[Click here to view the complete step-by-step Lab PDF](https://drive.google.com/file/d/1F6mIYlCDk2ctzzdinGAfIPDyiOfYOhxP/view?usp=drivesdk)*

# 📑 Linux Log Analysis & User Auditing Lab Documentation

This repository documents my hands-on experience in navigating the Linux CLI, auditing user permissions, and analyzing server logs for potential security alerts.

## 🛠️ Detailed Lab Tasks & Command Execution

| Task / Objective | Commands Executed | Key Findings & Outputs | Skills Mastered |
| :--- | :--- | :--- | :--- |
| **1. User Directory Auditing**<br>Inspect newly added users and map them to their correct corporate departments. | `cd /home/analyst/reports/users`<br>`ls`<br>`cat Q1_added_users.txt` | • Successfully displayed a structured table of Q1 added users.<br>• Identified critical fields: `employee_id`, `username`, and `department`. | • Linux file system navigation.<br>• Full-text file extraction using `cat`. |
| **2. Server Log Analysis**<br>Inspect log files to identify active system events, warnings, and error messages. | `cd /home/analyst/logs`<br>`ls`<br>`head server_logs.txt` | • Extracted the top lines of `server_logs.txt`.<br>• Discovered regular `info` messages alongside `error` alerts.<br>• Identified `warning` messages regarding disk storage. | • Log review & Incident analysis.<br>• Sifting through large log files efficiently using `head`. |
| 📸 **Lab Execution Screenshot** | *Captured from terminal* | ![Linux Log Analysis](./Linux%20Log%20Analysis%20&%20User%20Auditing%20Lab%20Docu.png) | • Evidence-based reporting & verification. |

---

## 💡 Quick Command Reference
* `cd` - Change directory (Navigating absolute and relative paths).
* `ls` - List directory contents (Discovering files and folders).
* `cat` - Concatenate (Displaying entire text file content).
* `head` - Top lines extractor (Viewing the first 10 rows of a file to save analytical time).
*
