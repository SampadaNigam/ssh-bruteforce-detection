# Ubuntu Internal Network Configuration

From your document: “addresses: 10.0.0.10/24… sudo netplan apply”

## Static IP Setup
Identify interface:
ip a

Edit Netplan:
sudo nano /etc/netplan/01-netcfg.yaml

Example:
network:
  version: 2
  ethernets:
    enp0s8:
      addresses:
        - 10.0.0.10/24
      dhcp4: no

Apply:
sudo netplan apply

Verify:
ip a
