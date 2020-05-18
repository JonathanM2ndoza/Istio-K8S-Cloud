# Istio-K8S-Cloud

Example of how use Istio and IBM Cloud Kubernetes Service.

## Create Kubernetes cluster in IBM Cloud

![Screenshot](prtsc/Istio-K8S-Cloud-3.png)

![Screenshot](prtsc/Istio-K8S-Cloud-3.1.png)

### Log in to the IBM Cloud CLI. If you have a federated account, include the --sso flag

jmendoza@jmendoza-ThinkPad-T420:~$ ibmcloud login --sso

###  Verify that the plug-in is installed properly

The service plug-in is displayed in the results as container-service/kubernetes-service.

![Screenshot](prtsc/Istio-K8S-Cloud-1.png)

### Set the context for your cluster in your CLI

![Screenshot](prtsc/Istio-K8S-Cloud-4.png)

## Install Istio on IBM Cloud Kubernetes Service

![Screenshot](prtsc/Istio-K8S-Cloud-7.png)

![Screenshot](prtsc/Istio-K8S-Cloud-8.png)

![Screenshot](prtsc/Istio-K8S-Cloud-9.png)

![Screenshot](prtsc/Istio-K8S-Cloud-9.1.png)

Ensure that the istio-* Kubernetes services are deployed before you continue:

![Screenshot](prtsc/Istio-K8S-Cloud-10.png)

Ensure the corresponding pods istio-citadel-*, istio-ingressgateway-*, istio-pilot-*, and istio-policy-* are all in the Running state before you continue.

![Screenshot](prtsc/Istio-K8S-Cloud-11.png)

## Download the Guestbook app and create the Redis database

Create the Redis controllers and services for both the master and the slave:

![Screenshot](prtsc/Istio-K8S-Cloud-13.png)




























