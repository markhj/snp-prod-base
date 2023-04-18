[
  id: kubernetes-resource-names-in-cli
  tags:
  locations:
]: #

# Resource names in CLI

## Format
````bash
export POD_NAME=$(kubectl get <resource> -o=jsonpath='{.path.to.value}')
````

## Example: Get name of first pod
````bash
export POD_NAME=$(kubectl get pods -o=jsonpath='{.items[0].metadata.name}')
````
