# haproxy-k8s
haproxy practice

> get nodeport number using

https://www.haproxy.com/documentation/kubernetes/latest/installation/

```bash
kubectl describe svc haproxy-ingress -n kocu-haproxy-controller
```

or by 
```bash
kubectl get svc haproxy-ingress

example output
haproxy-ingress   NodePort   10.97.20.172   <none>        80:31671/TCP,443:30332/TCP,1024:32537/TCP   58m

```

above means port 31671 on your NodePort gets forwarded to port 80 in the ingress controller (haproxy-ingress)



http://localhost:32537/stat

