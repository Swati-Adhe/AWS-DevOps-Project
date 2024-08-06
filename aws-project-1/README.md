# BridgeSync Hub Database Optimization and Deployment

## Introduction

**OrionCloud Innovations** is a cloud services provider specializing in helping businesses migrate and manage their applications on Amazon Web Services (AWS). One of their clients, **BridgeSync Hub**, an emerging startup, approached them to deploy a scalable and reliable database solution for their address book application.

**Problem Description:**
BridgeSync Hub was facing issues with database performance, scalability, and availability. They wanted to ensure a seamless user experience and eliminate downtime or data loss. To address these concerns, OrionCloud Innovations proposed a solution that involved:

1. Deploying an RDS Aurora MySQL instance within a private subnet of a VPC.
2. Configuring a web service on an EC2 instance to interact with the RDS Aurora (MySQL).
3. Conducting tests to add, modify, and delete contacts in a simple address book stored in the RDS database through the web browser.

**Tasks:**
1. Create a VPC and the respective security group.
2. Create an RDS Aurora MySQL instance.
3. Connect RDS with the web app server.
4. Access RDS from the EC2 instance.
5. Connect to RDS Aurora.

## Prerequisites

1. **AWS EC2 Instance**: A running EC2 instance with appropriate SSH key and security group settings.
2. **RDS Aurora MySQL Instance**: An RDS Aurora MySQL instance set up within your VPC.
3. **MySQL Client**: Installed on the EC2 instance for database management.

## Steps to Implement

### 1. Create a VPC and Security Group

- **Create a VPC**: Set up a Virtual Private Cloud (VPC) with appropriate subnets.
- **Configure Security Group**: Define inbound and outbound rules to allow necessary traffic.

### 2. Create an RDS Aurora MySQL Instance

- **Choose Database Engine**: Select Amazon Aurora MySQL.
- **Configure Instance**: Set instance size, storage, and other parameters.
- **Enable Multi-AZ Deployment**: Ensure high availability and failover support.
- **Monitor with CloudWatch**: Set up CloudWatch for monitoring performance and resource utilization.

### 3. Configure EC2 Instance

- **Set Up EC2 Instance**: Deploy an EC2 instance and configure it with necessary software (e.g., LAMP stack).
- **Connect to RDS Aurora**: Configure the EC2 instance to connect to the RDS Aurora MySQL instance.

## Database Operations

To perform common database operations, use the following commands:

1. **Show Databases:**
   ```sql
   SHOW DATABASES;

2. **Use a Database:**
   ```sql
   USE <database-name>;

3. **Show Tables:**
   ```sql
   SHOW TABLES;

4. **Query Data:**
   ```sql
   SELECT * FROM <table-name>;

## Conclusion
The **"BridgeSync Hub Database Optimization and Deployment"** project successfully established a robust database setup, improving performance and reliability for the BridgeSync Hub address book application. This setup ensures a scalable and stable database environment, supporting the application's growth and stability.
