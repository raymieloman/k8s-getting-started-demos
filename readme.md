# Starten van dit project
kubectl create -f ./namespace.yaml
kubectl create -f ./clusterip-service.yaml
kubectl create -f ./nodeport-service.yaml
kubectl create -f ./nginx-deployment.yaml

# Services first => from the official specs
The resources will be created in the order they appear in the file. Therefore, it's best to specify the service first, since that will ensure the scheduler can spread the pods associated with the service as they are created by the controller(s), such as Deployment.


# To test the clusterip service in the cluster
$ kubectl run my-nginx-app --image=nginx:latest 
$ kubectl exec -it my-nginx-app -- /bin/bash
$ curl http://clusterip:8082  (in the my-nginx-app)
(you can also use the client-pod.yaml for this)
