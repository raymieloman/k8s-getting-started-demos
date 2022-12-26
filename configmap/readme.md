From this link: https://kubernetes.io/docs/concepts/configuration/configmap/


And after applying this files
run
kubectl exec -it <podname> -- printenv

validate that there are properties printed which are defined in the cm file
