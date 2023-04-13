[
  id: kubernetes-diagnose-pod
  tags:
    - debugging
  locations:
]: #

# Diagnose a pod

If a pod isn't starting or has other problems, you can retrieve vital information with the ``describe`` command.
First get the list of pods, and then choose the ``NAME`` as ``<pod-name>``.

````bash
kubectl get pods
kubectl describe pod <pod-name>
````
