# Findings

## Summary
- Kali (10.0.0.11) attempted multiple SSH logins on Ubuntu (10.0.0.10)
- Hydra generated rapid login attempts using rockyou wordlist
- Splunk successfully ingested and visualized events

## Key Indicators
- High number of failed passwords
- Repeated attempts against root
- Attack timeline visible in Splunk
