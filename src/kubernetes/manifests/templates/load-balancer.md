[
  id: kubernetes-manifest-load-balancer
  tags:
    - template
  locations:
]: #

# Load balancer

````yml
apiVersion: v1
kind: Service
metadata:
  name: <name>
spec:
  selector:
    app: <app>
  ports:
  - name: http
    port: 80
    targetPort: 80
    protocol: TCP
  type: LoadBalancer
````
