🚀 End-to-End CI/CD Implementation | Jenkins + Docker + Kubernetes + AWS
I’m pleased to share my recent hands-on project where I successfully implemented a complete CI/CD pipeline for a sample retail application — as part of a DevOps certification challenge for Abstergo Corp. This project demonstrates how Continuous Integration and Continuous Deployment can drastically improve delivery speed and system reliability.

📍 Objective
Abstergo Corp required a system that:
->Automatically builds code pushed to GitHub.
-> Containerizes the application using Docker.
-> Pushes the image to Docker Hub.
-> Deploys it to a Kubernetes cluster for production use.


The app is a Node.js-based Train Schedule Viewer, ideal for demonstrating CI/CD automation.

🧰 Technology Stack
->Version Control: Git & GitHub
-> CI Server: Jenkins
-> Containerization: Docker
-> Image Registry: Docker Hub
-> Orchestration: Kubernetes
-> Cloud Infrastructure: AWS EC2

🛠️ Pipeline Breakdown
✅ Step 1: Jenkins Configuration
Installed and configured Jenkins on an EC2 instance.
Opened necessary ports and secured access.
Integrated GitHub with Jenkins to trigger builds on push.

✅ Step 2: Docker Image Creation & Push
Jenkins Job #1 builds the Docker image from source.
Tags and pushes the image to Docker Hub.
Example image: sushant960kr/train-schedule:9
📌 This step ensures every GitHub commit results in a new versioned Docker image.

✅ Step 3: Kubernetes Deployment
Set up Kubernetes (master & worker) using kubeadm on AWS EC2 instances.
Jenkins Job #2 pulls the Docker image and deploys it to the cluster.
Application exposed via NodePort and made accessible over the internet.
📍 Accessed live at: http://3.22.74.103:32001
 🚉 Train schedule app showing real-time updates like ON TIME, DELAYED, etc.

✅ Step 4: Jenkins Pipeline View
Chained Job #1 and Job #2 using the Pipeline View.
Achieved full automation from code push → build → Docker image → deploy to K8s.

💡 Key Learnings
Real-world experience in setting up Jenkins-Docker-Kubernetes integrations.
Deepened understanding of build automation and infrastructure-as-code.
Gained practical insight into troubleshooting deployment pipelines.

Once it is running, you can access it in a browser at http://localhost:8080
<img width="1916" height="1199" alt="Screenshot 2025-07-27 120149" src="https://github.com/user-attachments/assets/83ff0a04-f6e8-4933-a199-b885ca8ff4ec" />
<img width="1916" height="1195" alt="Screenshot 2025-07-27 135428" src="https://github.com/user-attachments/assets/fc75e39b<img width="1919" height="1094" alt="Screenshot 2025-07-27 134714" src="https://github.com/user-attachments/assets/115c47d9-0cb8-4268-a05d-cff7a09be2fb" />
<img width="1919" height="1148" alt="Screenshot 2025-07-28 121706" src="https://github.com/user-attachments/assets/79cf951d-6b5a-4bbb-965a-b3539cee8d63" />
<img width="1803" height="674" alt="Screenshot 2025-07-27 134524" src="https://github.com/user-attachments/assets/87c27768-71b5-4426-b7a5-d7fd9d7b6811" />
<img width="1916" height="1195" alt="Screenshot 2025-07-27 135428" src="https://github.com/user-attachments/assets/8497ebbb-3e16-4896-8a19-ae15c9ab68e5" />
