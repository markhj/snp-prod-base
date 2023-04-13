[
  id: kubernetes-access-shell
  tags:
    - shell
    - debugging
  locations:
]: #

# Access pod shell

You can access the shell of a pod with the command below.

````bash
kubectl exec --stdin --tty <pod-name> -- /bin/bash
````

To find your ``<pod-name>``, pick the ``NAME`` from:

````kubectl
kubectl get pods
````

> :information_source: Pods change the value under ``NAME`` when they're re-deployed. So, it's not possible to bookmark this value.
