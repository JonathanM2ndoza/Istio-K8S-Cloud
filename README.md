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

![Screenshot](prtsc/Istio-K8S-Cloud-14.png)

## Install the Guestbook app with manual sidecar injection

![Screenshot](prtsc/Istio-K8S-Cloud-15.png)

![Screenshot](prtsc/Istio-K8S-Cloud-15.1.png)

![Screenshot](prtsc/Istio-K8S-Cloud-15.2.png)

![Screenshot](prtsc/Istio-K8S-Cloud-15.3.png)

![Screenshot](prtsc/Istio-K8S-Cloud-15.4.png)

## Add the Watson Tone Analyzer

Create the Watson Tone Analyzer in your account:

jmendoza@jmendoza-ThinkPad-T420:~/IdeaProjects/JonathanM2ndoza/Istio-K8S-Cloud/istio101/workshop/plans$ ibmcloud resource service-instance-create jm-tone-analyzer-service tone-analyzer lite us-south

![Screenshot](prtsc/Istio-K8S-Cloud-16.png)

## Configure Istio to receive telemetry data

![Screenshot](prtsc/Istio-K8S-Cloud-17.png)

![Screenshot](prtsc/Istio-K8S-Cloud-17.1.png)

### View guestbook telemetry data with Jaeger

Generate a small load to the app

![Screenshot](prtsc/Istio-K8S-Cloud-18.png)

  ```shell
     jmendoza@jmendoza-ThinkPad-T420:~/IdeaProjects/JonathanM2ndoza/Istio-K8S-Cloud/istio101/workshop/plans$ kubectl port-forward -n istio-system \>   $(kubectl get pod -n istio-system -l app=jaeger -o jsonpath='{.items[0].metadata.name}') \
     >   16686:16686 &
     [1] 15252
     jmendoza@jmendoza-ThinkPad-T420:~/IdeaProjects/JonathanM2ndoza/Istio-K8S-Cloud/istio101/workshop/plans$ Forwarding from 127.0.0.1:16686 -> 16686
     Forwarding from [::1]:16686 -> 16686
     Handling connection for 16686
     Handling connection for 16686
     Handling connection for 16686
  ```

![Screenshot](prtsc/Istio-K8S-Cloud-18.1.png)
































