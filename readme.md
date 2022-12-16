let op:
jet moet! 
$ kubectl run my-nginx-app --image=nginx:latest 
$ kubectl exec -it my-nginx-app -- /bin/bash
 en  dan
$ curl http://clusterip:8082 doen in die my-nginx-app pod om de clusterip service te bereiken.
Je kunt de cluster ip service NIET bereiken in de nginx-pod
