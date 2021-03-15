# promtail-k8s
Grabber k8s logs for sending them to Loki


In this repository there is an ansible playbook for rolling out the Promtail graber to your k8s cluster for collecting logs.

Before starting work, you need to fill in the address of the loka server in vars.

***group_vars/all***
```bash
LOKI_SERVER: 'http://you-server:3100/loki/api/v1/push'
```

Also add your servers to `cluster.inventory`

As a success, you can see the data that appears in the `Grafana - Explore tab`
![screenshot of sample](https://i.gyazo.com/24e9fdcf4fafa864b9708a64e125401d.png)