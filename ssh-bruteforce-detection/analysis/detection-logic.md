# Detection Logic

## What We Detect
- Repeated failed SSH login attempts
- Source IP of attacker
- Target username
- Frequency of attempts

## Why It Works
SSH brute-force attacks generate:
- "Failed password"
- "Invalid user"
- High-frequency login attempts

Splunk correlates these patterns to identify brute-force behavior.
