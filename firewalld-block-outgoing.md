# Firewalld - Block Outgoing
* Block outgoing MSSQL service
```bash
systemctl start firewalld
firewall-cmd --get-active-zones
firewall-cmd --zone=trusted --change-interface=eth0
firewall-cmd --get-active-zones
firewall-cmd --direct --add-rule ipv4 filter OUTPUT 0 -p tcp -m tcp --dport=1433 -j DROP
```
* Test Connection
* Flush block rule
```bash
firewall-cmd --direct --remove-rule ipv4 filter OUTPUT 0 -p tcp -m tcp --dport=1433 -j DROP
firewall-cmd --direct --get-all-rules
firewall-cmd --zone=public --change-interface=eth0
firewall-cmd --get-active-zones
systemctl stop firewalld
```
