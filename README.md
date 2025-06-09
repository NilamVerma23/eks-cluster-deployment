# EKS Cluster Setup with Deployment on AWS

This is a small project I worked on to practice setting up an EKS cluster on AWS from scratch. It includes creating a custom VPC using CloudFormation, setting up the EKS cluster, configuring a node group, and deploying a basic containerized app using Kubernetes.

The goal was to get hands-on experience with infrastructure provisioning and Kubernetes on AWS—something that's highly relevant for DevOps and cloud-native roles.

---

## Project Structure

eks-cluster-deployment/
│
├── README.md
├── cloudformation/
│ └── amazon-vpc.yaml
├── kubernetes/
│ └── deployment.yaml
├── screenshots/
│ ├── vpc-stack-complete.png
│ ├── eks-cluster-active.png
│ └── node-group-active.png
└── docs/
└── eks-cluster-setup-guide.md


---

## Tools & Technologies Used

- **AWS CloudFormation** – for setting up the VPC
- **Amazon EKS** – managed Kubernetes service
- **eksctl** and **AWS CLI** – for creating and configuring the cluster
- **kubectl** – for interacting with the Kubernetes cluster
- **Docker** – used indirectly for understanding the containerized app
- **Linux CLI** – all tasks performed on a terminal

---

## What I Did (Summary)

- Uploaded a VPC YAML template via AWS CloudFormation to set up the networking
- Created an EKS cluster from the AWS Console and attached the IAM role and VPC
- Set up a Node Group for worker nodes
- Used `aws eks` and `kubectl` to connect to the cluster from CLI
- Deployed a simple Node.js-based web app with 3 replicas using a Kubernetes Deployment
- Verified everything using `kubectl get nodes`, `get pods`, etc.

---

## Screenshots

I've added a few screenshots in the `screenshots/` folder to show the working status at each step:
- VPC stack creation complete
- EKS cluster status as Active
- Node group created and ready

---

## Setup Guide

I’ve written a step-by-step guide for the full setup process. You can find it here:- [docs/eks-cluster-setup-guide.md](./docs/eks-cluster-setup-guide.md)

---

## To Check if It’s Working

Once everything is done, these commands will show the running resources:

kubectl get nodes
kubectl get deployments
kubectl get pods

---

## Why This Project?
I wanted to get more hands-on with AWS and Kubernetes, especially working with EKS. This was a great way to understand how the pieces fit together—from infrastructure provisioning to actual app deployment.

---

## It also helped me practice:
Working with CloudFormation templates
IAM roles and networking on AWS
Managing Kubernetes deployments

---

## About Me
Hi, I'm Nilam Verma.
I’m exploring cloud-native technologies and DevOps tools to build scalable, automated solutions. Always learning and improving.

GitHub: @NilamVerma23
LinkedIn: linkedin.com/in/nilam-verma-4b8256244/
