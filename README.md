# distributed-containers
Contains code associated to probe of concepts and demos of technologies related to **distributed containers**. 

The Repository is devided in the following folders:

- **kubernetes**:
  Contains examples of YAML code of applications uses in demos.

  - **Stateless**:
     This folder contains the code of a stateless hello world application deployment yaml and its related Ingress resource. 
     There are three yaml files:
     - hellodemo_deployment.yaml: Deployment resource of the workload associated to the hello work example.
     - hellodemo_ingress.yaml: Ingress definition of the hello wold example. Uses an annotation to get an external IP that was created before the 
                               this deployment through google cloud with the following command: "gcloud compute addresses create helloweb-ip"
     - hellodemo-ingress-nodeport.yaml: Ingress YAML equivalent to the previous one by defining a nodeport to be acceded from outside.
                                        Deploy one ingress file or the other.  

- **rancher**:
  Contains the Infrastructure as code resources to provision Rancher as a Product.  It has a folder for each hyperscaler where it can be provisioned.
  The Azure Rancher provision code has been tested and it deploys all the artefacts in one resource group specified. We can find the following provison 
  options:
  - Google Cloud. /gcp
  - Amazon. /aws
  - Azure. /azure


  ![image](./images/rancherazure.jpg)
  