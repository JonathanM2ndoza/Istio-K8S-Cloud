# Istio-K8S-Cloud

Example of how use Istio and IBM Cloud Kubernetes Service.

### Log in to the IBM Cloud CLI. If you have a federated account, include the --sso flag

jmendoza@jmendoza-ThinkPad-T420:~$ ibmcloud login --sso

###  Verify that the plug-in is installed properly

The service plug-in is displayed in the results as container-service/kubernetes-service.

![Screenshot](prtsc/Istio-K8S-Cloud-1.png)

### Create Kubernetes cluster in IBM Cloud

![Screenshot](prtsc/Istio-K8S-Cloud-3.png)

### Set the context for your cluster in your CLI

jmendoza@jmendoza-ThinkPad-T420:~$ ibmcloud ks clusters

jmendoza@jmendoza-ThinkPad-T420:~$ ibmcloud ks cluster config --cluster k8s-cluster

![Screenshot](prtsc/Istio-K8S-Cloud-4.png)





















