

# 🚀 Secure Chat Application with Kubernetes, GitOps & AWS

A microservices-based real-time chat application deployed using Kubernetes and modern DevOps practices. This project demonstrates GitOps workflows, secure secret management, and infrastructure provisioning using Terraform.




## ✨ Features


* **Real-time Messaging**: Send and receive messages instantly using Socket.io 
* **User Authentication & Authorization**: Securely manage user access with JWT 
* **Scalable & Secure Architecture**: Built to handle large volumes of traffic and data 
* **Modern UI Design**: A user-friendly interface crafted with React and TailwindCSS 
* **Profile Management**: Users can upload and update their profile pictures 
* **Online Status**: View real-time online/offline status of users 




## 📌 Project Overview

This project showcases an end-to-end DevOps implementation of a chat application using:

- Kubernetes for container orchestration  
- ArgoCD for GitOps-based continuous deployment  
- Terraform for infrastructure provisioning  
- AWS Secrets Manager for secure secret handling  

The system is designed to reflect real-world production architecture with a focus on **security, automation, and scalability**.

### 📝 Environment Configuration

Create a `.env` file in the root directory with the following configuration:

```env
# Database Configuration
MONGODB_URI=mongodb://root:admin@mongo:27017/chatApp?authSource=admin&retryWrites=true&w=majority

# JWT Configuration
JWT_SECRET=your_jwt_secret_key

# Server Configuration
PORT=5001
NODE_ENV=production
``

---

## 🏗️ Architecture

Frontend (React)  
↓  
Backend (Node.js / Express)  
↓  
MongoDB Database  

Deployed on Kubernetes (multi-service architecture)  
Managed via ArgoCD (GitOps)  
Secrets managed via AWS Secrets Manager + CSI Driver  

---

## 🔧 Tech Stack

- Frontend: React.js  
- Backend: Node.js (Express)  
- Database: MongoDB  
- Containerization: Docker  
- Orchestration: Kubernetes  
- GitOps: ArgoCD  
- Infrastructure as Code: Terraform  
- Cloud Services: AWS (IAM, Secrets Manager, ALB-ready setup)  

---

## 🔐 Security Implementation

- Used AWS Secrets Manager instead of hardcoded credentials  
- Integrated Secrets Store CSI Driver to inject secrets into Kubernetes pods  
- Avoided storing sensitive data in Kubernetes manifests  

---

## ⚙️ DevOps Workflow

1. Infrastructure provisioned using Terraform  
2. Kubernetes cluster configured with IAM roles and permissions  
3. Application manifests stored in Git repository  
4. ArgoCD continuously syncs and deploys changes (GitOps)  
5. Application tested locally using Kubernetes port-forwarding  

---

## 📊 Current Status

- Frontend and backend services deployed successfully  
- Chat functionality working locally  
- API endpoint /api/messages under debugging (integration in progress)  
- ALB-based public exposure under development  

---

## 🚀 How to Run Locally

### 1. Clone the repository
git clone https://github.com/<your-username>/<repo-name>.git  
cd <repo-name>

### 2. Apply Kubernetes manifests
kubectl apply -f .

### 3. Port-forward services
kubectl port-forward svc/frontend 8080:80  
kubectl port-forward svc/backend 5001:5001  

### 4. Access application
http://localhost:8080  

---

## 📸 Screenshots

- ArgoCD Application Dashboard  
- AWS Secrets Manager Integration  
- Chat Application UI  

---

## 💡 Key Learnings

- Implemented GitOps workflow using ArgoCD  
- Learned secure secret management with AWS Secrets Manager  
- Gained hands-on experience with Kubernetes microservices deployment  
- Debugged real-world frontend-backend communication issues  

---

## 🔮 Future Improvements

- Fix API routing and /api/messages endpoint  
- Deploy application on AWS EKS with ALB ingress  
- Enable public access with proper domain configuration  
- Add CI/CD pipeline (Jenkins / GitHub Actions)  

---

## 🤝 Contributing

Contributions, issues, and suggestions are welcome!

---

## 📬 Contact

Feel free to connect with me on LinkedIn for collaboration or opportunities.

---

## ⭐ If you found this project useful, give it a star!














