Zo run je een Horizontal Autoscaler create:
kubectl autoscale deployment nginx --cpu-percent=50 --min=3 --max=5 --dry-run=client -o yaml | grep -Ev "{}|null" > horizontalautoscaler.yaml
