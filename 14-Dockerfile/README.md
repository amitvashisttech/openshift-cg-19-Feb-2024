## Openshift Build from a Dockerfile & Git 

### 1. Create a new app
```
oc new-app --name hello-world-nginx-2 https://github.com/amitvashisttech/openshift-cg-19-Feb-2024 --context-dir 14-Dockerfile
```

### 2. Check the build Status 
```
oc logs -f buildconfig/hello-world-nginx-2
```

### 3. Overall Status
```
oc status
```

### 4. Status of all the objects 
```
oc get pod,deploy,build,svc,buildconfig,imagestream
```

### 5. Create a Route   
```
oc get svc
oc expose service hello-world-nginx-2
```
