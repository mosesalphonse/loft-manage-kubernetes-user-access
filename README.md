# loft-manage-kubernetes-user-access

  Many challenges that companies face or will face when they introduce Kubernetes for developers are already addressed today. The most fundamental of these challenges is how to provide developers a Kubernetes access. Here, virtual Kubernetes clusters are the newest solution that combine the advantages of existing approaches but without their disadvantages. Developers so get a fully isolated, very flexible self-service Kubernetes access that is also cost-efficient and does not require much effort from the sys admins. This makes vClusters a powerful new approach to solve the number one challenge of providing developers with infrastructure access to Kubernetes.

  Solutions such as Loft provide all of this out-of-the-box in an engineering-friendly fashion. Combining Loft’s vCluster platform with dev tools such as DevSpace makes the transition to Kubernetes even easier. Eventually, this can lead to a situation in which developers can mostly “ignore” the fact that they are using Kubernetes while they still have the freedom to directly interact with Kubernetes if they need it. Such a system will reduce organization-internal resistance against Kubernetes and so contributes to further Kubernetes adoption even during development.


## POC:
```
a) Install and Run Loft
b) Connect Multiple Kubernetes Clusters into Loft
c) Create user accounts and Virtual Cluster (vCluster)
d) Manage Clusters  resources including Sleep (Scale down to zero if not used)
```

## Prerequisite:
```
a) One or More Kubernetes Cluster

```


## Steps:
```
1) Download the Loft CLI
      
      curl -s -L "https://github.com/loft-sh/loft/releases/latest" | sed -nE 's!.*"([^"]*loft-linux-amd64)".*!https://github.com\1!p' | xargs -n 1 curl -L -o loft && chmod +x       loft;
      
      sudo mv loft /usr/local/bin;
      
2) Deploy Loft + Login  
      
      loft start

Note: If you use your domain, make sure you configure Ingress external IP into your domain

Login via browser or CLI.

3) Use Loft console to connect to additional kubernetes cluster, create users, vcluster etc.
4) connect to Vcluster

      loft login {url} --insecure  --username {username} --access-key {get it from loft profile}
      
      To Connect to vcluster, refer and copy the command from Loft console
    
```
