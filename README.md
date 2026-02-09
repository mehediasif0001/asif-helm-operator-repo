# install helm
```bash
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-4 
chmod 700 get_helm.sh
./get_helm.sh
helm version
```
> chmod 700 means full privilege for user in this file

![Alt text](https://github.com/mehediasif0001/asif-helm-operator-repo/blob/main/images/helm-install.png)

**bitnami**
Bitnami is a company (now part of VMware / Broadcom) that provides ready-to-use, pre-configured, and secure application packages for cloud and Kubernetes environments.

Bitnami maintains:
>Helm charts (for Kubernetes)
>Containers (Docker images)
>Virtual machine images
>Cloud marketplace images
>For popular software like:Apache, NGINX, MySQL, PostgreSQL, Redis, Kafka, WordPress, etc.

The Bitnami Helm repository is a collection of official, well-maintained Helm charts.

install botnami repo in helm 
```
helm repo add bitnami https://charts.bitnami.com/bitnami
```
>• Registers the Bitnami Helm repository in your system
>• Tells Helm where to download charts from
>• Required before using charts like bitnami/apache
>• You only need to do this one time

```
helm repo update
```
>• Fetches the latest chart versions from all added repositories
>• Ensures you install the most up-to-date charts
>• Best practice after adding a new repository


```
helm install amaze-surf bitnami/apache
```
🔹 Explanation

• helm install
– Installs a Helm chart into the Kubernetes cluster

• amaze-surf
– Release name
– Used to manage this deployment (upgrade, rollback, uninstall)

• bitnami/apache
– Apache Helm chart from the Bitnami repository


• Check release status
```
helm status amaze-surf
```
• List Helm releases
```
helm list
 ```
• Check Kubernetes resources
```
kubectl get pods
kubectl get svc
```
