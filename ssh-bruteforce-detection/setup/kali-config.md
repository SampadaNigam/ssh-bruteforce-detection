# Kali Internal Network Configuration

From your document: “sudo nmcli con mod… 10.0.0.11/24… Troubleshooting: Read-only file system”

## Static IP Setup
sudo nmcli con mod "Wired connection 1" ipv4.addresses 10.0.0.11/24
sudo nmcli con mod "Wired connection 1" ipv4.method manual
sudo nmcli con up "Wired connection 1"

Verify:
ip a

## Troubleshooting
If you see “Read-only file system”:
- Reboot Kali
- Or remount:
  sudo mount -o remount,rw /
