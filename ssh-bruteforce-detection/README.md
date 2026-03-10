# SSH Brute-Force Detection Lab (Kali → Ubuntu → Splunk)

This project demonstrates how I built a mini SOC lab using VirtualBox, Ubuntu, Kali,
and Splunk to detect SSH brute-force attacks. The attacker (Kali) uses Hydra to
generate SSH login attempts, while Splunk ingests `/var/log/auth.log` from Ubuntu
and visualizes the attack.

## 🔧 Tools Used
- Ubuntu Server (Splunk + SSH target)
- Kali Linux (attacker)
- Hydra (brute-force tool)
- Splunk Enterprise (free)
- VirtualBox
- rockyou wordlist

## Project Structure
ssh-bruteforce-detection/
│
├── setup/
├── attack-simulation/
├── splunk/
├── analysis/
├── screenshots/
└── report/


## Key Results
- Successfully generated SSH brute-force traffic using Hydra  
- Splunk ingested `/var/log/auth.log` and detected failed login attempts  
- Time synchronization issues fixed (NTP)  
- Verified attacker IP, username attempts, and frequency  

## What I Learned
- Linux network configuration (static IPs, Netplan, nmcli)
- Splunk log ingestion and search queries
- SSH authentication log analysis
- Troubleshooting VirtualBox networking


## Screenshots
See `/screenshots` folder.

