# promtail-k8s
Grabber k8s logs for sending them to Loki


There is an ansible playbook for rolling out the Promtail graber to your k8s cluster for collecting logs.


```bash
ansible-playbook docker-deploy.yml --extra-vars \"host_group=INSTANCES \"
```


Before starting work, you need to fill in the address of the loki server in vars.

***group_vars/all***
```bash
LOKI_SERVER: 'http://you-server:3100/loki/api/v1/push'
```

Also add your servers to `cluster.inventory`

As a success, you can see the data that appears in the `Grafana - Explore tab`
![screenshot of sample](https://i.gyazo.com/15fa324c04f851bf0b2896d4b8096214.png)