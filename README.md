

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
| 📸 **Lab Execution Screenshot** | *Captured from terminal* | ![Linux Log Analysis](./Linux%20Log%20Analysis%20&%20User%20Auditing%20Lab%20Docu.png) <img width="942" height="422" alt="linux-log-analysis-user-auditing" src="https://github.com/user-attachments/assets/3c345873-10b9-490d-879c-5ebc1feb76a6" />
| • Evidence-based reporting & verification. |

---

## 💡 Quick Command Reference
* `cd` - Change directory (Navigating absolute and relative paths).
* `ls` - List directory contents (Discovering files and folders).
* `cat` - Concatenate (Displaying entire text file content).
* `head` - Top lines extractor (Viewing the first 10 rows of a file to save analytical time).

# Linux File Management and Log Analysis Lab

## 🎯 Objective
The objective of this lab is to practice navigating the Linux file system, inspecting user reports, and analyzing system log files using core CLI tools (`cd`, `ls`, `grep`, and `|`).

---

## 💻 Lab Steps & Execution Reference

| Step | Objective | Command Executed | Key Outputs / Insights |
| :--- | :--- | :--- | :--- |
| **1** | Navigate to logs directory and analyze server logs | `cd logs`<br>`grep error server_logs.txt` | Identified multiple critical errors including:<br>• `The password is incorrect`<br>• `The username is incorrect`<br>• `Unauthorized access` |
| **2** | Change directory to user reports | `cd /home/analyst/reports/users` | Successfully moved to the targeted directory for quarter reports. |
| **3** | Filter files for the first quarter (Q1) | `ls \| grep Q1` | Isolated Q1 files:<br>• `Q1_access.txt`<br>• `Q1_added_users.txt`<br>• `Q1_deleted_users.txt` |
| **4** | Filter all access logs across all quarters | `ls \| grep access` | Successfully isolated access reports for all quarters (`Q1_access.txt` through `Q4_access.txt`). |
| **5** | List all files in the current directory | `ls` | Displayed the complete structure of all quarterly text files (`added_users`, `deleted_users`, `access`). |
| **6** | Audit a specific deleted user | `grep jhill Q2_deleted_users.txt` | Found user **jhill** (ID: `1025`) under the `Sales` department. |
| **7** | Filter new additions by department | `grep "Human Resources" Q4_added_users.txt` | Extracted HR personnel added in Q4:<br>• `1151 sshah Human Resources`<br>• `1145 msosa Human Resources` |

---

## 🛠️ Extracted Log Data Summaries

### 🔍 Server Log Security Events (`server_logs.txt`)
| Timestamp | Event Type | Description / Message |
| :--- | :--- | :--- |
| `2022-09-28 13:56:22` | `error` | The password is incorrect |
| `2022-09-28 15:56:22` | `error` | The username is incorrect |
| `2022-09-28 16:56:22` | `error` | The password is incorrect |
| `2022-09-29 13:56:22` | `error` | An unexpected error occurred |
| `2022-09-29 15:56:22` | `error` | Unauthorized access |
| `2022-09-29 16:56:22` | `error` | Unauthorized access |

### 👥 Targeted User Queries
| Target Query | Source File | Extracted Record Details |
| :--- | :--- | :--- |
| `jhill` | `Q2_deleted_users.txt` | `1025   jhill   Sales` |
| `"Human Resources"` | `Q4_added_users.txt` | `1151   sshah   Human Resources`<br>`1145   msosa   Human Resources` |

---

## 🚀 Skills Demonstrated
* **Log Analysis & Threat Hunting:** Filtering system events to detect unauthorized access and authentication failures.
* **Data Filtering & Pipeline Usage:** Employing pipes (`|`) and `grep` regex targeting to parse unstructured text files rapidly.
* **System Administration:** Efficient navigation and directory mapping via the Linux CLI.

 # Linux File and Directory Management Lab

## Overview
This practical lab demonstrates essential Linux command-line operations for managing files and directories. The tasks include creating, moving, listing, and deleting files and directories within a Linux environment, simulated as an IT Security Analyst.

## Objectives
* Create and remove directories to maintain an organized file system.
* Navigate between absolute and relative directory paths.
* Move and manage report files across folders.
* Create and delete temporary documentation files securely.

## Commands Used
* `mkdir`: Create a new directory.
* `rmdir`: Remove an empty directory.
* `ls`: List directory contents.
* `cd`: Change the current working directory.
* `mv`: Move or rename files and directories.
* `rm`: Remove files.
* `touch`: Create a new empty file.

---

## Lab Walkthrough & Execution

| Step | Description | Commands Executed |
| :---: | :--- | :--- |
| **1** | **Directory Creation & Cleanup:**<br>Initialized a new directory named `logs` for structured log management, listed the directory layout, and removed an unneeded temporary empty directory named `temp`. | `mkdir logs`<br>`ls`<br>`rmdir temp`<br>`ls` |
| **2** | **Navigation & File Relocation:**<br>Navigated to the notes directory using the absolute path `/home/analyst/notes`. Moved the quarterly patch report `Q3patches.txt` into the designated `reports` folder. | `cd /home/analyst/notes`<br>`mv Q3patches.txt /home/analyst/reports/`<br>`ls`<br>`ls /home/analyst/reports` |
| **3** | **File Cleanup & Task Initialization:**<br>Permanently deleted the stale temporary note file `tempnotes.txt`, and initialized a fresh tracking file named `tasks.txt` to log upcoming duties. | `rm tempnotes.txt`<br>`ls`<br>`touch tasks.txt`<br>`ls` |<img width="1920" height="889" alt="Linux File and Directory Management" src="https://github.com/user-attachments/assets/f7c0ea95-5e18-4692-aced-f3bba865526c" />

---

## Lab Proof & Verification

### Terminal Evidence
Below is the terminal capture verifying that all file management workflows, directory structures, and system cleanup commands were completed successfully without errors:

![Linux Lab Screenshot](lab-terminal.png)
