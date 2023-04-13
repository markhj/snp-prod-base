[
  id: kubernetes-restart-deployment
  tags:
    - kubectl
  locations:
]: #

# Restart deployment

To re-run a failed (or successful, for the matter) deployment, execute the following.
Replace ``<deployment-name>`` with the name of your deployment. This is found in your manifest or Kubernetes Dashboard, if you can't remember.

````bash
kubectl rollout restart deployment/<deployment-name>
````
