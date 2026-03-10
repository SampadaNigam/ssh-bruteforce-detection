# Splunk Installation on Ubuntu

“wget -O splunk.deb… sudo dpkg -i splunk.deb”

## Download & Install
wget -O splunk.deb "https://download.splunk.com/products/splunk/releases/.../splunk-linux-2.6-amd64.deb"
sudo dpkg -i splunk.deb

## Start Splunk
sudo /opt/splunk/bin/splunk start --accept-license

Enable at boot:
sudo /opt/splunk/bin/splunk enable boot-start

Access UI:
http://<Ubuntu NAT IP>:8000
