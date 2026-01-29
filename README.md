\# GKE Portfolio App



A simple web application deployed on \*\*Google Kubernetes Engine (GKE)\*\* using modern cloud-native tooling.



\## 🚀 Architecture Overview



This project demonstrates a full containerized deployment workflow on Google Cloud:



\- Dockerized static web app (NGINX)

\- Google Cloud Build for image builds

\- Artifact Registry for container storage

\- Google Kubernetes Engine (GKE) for orchestration

\- Kubernetes Service (LoadBalancer) for public access



\## 🧱 Architecture Diagram (Logical)



User Browser  

→ Google Cloud Load Balancer  

→ Kubernetes Service (LoadBalancer)  

→ GKE Cluster  

→ Pod (NGINX container serving index.html)



\## 🛠️ Technologies Used



\- Google Cloud Platform (GCP)

\- Google Kubernetes Engine (GKE)

\- Docker

\- Google Cloud Build

\- Artifact Registry

\- Kubernetes (kubectl)

\- NGINX



\## 📦 Deployment Flow



1\. Build Docker image locally using Cloud Build

2\. Push image to Artifact Registry

3\. Deploy image to GKE using Kubernetes Deployment

4\. Expose application using a Kubernetes LoadBalancer Service

5\. Access app via external IP



\## 🌐 Live Application



The application is exposed publicly via a GKE LoadBalancer service.



> External IP assigned dynamically by Google Cloud



\## 🎯 What This Project Demonstrates



\- End-to-end container deployment on GCP

\- Kubernetes fundamentals (pods, deployments, services)

\- Cloud-native CI build pipeline

\- Real-world cloud engineer workflow



\## 🔮 Next Improvements (Planned)



\- HTTPS with Google-managed certificates

\- CI/CD auto-deploy on Git push

\- Kubernetes ConfigMaps for live content updates

\- Monitoring and logging (Cloud Operations)



---



\*\*Author:\*\* Courtney Artis  

\*\*Role Target:\*\* Cloud Engineer / Platform Engineer  

\*\*Last Updated:\*\* January 2026


## Architecture

User Browser
|
| HTTP (port 80)
v
GKE Service (type: LoadBalancer)
|
| routes traffic to
v
Kubernetes Deployment (portfolio-app)
|
| runs container image from
v
Artifact Registry (Docker image)
^
|
Cloud Build (builds + pushes image from local source)
^
|
Local Project Folder (index.html + Dockerfile)


