# acmdemo
source for acm demos

## Deploying a simple vm application

```
oc login
cd acm/vmapp
oc apply -f .
```



## Policies

The policy directory contains a few different policies. We will use these policies to lay down some default authentication on new clusters and ensure that my account is added to the cluster-admin role