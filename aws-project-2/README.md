# Multi-Region Containerized Application Deployment on AWS

## Overview

This project implements a multi-region, containerized application environment on AWS using **Infrastructure as Code (IaC)** with **AWS CloudFormation**. The architecture is designed for high availability, disaster recovery, and automated CI/CD pipelines, with continuous monitoring and alerting for proactive management.

## Key Features

- **Multi-Region High Availability**: Deploys an Amazon ECS cluster to manage Docker containers, utilizing Amazon ECR for image storage. Route 53 handles traffic routing across multiple AWS regions to ensure seamless performance.
- **Disaster Recovery**: Sets up a disaster recovery strategy by replicating resources and data across AWS regions.
- **CI/CD Pipeline Automation**: Automates the CI/CD process using AWS CodePipeline, with integration for CodeBuild and CodeDeploy. A manual approval stage ensures controlled deployment to production environments.
- **Infrastructure as Code (IaC)**: Uses AWS CloudFormation to define, provision, and manage infrastructure across regions, ensuring consistency and rapid replication.
- **Monitoring and Alerts**: Implements AWS CloudWatch for monitoring CPU, memory, and ECS service health, with SNS notifications for real-time alerts on any anomalies.

## Architecture

- **Amazon ECS**: Manages the containerized application across multiple regions.
- **Amazon ECR**: Stores Docker images for the application.
- **AWS CloudFormation**: Used for deploying infrastructure as code, ensuring high availability and disaster recovery across regions.
- **AWS CodePipeline**: Automates the CI/CD pipeline, integrating CodeBuild for building Docker images and CodeDeploy for deployment.
- **CloudWatch & SNS**: Provides continuous monitoring and sends alerts when thresholds (e.g., high CPU usage) are crossed.


