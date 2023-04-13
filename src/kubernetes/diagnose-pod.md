[
  id: kubernetes-diagnose-pod
  tags:
    - debugging
  locations:
]: #

# Diagnose a pod

If a pod isn't starting or has other problems, you can retrieve vital information with the ``describe`` command.

````bash
kubectl describe pod <pod-name>
````

To find the ``<pod-name>``, run the command below the ``NAME`` value.

````bash
kubectl get pods
````
