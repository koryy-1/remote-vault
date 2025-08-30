получить pods / deployments / services / nodes / namespaces / ingress / storageclass / pvc / pv
```
kubectl get <component>
```
e.g.
```
kubectl get pods
```
```
kubectl get deployments
```
```
kubectl get services
```

компоненты из другого NS
```
kubectl get <component> --namespace=<namespace>
```
e.g.
```
kubectl get deployments --namespace=ingress-nginx
```

применить какой-либо конфиг, например деплоймент
```
kubectl apply -f .\platforms-depl.yaml
```

рефреш образов для деплоймента
```
kubectl rollout restart deployment platforms-depl
```

## secrets
получить инфу
```
kubectl get secrets
```
```
kubectl describe secrets <secret name>
```

создать
```
kubectl create secret generic postgres --from-literal=<key>="<value>"
```
e.g.
```
kubectl create secret generic postgres --from-literal=postgres_password="str0ng_pwd"
```
из файла
``` 
kubectl create secret generic db-user-pass --from-file=password=./password.txt
```

изменить
```
kubectl edit secrets <secret-name>
```

удалить
```
kubectl delete secret <secret-name>
```
