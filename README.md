# Architecting Web Application on AWS Cloud using (PAAS & SAAS)

This project demonstrates how to architect a web application using AWS Cloud services. Below are the steps to implement the solution.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Flow of Execution](#flow-of-execution)
3. [Tools and Services](#tools-and-services)
4. [Prerequisites](#prerequisites)
5. [Step-by-Step Execution](#step-by-step-execution)
6. [Conclusion)

---

## Project Overview

The objective of this project is to build and deploy a web application on AWS using various services like Elastic Beanstalk, RDS, Elastic Cache, and more. This guide walks through the setup and deployment process.

---

## Flow of Execution

The flow of execution is as follows:

1. Login to AWS Account.
2. Create a key pair for the Beanstalk instance.
3. Configure a security group for ElastiCache, RDS, and ActiveMQ to ensure controlled and secure network access.
4. ![Screenshot 2024-09-24 122502](https://github.com/user-attachments/assets/778c6720-a719-4d0b-8a82-ce76093fcc95)

5. Create RDS, Amazon ElasticCache, Amazon ActiveMQ.
6. Create an Elastic Beanstalk environment.
7. Update the security group of the backend to allow traffic from the Beanstalk security group.
8. Update the security group of the backend to allow internal traffic.
9. Launch an EC2 instance for DB initializing.
10. Login to the instance and initialize the RDS DB.
11. Add a 443 HTTPS listener to the Elastic Load Balancer.
12. Build artifacts with backend information.
13. Deploy artifacts to Beanstalk.
14. Create an entry in GoDaddy DNS Zones for domain management.

---

## Tools and Services

- **AWS Elastic Beanstalk**: For managing web app deployment.
- **Amazon RDS**: To manage the relational database.
- **Amazon ElasticCache**: To provide in-memory data store services.
- **Amazon ActiveMQ**: For message queuing services.
- **EC2**: Virtual servers for computing.
- **GoDaddy DNS**: For domain and DNS zone management.

---

## Prerequisites

Before starting, ensure the following:

1. An active AWS account.
2. A GoDaddy account for DNS management.
3. AWS CLI installed and configured on your machine.
4. Git installed and set up on your machine.

---

## Step-by-Step Execution

### Step 1: Login to AWS Account
Login to your AWS account via the AWS Console or using the AWS CLI:
```bash
aws configure
