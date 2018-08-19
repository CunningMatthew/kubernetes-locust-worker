# docker-locust

Docker Image for a [Locust](http://locust.io/).

# Running in K8s

kubectl create configmap locust-config --from-file=locust_test/

kubectl create -f locust-deployment.yaml

kubectl expose deployment locust-deployment --type=NodePort

kubectl create -f locust-ingress.yaml

# Configuring minikube to run locally

Set up a new virtual switch in Hyper-V Manager on windows that was configured to the external network

Started my minikube instance using the command `minikube start --vm-driver hyperv --hyperv-virtual-switch "minikube_switch"`

Got the IP of my minikube deployment by using the command `minikube ip`

Enabled ingress on the minikube instance by using the command `minikube addons enable ingress`