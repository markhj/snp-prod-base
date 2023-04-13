[
  id: kubernetes-access-shell
  tags:
    - shell
    - debugging
  locations:
]: #

# Access pod shell

You can access the shell of a pod with the command below.
First, we're retrieving the list of pods. Replace ``<pod-name>`` the value in ``NAME`` colu

````bash
kubectl get pod
kubectl exec --stdin --tty <pod-name> -- /bin/bash
````

> :information_source: Pods change the value under ``NAME`` when they're re-deployed. So, it's not possible to bookmark this value.
