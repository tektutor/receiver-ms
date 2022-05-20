# Deploying reciver microservice into OpenShift
```
cd ~
git clone https://github.com/tektutor/receiver-ms.git

cd receiver-ms
oc apply -f receiver.yml
```

# Create a clusterip internal service
```
oc expose deploy receiver-ms
```

# Expose a route for the clusterip service
```
oc expose svc/receiver-ms
```

You can invoke the receiver-ms by calling the route url
```
oc get route
```
