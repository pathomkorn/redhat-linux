# Enable Optional Repo
```bash
# subscription-manager config --server.proxy_hostname=<proxy_server> --server.proxy_port=<proxy_port>
# subscription-manager register --username <rhn_username> --password <rhn_password>
# subscription-manager list --available
# subscription-manager attach --pool=<pool_id>
# subscription-manager repos --enable=rhel-7-server-optional-rpms
# yum repolist
```
