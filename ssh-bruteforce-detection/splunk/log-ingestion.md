# Splunk Log Ingestion

“Add input for /var/log/auth.log… splunk add monitor”

## Add SSH Log Input
GUI:
Settings → Data Inputs → Files & Directories → Add /var/log/auth.log

CLI:
sudo /opt/splunk/bin/splunk add monitor /var/log/auth.log

Restart:
sudo /opt/splunk/bin/splunk restart
