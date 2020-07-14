k8s-cheat-sheet
---------------


## Secrets

### Extract docker credentials from docker secret

```
kubectl get secrets docker-registry-credentials -n default -o go-template='{{ index .data ".dockerconfigjson"}}' | base64 -d
```
