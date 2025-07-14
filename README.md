# 🐳 Containerized Microservices with AWS EKS

This project demonstrates how to design, deploy, and manage a containerized microservices architecture using AWS services such as **EKS (Elastic Kubernetes Service)**, **ECR**, **CodePipeline**, and **ALB**.

🔗 **GitHub Repository**: [https://github.com/Mithra1995/ekscode](https://github.com/Mithra1995/ekscode)

---

## 📌 Objective

To build a robust, scalable, and secure infrastructure for running containerized microservices on the cloud using Docker, Kubernetes (EKS), and AWS DevOps services.

---

## 🧱 Architecture Overview

The project architecture includes:

- **EKS**: For managing Kubernetes clusters and deploying services.
- **ALB**: To route traffic to the right microservices.
- **ECR**: For storing Docker images securely.
- **VPC**: To isolate and control networking.
- **CloudWatch**: For monitoring and logging.
- **CodePipeline**: To automate the CI/CD workflow.

---

## 🛠️ Services Used

- ✅ Amazon EKS
- ✅ Application Load Balancer (ALB)
- ✅ Amazon VPC
- ✅ Amazon ECR
- ✅ AWS CodePipeline
- ✅ AWS CloudWatch
- ✅ Docker

---

## 🚀 Step-by-Step Implementation

1. **Push Code to GitHub**
   - Repository: [ekscode](https://github.com/Mithra1995/ekscode)

2. **Create ECR Repository**
   - Used to store and version Docker images.

3. **Provision EKS Cluster**
   - Created using AWS CloudShell or Terraform.

4. **Set Up AWS CodePipeline**
   - Source: GitHub repository
   - Build: CodeBuild with `buildspec.yml`
   - Deploy: kubectl applies manifest to EKS

5. **Deploy Microservices**
   - Validate `Deployment` and `Service` are created using:
     ```bash
     kubectl get deployments
     kubectl get svc
     ```

6. **Verify Load Balancer**
   - Access the application through the DNS of the ALB created.

7. **Artifacts**
   - Deployment and service manifests (`deployment.yaml`, `service.yaml`) are stored in S3 as output artifacts.

---

## 📄 Deployment Manifests

```yaml
# deployment.yaml
apiVersion: apps/v1
kind: Deployment
...


# service.yaml
apiVersion: v1
kind: Service
...
