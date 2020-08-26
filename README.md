# acmdemo
source for acm demos

## Deploying a simple vm application



```
oc login
cd acm/simpleapp
oc apply -f .
```


## Deploying a multi-cluster application

```
oc login
cd acm/vmapp
oc apply -f .
```



## Policies

The policy directory contains a few different policies. We will use these policies to lay down some default authentication on new clusters and ensure that my account is added to the cluster-admin role.

To start we need to have a few tools available. The biggest one is "kustomize"

We will store all our policies in the namespace "open-cluster-management-policies".  Note that you can put policies in any project/namespace, this is just where we will be storing these example policies.

```
oc login
oc create -f acm/policy/policies-namespaces.yaml
kustomize build acm/policies/ | oc apply -f -
```

## Scan for vulnerabilities

tag a cluster with enforceSecureImages=true
