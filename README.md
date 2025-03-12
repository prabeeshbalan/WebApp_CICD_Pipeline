# 🚀 CI/CD Pipeline for Kubernetes-Based Web Application on AWS

## 📌 Overview

This project automates the deployment of a web application using a complete **CI/CD pipeline** with **Terraform, Ansible, Jenkins, Kubernetes, GitHub, and AWS**.

## 🛠️ Tech Stack & Tools

| Tool                             | Purpose                                                                          |
| -------------------------------- | -------------------------------------------------------------------------------- |
| **Terraform**                    | Infrastructure as Code (IaC) to provision AWS services (EKS, EC2, S3, IAM, etc.) |
| **Ansible**                      | Server configuration & application deployment                                    |
| **Jenkins**                      | CI/CD automation (trigger on GitHub commits, build Docker images, deploy to EKS) |
| **Kubernetes (EKS)**             | Orchestration for microservices & containerized apps                             |
| **Docker**                       | Containerizing the application                                                   |
| **GitHub**                       | Source code management & Jenkins webhook triggers                                |
| **AWS (EKS, S3, IAM, EC2, RDS)** | Cloud hosting infrastructure                                                     |

## 🚀 Architecture & Workflow

1. **Terraform provisions AWS resources**:

   - EKS Cluster
   - EC2 instance (Jenkins Server)
   - S3 for storing Terraform state
   - IAM roles & policies

2. **Jenkins Pipeline Automation**:

   - Triggers on GitHub commit (webhook).
   - Builds Docker image & pushes to Amazon ECR.
   - Deploys updated app to Kubernetes (EKS).

3. **Ansible configures Jenkins & Kubernetes**:

   - Installs required dependencies.
   - Configures Jenkins plugins & jobs.

4. **Kubernetes (EKS) Deployment**:

   - Deploys microservices using **Helm charts** or Kubernetes manifests.

## 🔧 Setup & Usage

### 1️⃣ Clone Repository

```sh
git clone https://github.com/heroku/node-js-sample.git
cd node-js-sample
```

### 2️⃣ Initialize & Apply Terraform

```sh
terraform init
terraform apply
```

### 3️⃣ Configure Jenkins Server (Ansible)

```sh
ansible-playbook -i inventory install_jenkins.yml
```

### 4️⃣ Deploy Web App to Kubernetes (EKS)

```sh
kubectl apply -f k8s/deployment.yml
```

### 5️⃣ Run Locally (Optional)

```sh
npm install
npm start
```

## 🎯 Expected Outcome

- **Code commit to GitHub** triggers Jenkins build.
- Jenkins **builds Docker image** & **pushes to Amazon ECR**.
- Jenkins **deploys the application** to **Kubernetes (EKS)**.
- Application runs in **AWS cloud, managed via Kubernetes**.

## ✅ Key Benefits

✔ **Automated Infrastructure** (Terraform)\
✔ **Consistent Configuration Management** (Ansible)\
✔ **Continuous Integration & Deployment** (Jenkins)\
✔ **Scalable Microservices Deployment** (EKS)\
✔ **Version Control & Webhooks** (GitHub)\
✔ **AWS Cloud Native Approach** (EKS, EC2, ECR, IAM)

## 🎯 Next Steps

- Implement **Helm charts** for Kubernetes deployment.
- Add **Prometheus & Grafana** for monitoring.
- Configure **AWS ALB Ingress** for external access.
- Integrate **GitHub Actions** for alternative CI/CD approach.

## 📜 License

This project is open-source and licensed under the MIT License.

