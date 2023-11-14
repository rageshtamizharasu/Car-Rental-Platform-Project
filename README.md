# Car Rental System

## Overview

The Car Rental System is a sophisticated web-based application built with Java Core and Maven, utilizing microservices architecture orchestrated by Kubernetes. This project adheres to core principles, ensuring scalability, reliability, and efficient deployment. Furthermore, the system embraces modern DevOps practices, incorporating Docker for containerization and Kubernetes for orchestration. The following sections delve into key principles, including Disaster Recovery (DR) strategies.

## Principles

### 1. Microservices Architecture

The system employs a microservices architecture, breaking down the application into independently deployable services. Each microservice focuses on a specific business capability, promoting modularity, flexibility, and ease of maintenance.

### 2. Containerization with Docker

Docker containers encapsulate each microservice, ensuring consistency across various environments. The use of Docker allows for seamless deployment, scaling, and management of application components, fostering a reliable and reproducible deployment pipeline.

### 3. Orchestration with Kubernetes

Kubernetes orchestrates Docker containers, providing automated deployment, scaling, and management. This ensures high availability, fault tolerance, and efficient resource utilization, crucial for a scalable and reliable application.

### 4. Infrastructure as Code (IaC) with Terraform

Infrastructure provisioning is automated with Terraform, adhering to the principles of Infrastructure as Code (IaC). This enables consistent and repeatable infrastructure deployment, reducing the risk of configuration drift and promoting version control for infrastructure changes.

### 5. Continuous Integration and Continuous Deployment (CI/CD) with Jenkins

Jenkins is employed for CI/CD pipelines, automating the software delivery process. This includes building, testing, and deploying the application. CI/CD practices ensure rapid and reliable releases, enhancing the overall development lifecycle.

## Disaster Recovery (DR) Strategies

### 1. Pilot Light DR Strategy

The Car Rental System implements a Pilot Light DR strategy, maintaining a minimal version of the primary production environment in AWS. Key components include:
![DR-strategy](https://github.com/rageshtamizharasu/Car-Rental-Platform-Project/assets/39893176/57896c55-dd9f-4484-bc76-154184ca4c4f)

- **Amazon RDS:**
  - Multi-AZ deployment for high availability and automatic failover.
  - Automated backups to ensure data integrity.

- **Amazon S3:**
  - Stores critical backups, configuration files, and essential data.
  - Lifecyle policies manage data and log retention.

- **EC2 Instances:**
  - Minimal instances maintained in a stopped state, ready for rapid scaling in case of disaster.

- **Amazon Route 53:**
  - Manages DNS to redirect traffic to the standby environment when a disaster is detected.

### 2. Kubernetes Stateful Deployment

Kubernetes provides stateful deployment for the Car Rental System, ensuring data consistency and reliability. This includes:

- **Persistent Volumes (PVs):**
  - Used to persist data for stateful applications.
  - PVs are dynamically provisioned and managed by Kubernetes.

- **Rolling Updates:**
  - Kubernetes deployment strategies, such as rolling updates, guarantee seamless updates and high availability.

### 3. Regular DR Drills

Regular Disaster Recovery drills are conducted to validate the effectiveness of the implemented strategies. These drills include:

- **Simulated Failovers:**
  - Testing failover procedures for RDS and EC2 instances.
  - Evaluating the effectiveness of Route 53 redirection.

- **Kubernetes Cluster Failovers:**
  - Simulating failures and monitoring Kubernetes cluster behavior during these events.

### 4. Monitoring and Logging

Comprehensive monitoring and logging practices are implemented using tools like Prometheus, Splunk, and AWS CloudTrail. These tools provide:

- **Real-time Monitoring:**
  - Monitoring of application and infrastructure health.
  - Immediate alerts for any anomalies.

- **Log Analysis:**
  - Analyzing logs for troubleshooting and identifying potential issues.
  - Enhancing overall system observability.

## Getting Started

### Prerequisites:

- AWS Account with necessary permissions.
- Java Development Kit (JDK) installed.
- Maven installed locally.
- Docker and Kubernetes installed.
- Access to Jenkins for CI/CD setup.

### Usage
## Customer Workflow:

Register for an account or log in.
Browse available cars and make reservations.
View and manage bookings on the user dashboard.
Administrator Workflow:

Log in as an administrator.
Manage car inventory, bookings, and customer accounts.
Generate reports and analytics.

## Conclusion
The Car Rental System embodies a comprehensive and modern approach to web application development. It leverages microservices, containerization, and orchestration to provide a scalable, reliable, and efficient car rental experience. The implementation of Disaster Recovery strategies ensures business continuity, while the CI/CD pipelines and DevOps practices streamline the development lifecycle.

## Contact
For questions or support, contact Ragesh at rageshtamizharasu@outlook.com

This markdown content can be used as the README file for your Git repository. Please replace placeholders such as Ragesh and Team Members with your actual details. Additionally, consider adding images or diagrams to enhance the visual appeal of the README.




