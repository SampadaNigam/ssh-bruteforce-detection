# Incident Report: SSH Brute-Force Attempt

## Executive Summary
A brute-force attack was simulated from Kali (10.0.0.11) targeting Ubuntu (10.0.0.10).
Splunk successfully detected repeated failed SSH login attempts.

## Timeline
- Attack initiated using Hydra
- Logs generated in /var/log/auth.log
- Splunk ingested logs in real time
- Detection queries confirmed brute-force activity

## Impact
No system compromise occurred. Attack was contained within lab.

## Recommendations
- Implement fail2ban
- Enforce key-based authentication
- Disable root login
