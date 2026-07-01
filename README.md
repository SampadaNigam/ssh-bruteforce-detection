# 🛡️ Enterprise Security Monitoring: Automated SSH Brute-Force Detection Lab
An end-to-end cyber defense engineering project demonstrating log ingestion, parsing infrastructure, real-time brute-force threat detection, and incident analysis using Splunk Enterprise and Linux Linux PAM (`auth.log`) ecosystems.

---

## 📌 Project Overview
This project simulates an adversarial authentication attack vector (Brute-Force / Credential Stuffing) inside an enterprise infrastructure. It demonstrates how a Security Analyst configures centralized log forwarding, processes unstructured system authentication logs, and builds targeted alerting frameworks to intercept active identity-based threats.

* **Target Objective:** Track, isolate, and alert on multi-threaded automated credential attacks before system compromise.
* **Core Framework:** Aligned with **MITRE ATT&CK Matrix T1110 (Brute Force)**.

---

## 🏗️ Architectural Topology & Environment
The deployment utilizes an isolated hypervisor network topology configured via static IP allocations and local network management engines (`Netplan`/`nmcli`).

* **SIEM Core & Ingestion Target:** Ubuntu Server Core running Splunk Enterprise (Centralized Indexer & Forwarding Engine)
* **Identity Audit Log Provider:** Linux Pluggable Authentication Modules (`PAM` framework pushing to `/var/log/auth.log`)
* **Adversarial Emulator:** Kali Linux (Utilizing high-speed parallel login tools via the `Hydra` automation framework)
* **Attack Payload Matrix:** Standard industry-grade dictionary matrices (`RockYou` wordlist payload)

---

## 📁 Repository Directory Structure

```text
├── setup/             
├── attack-simulation/   
├── splunk/             
├── analysis/        
├── screenshots/       
└── report/              
```

---

## 🔍 Technical Implementation Matrix

### 1. Centralized Log Ingestion & Time-Sync Baseline (`/setup`)
* **Time Synchronization Validation:** Implemented Network Time Protocol (NTP) baseline configuration across all network endpoints. This steps ensures millisecond accuracy across log timestamps, preventing correlation drift during time-sensitive incident triage.
* **Source-Type Mapping:** Configured local monitoring paths for `/var/log/auth.log` inside Splunk to parse SSH authentication attempts continuously.

### 2. Adversarial Emulation Lifecycle (`/attack-simulation`)
* **High-Concurrency Bruteforcing:** Executed targeted directory attacks against the SSH daemon utilizing multiple concurrent workers to generate high-density log volumes.
* **Log Signature Validation:** Extracted specific cryptographic and failure status markers generated during the invalid authentication sequence.

### 3. Detection Engineering & SPL Analysis (`/splunk` & `/analysis`)
Advanced SPL query engineering was utilized to parse the unstructured Linux PAM logs, filtering out standard user errors from programmatic attacks:
* **Attack Signature Parsing:** Isolated string indicators such as `Failed password for invalid user`, `Connection closed by`, and `Disconnecting: Too many authentication failures`.
* **Field Extraction Performance:** Isolated critical indicators of compromise (IoCs) including `Attacker Source IP`, `Target Username Attempted`, `Source Port`, and `Failure Frequency Delta`.
* **Behavioral Threshold Rule:** Formulated logic to flag an incident when an external IP hits the authentication daemon with $\ge 15$ failed attempts within a rolling 30-second window.

---

## 🚀 Key Learning Deliverables & Professional Competencies
Through engineering this defensive architecture, the following enterprise security skills were validated:
* **Linux Infrastructure Hardening:** Gained deep operational knowledge of Linux core networking engines, Pluggable Authentication Modules (PAM), and SSH operational configurations.
* **SIEM Forensic Analysis:** Practical mastery of building precise forensic queries to parse high-velocity identity logs and map behavioral patterns.
* **Incident Timeline Reconstruction:** Rebuilt step-by-step adversarial actions sequentially from initial handshake failure to target host exhaustion.
