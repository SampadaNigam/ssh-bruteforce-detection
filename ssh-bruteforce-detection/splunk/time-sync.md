# Fixing Splunk Time Sync (NTP)

“sudo timedatectl set-ntp true… sudo ntpdate pool.ntp.org”

## Enable NTP
sudo timedatectl set-ntp true

Restart service:
sudo systemctl restart systemd-timesyncd

If still unsynchronized:
sudo apt install ntpdate
sudo ntpdate pool.ntp.org

Set timezone:
sudo timedatectl set-timezone <your local time zone>
