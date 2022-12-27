From this link: https://kubernetes.io/docs/concepts/configuration/configmap/


And after applying this files
run
kubectl exec -it <podname> -- printenv

validate that there are properties printed which are defined in the cm file


You can also create a scalar (no depth) configmap using this syntax:
kubectl create configmap myconfigmap --from-env-file=./groep-configmap.txt
