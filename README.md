# Kubernetes Experaince
We already installed minikube for you. Check that it is properly installed, by running the minikube version command:
$ minikube version

OK, we can see that minikube is in place.
Start the cluster, by running the minikube start command:
$ minikube start

To interact with Kubernetes during this bootcamp we’ll use the command line interface, kubectl. We’ll explain kubectl in detail in the next modules, but for now, we’re just going to look at some cluster information. To check if kubectl is installed you can run the kubectl version command:
$ kubectl version

Let’s view the cluster details. We’ll do that by running kubectl cluster-info:
$ kubectl cluster-info

During this tutorial, we’ll be focusing on the command line for deploying and exploring our application. To view the nodes in the cluster, run the kubectl get nodes command:
$ kubectl get nodes

$ kubectl get deployments or secret or ....

Troubleshooting with kubectl

$ kubectl get - list resources
$ kubectl describe - show detailed information about a resource
$ kubectl logs - print the logs from a container in a pod
$ kubectl exec - execute a command on a container in a pod
    
$ kubectl get pods -> to show all pods 
$ kubectl describe pods -> get info about pods 
$ kubectl exec -it podname -> to go in to pods
$ kubectl delete svc -> delete resources by name files 
$ kubectl get all -> show all 
$ minikube service (name of service) to bind it to ip address 
$ minikube addons enable ingress -> to enable ingress and install nginx to cluster  
$ kubectl get ns -> get all namespaces 
$ kubectl config get-contexts -> show all context (local and clould)
$ kubectl config use-context CONTEXT_NAME -> set the context
$ kubectl create secret tls hello-app-tls \
    --namespace dev \
    --key server.key \
    --cert server.crt
    
    
annotations:
    nginx.ingress.kubernetes.io/proxy-body-size: "600m"
    nginx.org/client-max-body-size: "600m"
    nginx.ingress.kubernetes.io/force-ssl-redirect: "true"
    nginx.ingress.kubernetes.io/backend-protocol: "HTTP" -> this nota solve Plain HTTP Request Was Sent to HTTPS Port’ in NGINX in ingress
    cert-manager.io/cluster-issuer: "letsencrypt-prod"
    kubernetes.io/ingress.class: nginx

## URLs:
* https://kubernetes.io/docs/tasks/tools/
* https://kubernetes.io/docs/tutorials/kubernetes-basics/
* https://computingforgeeks.com/how-to-install-minikube-on-ubuntu-debian-linux/
* https://kubernetes.io/docs/concepts/configuration/secret/
* ssl tunnel https://www.concordia.ca/ginacody/aits/support/faq/ssh-tunnel.html
* https://stackoverflow.com/questions/42564058/how-to-use-local-docker-images-with-minikube
* https://kubernetes.io/docs/tasks/debug/debug-application/get-shell-running-container/
* https://stackoverflow.com/questions/47693911/how-to-delete-kubectl-service
* https://www.youtube.com/watch?v=X48VuDVv0do
* https://gitlab.com/nanuchi/youtube-tutorial-series/-/blob/master/kubernetes-ingress/dashboard-ingress.yaml
* https://www.tecmint.com/find-listening-ports-linux/
* https://kubernetes.io/docs/concepts/services-networking/ingress/
* https://assistanz.com/steps-to-create-custom-namespace-in-the-kubernetes/
* https://stackoverflow.com/questions/43643463/how-to-switch-kubectl-clusters-between-gcloud-and-minikube
----------------------------------------------------------------------------------------------------------------------------

## AWS Experaince 
### IAM
The AWS account root user or an IAM administrator for the account can create IAM identities. An IAM identity provides access to an AWS account. A user group is a collection of IAM users managed as a unit. An IAM identity represents a user, and can be authenticated and then authorized to perform actions in AWS. Each IAM identity can be associated with one or more policies. Policies determine what actions a user, role, or member of a user group can perform, on which AWS resources, and under what conditions.
* [IAM Video](https://www.youtube.com/watch?v=y8cbKJAo3B4)

### VPC
* [AWS VPC](https://aws.amazon.com/vpc/)
* [VPC Video](https://www.youtube.com/watch?v=bGDMeD6kOz0)

### ECR

----------------------------------------------------------------------------------------------------------------------------


