```bash
firewall-cmd --get-default-zone
firewall-cmd --get-active-zones
firewall-cmd --get-zones
firewall-cmd --permanent --zone=internal --change-interface=eth0
firewall-cmd --permanent --zone=internal --add-service=ssh
firewall-cmd --permanent --zone=internal --add-service=http
firewall-cmd --permanent --zone=internal --add-service=https
firewall-cmd --permanent --zone=internal --add-service=dns
firewall-cmd --permanent --zone=internal --add-service=ntp
firewall-cmd --permanent --zone=internal --add-service=ftp
firewall-cmd --permanent --zone=internal --add-service=smtp
firewall-cmd --permanent --zone=public --add-forward-port='port=8001:proto=tcp:toport=8001:toaddr=X.X.X.X'
firewall-cmd --permanent --zone=public --add-forward-port='port=8080:proto=tcp:toport=8080:toaddr=X.X.X.X'
firewall-cmd --permanent --zone=public --add-forward-port='port=8443:proto=tcp:toport=8443:toaddr=X.X.X.X'
firewall-cmd --permanent --zone=public --add-forward-port='port=8500:proto=tcp:toport=8500:toaddr=X.X.X.X'
firewall-cmd --permanent --zone=public --add-forward-port='port=9443:proto=tcp:toport=9443:toaddr=X.X.X.X'
firewall-cmd --permanent --zone=public --add-forward-port='port=30000-32767:proto=tcp:toport=30000-32767:toaddr=X.X.X.X'
firewall-cmd --reload
firewall-cmd --list-all
firewall-cmd --list-all --zone=internal
```
