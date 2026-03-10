# Troubleshooting Notes

“Remount filesystem… sudo mount -o remount, rw /”

## Kali Read-Only Filesystem
Fix:
sudo mount -o remount,rw /

## Network Issues
Restart NetworkManager:
sudo systemctl restart NetworkManager

## DHCP (Ubuntu NAT)
sudo dhclient
