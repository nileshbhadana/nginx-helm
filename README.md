## Nginx Helm Chart

### 📜 Prerequisites

- Helm cli v3
    >Refer [this](https://helm.sh/docs/intro/install/) document to install helm

- Kubernetes cluster configured.
---
### How to install chart:-
1. Add helm repository
    ```
    helm repo add nginx-nilesh http://nileshbhadana.me/nginx-helm
    ```
2. Installing chart
    ```
    helm install nginx nginx-nilesh/nginx
    ```

---
### Customize the chart by pulling it on your machine
1. Pull chart as tar
    ```
    helm pull nginx-nilesh/nginx
    ```

2. Unzipping the tar file.
    ```
    tar -xvf nginx-1.0.0.tgz
    ```

Now you can find the chart in `nginx` folder and customize it using your favourite editor. 

---
### Changing configuration
- Nginx configurations are used by the nginx pod through configmap - `nginx-server-block`. To make changes you need to update it in `values.yaml` file of this chart otherwise it uses default values.

## Changing static site
- Right now static site has a default html present and this is also a part of configmap, so you can update the `staticSite` section in values file to make new changes.
