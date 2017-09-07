Docker Stack for Ansible AWX

Deploy the stack with following command

```
DOMAIN=domain.com docker stack deploy --compose-file awx.yml awx
```

This compose file works with volume driver "docke-volume-netshare" by ContainX
