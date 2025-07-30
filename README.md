🚀 End-to-End CI/CD Implementation | Jenkins + Docker + Kubernetes + AWS
I’m pleased to share my recent hands-on project where I successfully implemented a complete CI/CD pipeline for a sample retail application — as part of a DevOps certification challenge for Abstergo Corp. This project demonstrates how Continuous Integration and Continuous Deployment can drastically improve delivery speed and system reliability.

📍 Objective
Abstergo Corp required a system that:
->Automatically builds code pushed to GitHub.
-> Containerizes the application using Docker.
-> Pushes the image to Docker Hub.
-> Deploys it to a Kubernetes cluster for production use.

🔗 GitHub Repository
📁 I used a forked version of a sample application from the original repository and worked on my own repo:
 👉 https://lnkd.in/gdRQymEi

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
<img width="1916" height="1199" alt="Screenshot 2025-07-27 120149" src="https://github.com/user-attachments/assets/6d4ab1fa-8005-48ca-b229-ad07c4756d83" />
<img width="1919" height="1094" alt="Scre<img width="1916" height="1199" alt="Screenshot 2025-07-27 120149" src="https://github.com/user-attachments/assets/a265552c-2ffe-4e80-89ca-541ff2ba8226" />
<img width="1919" height="1148" alt="Screenshot 2025-07-28 121706" src="https://github.com/user-attachments/assets/c7a9d5e2-55ca-4a7d-9281-d077e942acc4" />
<img width="1916" height="1195" alt="Screenshot 2025-07-27 135428" src="https://github.com/user-attachments/assets/6bb92bbf-1731-424a-910f-c69811251897" />
<img width="1803" height="674" alt="Screenshot 2025-07-27 134524" src="https://github.com/user-attachments/assets/abd0e6cb-b732-4319-b577-4c4671715b89" />
<img width="1919" height="1094" alt="Screenshot 2025-07-27 134714" src="https://github.com/user-attachments/assets/3cf34c75-9c83-404e-b4e7-840c381e47a2" />
<img width="1916" height="1199" alt="Screenshot 2025-07-27 120149" src="https://github.com/user-attachments/assets/ae8a1a3d-3865-40b6-8eb2-509b51f03871" />
<img width="1803" height="674" alt="Screenshot 2025-07-27 134524" src="https://github.com/user-attachments/assets/d046b445-8256-4799-a54e-1b895db73d0a" />
enshot 2025-07-27 134714" src="https://github.com/user-attachments/assets/9580906d-0ba6-4edb-ab33-b6cb1141f424" />
-b169-4772-b246-1be1d4e39e11" />
<img width="1919" height="1094" alt="Screenshot 2025-07-27 134714" src="https://github.com/user-attachments/assets/98f93510-920d-45d3-a918-9bf489618842" />
<img width="1916" height="1195" alt="Screenshot 2025-07-27 135428" src="https://github.com/user-attachments/assets/6d3424fe-28d2-42c3-b951-ebfb63778cfc" />
<img wi<img width="1919" height="1148" alt="Screenshot 2025-07-28 121706" src="https://github.com/user-attachments/assets/a85255ab-1e92-43fc-ade5-fad48ca5204f" />
<img width="1916" height="1195" alt="Screenshot 2025-07-27 135428" src="https://github.com/user-attachments/assets/88dd093a-1f66-43b6-8e87-b5c6eb437914" />
dth="1919" height="1094" alt="Screenshot 2025-07-27 134714" src="https://github.com/user-attachments/assets/b28b1631-9f77-4e42-a6a2-101d9b4f711a" />
<img width="1803" height="674" alt="Screenshot 2025-07-27 134524" src="https://github.com/user-attachments/assets/46d72c69-dafc-4671-9333-2b6708d67a80" />
<img width="1803" height="674" alt="Screenshot 2025-07-27 134524" src="https://github.com/user-attachments/assets/124cd1bf-b222-422e-a177-5dd38d0c6c70" />
<img width="1916" height="1199" alt="Screenshot 2025-07-27 120149" src="https://github.com/user-attachments/assets/f270e6c1-dc1f-4647-864b-425831039d06" />
<img width="1919" height="1148" alt="Screenshot 2025-07-28 121706" src="https://github.com/user-attachments/assets/69fa8b26-ab4c-45be-984d-e41855a47de3" />
