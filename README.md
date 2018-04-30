# Sensu on kubernetes deployed on AWS

## Architecture

https://go.gliffy.com/go/publish/11814882


## Status

Tested & Verified with below versions:
- kubernetes > 1.5.0 (no RBAC support)
- redis 3.2.6
- rabbitmq 3.6.6
- erlang 19.2
- sensu 0.20.3
- uchiwa 0.10.3


## Prerequisite

- clone and adjust [dixithb/Sensu-Uchiwa-Kubernetes](https://github.com/dixithb/Sensu-Uchiwa-Kubernetes)

Credentials:
- [rabbitmq user](https://github.com/dixithb/Sensu-Uchiwa-Kubernetes/blob/master/kubernetes/10-secret-rabbitmq.yaml#L8)
- [rabbitmq pass](https://github.com/dixithb/Sensu-Uchiwa-Kubernetes/blob/master/kubernetes/10-secret-rabbitmq.yaml#L9)
- [rabbitmq vhost](https://github.com/dixithb/Sensu-Uchiwa-Kubernetes/blob/master/kubernetes/10-secret-rabbitmq.yaml#L10)
- [rabbitmq cookie](https://github.com/dixithb/Sensu-Uchiwa-Kubernetes/blob/master/kubernetes/10-secret-rabbitmq.yaml#L7)

## Deploy

```
kubectl create -f kubernetes
```
## ToDo

- switch to alpine based sensu container after [#1201](https://github.com/sensu/sensu/issues/1201)
- add RBAC support
