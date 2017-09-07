Docker Stack for Ansible AWX
============================

Deploy the stack with following command

```
DOMAIN=domain.com docker stack deploy --compose-file awx.yml awx
```

```
docker stack ps awx
ID                  NAME                IMAGE                         NODE                DESIRED STATE       CURRENT STATE            ERROR               PORTS
uplhpeaj7qtq        awx_awx_task.1      chmod666/awx_task:1.0.0.280   swarm3              Running             Running 2 minutes ago                        
t4nszesw6l72        awx_awx_web.1       chmod666/awx_web:1.0.0.280    swarm1              Running             Running 2 minutes ago                        
8gbqqv4swsfk        awx_rabbitmq.1      chmod666/rabbitmq:3           swarm2              Running             Running 36 minutes ago                       
55bzqy29bde3        awx_postgres.1      chmod666/postgres:9.6         swarm1              Running             Running 36 minutes ago                       
```

This compose file works with volume driver "docker-volume-netshare" by ContainX for the nfs part
