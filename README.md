# DevOps-Project-BankApplication-BlueGreen-Deployment-MultiCloud

The project is in multicloud (AWS and Azure Cloud) with AWS as the major cloud.


![image](https://github.com/user-attachments/assets/5238d7a8-eaf2-4a49-98b5-821348f3acfc)

This DevOps Project deals with creation of Infrastructure using Terraform and setup of CICD Pipeline using Jenkins, Monitoring using Prometheus and Grafana and Log Aggregation using Loki, Promtail and Grafana. SonarQube was used for Code-Analysis and Maven was used as the Build Tool. Nexus Artifactory was used to keep the Artifacts as shown in the Architecture diagram above. Trivy was used for Docker Image Scan. The Docker Image was kept in the Elastic Container Registry (ECR) and which was deployed to EKS Cluster using the ArgoCD as shown in the high-level architecture diagram above. User was able to access the Application through the Ingress and hence the Kubernetes Service. The source code was present in the GitHub Repository https://github.com/singhritesh85/Bank-App.git. For this project to deploy a new Release of code I had used Blue-Green deployment with the help of ArgoCD Rollout. Promtail and Node Exporter was installed on all the Loki Servers, Grafana, Prometheus, Jenkins (Master and Slave Nodes) using the boot-strapping script. For the EKS cluster the Promtail and Node Exporter was installed with the help of helm. 
Promtail is Log Aggregation Agent for Loki and Node Exporter agent collects the metrics and forward to Loki and Prometheus respectively. The high-level architecture diagram of the project is as shown above. Installation of Jenkins-Master, Jenkins-Slave, Nexus, SonarQube, Loki Servers, Prometheus and Grafana had been done using the bootstrapping Script. 

