[
  id: kubernetes-resource-names-in-cli
  tags:
  locations:
]: #

# Resource names in variables

Retrieve a resource name, like a pod or service, and store it in a variable.

## Format
````bash
export POD_NAME=$(kubectl get <resource> -o=jsonpath='{.path.to.value}')
````

## Example: Get name of first pod
````bash
export POD_NAME=$(kubectl get pods -o=jsonpath='{.items[0].metadata.name}')
````
