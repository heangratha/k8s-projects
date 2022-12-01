K8S Infrastructure Setup 1.24.8
===============================

For Testing Local Environment OR Can Deploy as Production
---------------------------------------------------------

Requirement:
------------
```
Ubuntu: 22.04
ansible: 2.10.x
python: 3.10.x
kubernetes: 1.24.x
```

k8s infrastructure.

```
# Kubernetes server
192.168.56.220 k8s-control-plan
192.168.56.221 k8s-worker1
```

- Review the IP address of controller and nodes in `inventory.yml` file to make sure it matches above

- Provision the cluster

```
ansible-playbook 1-setup.yml
ansible-playbook 2-join.yml
ansible-playbook 3-ingress.yml
```

- Reset the cluster

```
ansible-playbook 0-reset.yml
```

- Better regenerate certificate for 10 years prevent expiraltion
