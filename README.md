### Задача 1: Рассмотрите пример 14.5/example-security-context.yml
- Создание модуля
```
vlad@home:~/Documents/Netology/DevOps/netology-DevOps-dz_66$ kubectl apply -f ../../homework/clokub-homeworks/14.5/example-security-context.yml 
pod/security-context-demo created
vlad@home:~/Documents/Netology/DevOps/netology-DevOps-dz_66$ kubectl get pods 
NAME                    READY   STATUS    RESTARTS   AGE
security-context-demo   1/1     Running   0          3s
```

- Проверка настроек внтури модуля

```
vlad@home:~/Documents/Netology/DevOps/netology-DevOps-dz_66$ kubectl exec --stdin --tty pods/security-context-demo -- /bin/bash
bash-5.1$ id -u ; id -g
1000
3000

```