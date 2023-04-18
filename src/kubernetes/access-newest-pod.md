[
  id: kubernetes-access-newest-pod
  tags:
    - shell
    - debugging
  locations:
]: #

# Access most recent pod

To enter the most recently deployed pod:

````bash
kubectl exec --stdin --tty $(kubectl get pods --sort-by=.metadata.creationTimestamp -o=jsonpath='{.items[-1].metadata.name}') -- /bin/bash
````

> **TIP**: Add this in a command in your system that you can quickly execute.