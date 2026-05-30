


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
| **3** | **File Cleanup & Task Initialization:**<br>Permanently deleted the stale temporary note file `tempnotes.txt`, and initialized a fresh tracking file named `tasks.txt` to log upcoming duties. | `rm tempnotes.txt`<br>`ls`<br>`touch tasks.txt`<br>`ls` |

---

## Lab Proof & Verification

### Terminal Evidence
Below is the terminal capture verifying that all file management workflows, directory structures, and system cleanup commands were completed successfully without errors:

![Linux Lab Screenshot](lab-terminal.png)<img width="1920" height="889" alt="Linux File and Directory Management" src="https://github.com/user-attachments/assets/f7c0ea95-5e18-4692-aced-f3bba865526c" />

# Linux File Permissions & Access Control Lab

## Overview
This lab demonstrates how to manage and audit file and directory permissions in a Linux environment using the `chmod` command. The objective was to secure sensitive project files by restricting unauthorized read, write, and execute access for different user categories (Owner, Group, and Others).

## Lab Objectives
* Analyze existing file permissions using `ls -l` and `ls -la`.
* Modify permissions for specific users, groups, and others using symbolic notation.
* Secure hidden configuration files and directories.

---

## Tasks & Commands Executed

Based on the lab session captured in `0685821a-d46f-464b-9322-a6ae5b40343e`:

### 1. Auditing Directory Contents
* Used `ls -l` to list standard files and `ls -la` to reveal hidden files (like `.project_x.txt`).

### 2. Restricting "Others" Access
* **Command:** `chmod o-w project_k.txt`
* **Purpose:** Removed write (`w`) permission for others (`o`) from `project_k.txt` to prevent unauthorized modifications.

### 3. Restricting "Group" Access
* **Command:** `chmod g-r project_m.txt`
* **Purpose:** Removed read (`r`) permission for the group (`g`) from `project_m.txt` to ensure confidentiality within the team.

### 4. Securing Hidden Files
* **Command:** `chmod u-w,g-w,g+r .project_x.txt`
* **Purpose:** Modified permissions on the hidden file `.project_x.txt` to revoke write access from the owner and group, while ensuring the group has read access.

### 5. Securing Directories
* **Command:** `chmod g-x drafts`
* **Purpose:** Removed execute (`x`) permission from the `drafts` directory for group members, preventing them from entering or traversing the directory.

---

## Skills Learned
* **Linux CLI Navigation:** Efficient use of file listing flags (`-l`, `-a`).
* **Access Control:** Implementing the principle of least privilege by stripping unnecessary permissions.
* **Security Auditing:** Identifying over-permissive files and remediating them instantly.
*<img width="1920" height="1483" alt="Linux File Permissions   Access Control Lab" src="https://github.com/user-attachments/assets/ccbe0f85-eb05-4fcb-93a4-89904c1044ab" />

# Linux User, Group, and Ownership Management Lab

## Overview
This lab focuses on user account administration, group management, and modifying file ownership within a Linux system. Managing these elements is crucial for enforcing security policies, managing privileges, and ensuring proper access control across shared environments.

## Lab Objectives
* Create and delete user accounts securely using administrative privileges (`sudo`).
* Modify user group affiliations (both primary and secondary groups).
* Change file ownership to restrict or grant specific user access.
* Clean up residual groups after user deletion.

---

## Tasks & Commands Executed

Based on the lab session captured in `ecd16ec9-37a3-4339-a721-67a0930e422e`:

### 1. Creating a New User
* **Command:** `sudo useradd researcher9`
* **Purpose:** Created a new standard user account named `researcher9`.

### 2. Managing Group Affiliations
* **Primary Group:** `sudo usermod -g research_team researcher9`
  * *Purpose:* Changed the primary group of `researcher9` to `research_team`.
* **Secondary Group:** `sudo usermod -aG sales_team researcher9`
  * *Purpose:* Appended (`-aG`) the user to a secondary group named `sales_team` without removing them from their primary group.

### 3. Changing File Ownership
* **Command:** `sudo chown researcher9 /home/researcher2/projects/project_r.txt`
* **Purpose:** Transferred the ownership (`chown`) of `project_r.txt` to `researcher9`, granting them owner-level privileges over that specific file.

### 4. User and Group Deletion (Cleanup)
* **Command:** `sudo userdel researcher9`
  * *System Response:* The system notified that the group `researcher9` was not automatically removed because it wasn't the user's primary group at the time of deletion.
* **Command:** `sudo groupdel researcher9`
  * *Purpose:* Manually deleted the residual `researcher9` group to maintain a clean system configuration and avoid orphaned groups.

---

## Skills Learned
* **User Lifecycle Management:** Creating, modifying, and safely deleting user accounts.
* **Access Control & Ownership:** Applying the concept of file ownership (`chown`) to control asset access.
* **System Hygiene:** Handling warnings during user deletion and manually removing leftover groups to prevent configuration drift.
*<img width="1920" height="889" alt="Linux User, Group, and Ownership Management Lab" src="https://github.com/user-attachments/assets/d7d6e507-cd0c-4654-92c6-09b9a7b38673" />

# Linux System Administration & Commands Reference

A comprehensive technical reference documentation for essential Linux commands, configuration files, and system management utilities based on system manual (`man`) pages.

---

## 1. System Documentation & Command Discovery Utilities

These utilities are the primary built-in tools used to navigate system documentation, search for specific commands, or find their purposes directly from the terminal.

### The Core Help Utilities
* **`man`**: The primary interface used to view the system's reference manuals. [span_0](start_span)[span_1](start_span)[span_2](start_span)[span_3](start_span)It provides complete, exhaustive documentation for any command, including syntax, deep descriptions, options, affected files, and exit values[span_0](end_span)[span_1](end_span)[span_2](end_span)[span_3](end_span).
* **[span_4](start_span)`whatis`**: Displays a one-line manual page description to give a quick overview of what a command does[span_4](end_span).
  * *[span_5](start_span)Example*: `whatis cat` outputs "concatenate files and print on the standard output"[span_5](end_span).
* **[span_6](start_span)`apropos`**: Searches the manual page descriptions for specific keywords when the exact command name is unknown[span_6](end_span).
  * *[span_7](start_span)Example*: `apropos a first part file` helps locate the `head (1)` command[span_7](end_span).
  * *[span_8](start_span)Example*: `apropos create new group` helps locate the `groupadd (8)` command[span_8](end_span).

### Quick Comparison Matrix

| Utility | Best Used When... | Expected Output Type |
| :--- | :--- | :--- |
| **`man [command]`** | You know the command but need **full, detailed instructions** and all flags. | [span_9](start_span)A comprehensive, multi-page scrollable manual[span_9](end_span). |
| **`whatis [command]`** | You know the command name but just need a **one-line reminder** of its role. | [span_10](start_span)A single, short descriptive sentence[span_10](end_span). |
| **`apropos [keyword]`** | You **don't know the command name** and want to search by its meaning/action. | [span_11](start_span)[span_12](start_span)A curated list of matching commands and tools[span_11](end_span)[span_12](end_span). |

---

## 2. File & Directory Management

### `cat` — Concatenate files and print on the standard output
* **[span_13](start_span)Synopsis**: `cat [OPTION]... [FILE]...`[span_13](end_span)
* **[span_14](start_span)Description**: Concatenates file(s) to standard output[span_14](end_span). [span_15](start_span)If no file is specified, it reads from the standard input[span_15](end_span).
* **Key Options**:
  * [span_16](start_span)`-n`, `--number`: Numbers all output lines[span_16](end_span).
  * [span_17](start_span)`-b`, `--number-nonblank`: Numbers nonempty output lines (overrides `-n`)[span_17](end_span).
  * [span_18](start_span)`-e`: Equivalent to `-vE`[span_18](end_span).
  * [span_19](start_span)`-E`, `--show-ends`: Displays a `$` character at the end of each line[span_19](end_span).
  * [span_20](start_span)`-s`, `--squeeze-blank`: Suppresses repeated empty output lines[span_20](end_span).
  * [span_21](start_span)`-t`: Equivalent to `-vT`[span_21](end_span).
  * [span_22](start_span)`-T`, `--show-tabs`: Displays TAB characters as `^I`[span_22](end_span).
  * [span_23](start_span)`-v`, `--show-nonprinting`: Uses `^` and `M-` notation, except for LFD and TAB[span_23](end_span).

### Other Core File Commands
* **[span_24](start_span)`head (1)`**: Outputs the first part of files[span_24](end_span).
* **[span_25](start_span)`rm (1)`**: Removes files or directories[span_25](end_span).
* **[span_26](start_span)`rmdir (1, 2)`**: Removes empty directories or deletes a directory[span_26](end_span).

---

## 3. User & Group Account Management

### `useradd` — Create a new user or update default new user information
* **Synopsis**: 
  * [span_27](start_span)`useradd [options] LOGIN`[span_27](end_span)
  * [span_28](start_span)`useradd -D [options]` (to view or change default values)[span_28](end_span)
* **[span_29](start_span)Description**: A low-level utility for adding users[span_29](end_span). [span_30](start_span)On Debian systems, administrators should usually use `adduser (8)` instead[span_30](end_span).

#### Primary Creation Options:
* [span_31](start_span)[span_32](start_span)`-m`, `--create-home`: Creates the user's home directory if it does not exist, copying initial files from the skeleton directory[span_31](end_span)[span_32](end_span).
* [span_33](start_span)`-M`, `--no-create-home`: Explicitly forces `useradd` not to create the home directory, even if the system-wide setting (`CREATE_HOME`) in `/etc/login.defs` is set to yes[span_33](end_span).
* [span_34](start_span)`-d`, `--home-dir HOME_DIR`: Specifies a custom login directory name[span_34](end_span). [span_35](start_span)[span_36](start_span)The directory does not have to exist and won't be created if it is missing unless combined with `-m`[span_35](end_span)[span_36](end_span).
* [span_37](start_span)`-b`, `--base-dir BASE_DIR`: Defines the default base directory prefix for the system if `HOME_DIR` is not specified (concatenates `BASE_DIR + LOGIN`)[span_37](end_span). [span_38](start_span)Defaults to `/home`[span_38](end_span).
* [span_39](start_span)`-c comment`: Adds a short description or text string, generally used as the field for the user's full name[span_39](end_span).
* [span_40](start_span)`-e EXPIRE_DATE`: The specific date on which the user account will be disabled, formatted as `YYYY-MM-DD`[span_40](end_span).
* [span_41](start_span)`-f INACTIVE`: Number of days after a password expires until the account is permanently disabled (`0` disables immediately, `-1` disables the feature)[span_41](end_span).
* [span_42](start_span)`-g GROUP`: Sets the primary group name or GID for the new user[span_42](end_span).
* [span_43](start_span)`-G GROUP1,GROUP2`: A comma-separated list of supplementary groups that the user is also a member of, with no intervening whitespace[span_43](end_span).
* [span_44](start_span)`-s SHELL`: Defines the name of the user's custom login shell[span_44](end_span).
* [span_45](start_span)`-u UID`: Sets a specific numerical value for the user's ID[span_45](end_span). [span_46](start_span)Must be unique unless combined with the `-o` option[span_46](end_span).
* [span_47](start_span)`-o`, `--non-unique`: Allows the creation of a user account with a duplicate (non-unique) UID (valid only with `-u`)[span_47](end_span).
* [span_48](start_span)`-r`, `--system`: Creates a system account with no password aging information in `/etc/shadow` and assigns a UID within the system range[span_48](end_span).

### `groupadd` — Create a new group
* **[span_49](start_span)Description**: Creates an entirely new group account in the system using the specified configurations[span_49](end_span).

---

## 4. System Files & Configurations Affected

System account management commands read and write to several critical configuration files:

* **[span_50](start_span)`/etc/passwd`**: Stores core user account information[span_50](end_span).
* **[span_51](start_span)`/etc/shadow`**: Holds secure, encrypted user account information and password details[span_51](end_span).
* **[span_52](start_span)`/etc/group`**: Contains group account definitions[span_52](end_span).
* **[span_53](start_span)`/etc/gshadow`**: Holds secure group account details[span_53](end_span).
* **[span_54](start_span)`/etc/default/useradd`**: Stores the system-wide default values used during account creation[span_54](end_span).
* **[span_55](start_span)[span_56](start_span)`/etc/skel/`**: Directory containing default configuration files copied into a new user's home directory when created[span_55](end_span)[span_56](end_span).
* **[span_57](start_span)[span_58](start_span)[span_59](start_span)`/etc/login.defs`**: Configuration file for the shadow password suite, defining properties like UID ranges, home directory permissions, and password aging policies[span_57](end_span)[span_58](end_span)[span_59](end_span).

---

## 5. Command Exit Values (Status Codes)

[span_60](start_span)[span_61](start_span)When executing `useradd`, the tool returns specific exit codes depending on the result[span_60](end_span)[span_61](end_span):
* **[span_62](start_span)`0`**: Success[span_62](end_span)
* **[span_63](start_span)`1`**: Can't update password file[span_63](end_span)
* **[span_64](start_span)`3`**: Invalid argument to option[span_64](end_span)
* **[span_65](start_span)`4`**: UID already in use (and no `-o` provided)[span_65](end_span)
* **[span_66](start_span)`6`**: Username already in use[span_66](end_span)
* **[span_67](start_span)`9`**: Can't update group file[span_67](end_span)
* **[span_68](start_span)`10`**: Can't create home directory[span_68](end_span)
* **[span_69](start_span)`12`**: Can't update SELinux user mapping[span_69](end_span)
*[System Administration & Commands Reference.pdf](https://github.com/user-attachments/files/28429507/System.Administration.Commands.Reference.pdf)
