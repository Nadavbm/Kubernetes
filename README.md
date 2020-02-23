# Kubernetes

### Install Kubernetes and Minikube on Ubuntu16
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
chmod +x kubectl
mv kubectl /usr/local/bin/ 
kubectl version --client

curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64   && chmod +x minikube
install minikube /usr/local/bin/
minikube
minikube start --vm-driver=virtualbox

## Kubernets in Google cloud project
gcloud projects list
gcloud config set project projectName
gcloud config set compute/zone us-west1-a
gcloud config set compute/region us-west

gcloud container clusters list

gcloud container cluster get-credentials clusterName \
    --zone us-west1-a \
    --project projectName

kubectl config rename-context gke_projectName_us-wests1-a_clusterName kubectxName



