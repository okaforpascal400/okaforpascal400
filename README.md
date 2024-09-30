# Architecting Enterprise Web Application on AWS Cloud using (PAAS & SAAS)

This project demonstrates how to architect a web application using AWS Cloud services. Below are the steps to implement the solution.

## Table of Contents
1.  Project Overview
2.  Step by step execution
3.  Tools and Services
4.  Prerequisites
5.  Conclusion

---

## Project Overview

The objective of this project is to build and deploy a web application on AWS using various services like Elastic Beanstalk, RDS, Elastic Cache, and more. This guide walks through the setup and deployment process.

---

## Step by step execution is as follows:

1. Login to AWS Account.
2. Create a key pair for the Beanstalk instance.
3. Configure a security group for ElastiCache, RDS, and ActiveMQ to ensure controlled and secure network access.
4. ![Screenshot 2024-09-24 122502](https://github.com/user-attachments/assets/778c6720-a719-4d0b-8a82-ce76093fcc95)

5. Create RDS, Amazon ElasticCache, Amazon ActiveMQ.
 Amazon RDS (Relational Database Service): Create an RDS instance to serve as the database for your application. RDS provides a scalable, managed relational database service, supporting engines like MySQL, PostgreSQL, and SQL Server. For this project, the database will store critical backend data and provide high availability.
 
 ![Screenshot 2024-09-28 041814](https://github.com/user-attachments/assets/54e5f447-d9d6-4bac-9b89-5ca19146ff9f)

6. Create an Elastic Beanstalk environment.
10. ![Screenshot 2024-09-28 041401](https://github.com/user-attachments/assets/83ea1f16-7763-407b-8aba-49c7d3d7c54d)

11. Update the security group of the backend to allow traffic from the Beanstalk security group.
12. Update the security group of the backend to allow internal traffic.
13. ![Screenshot 2024-09-24 122017](https://github.com/user-attachments/assets/522a79b3-ddf6-489a-93d1-483c3a904e79)

14. Launch an EC2 instance for DB initializing.
15. Login to the instance and initialize the RDS DB.
16. ![Screenshot 2024-09-28 002210](https://github.com/user-attachments/assets/62b492e6-89bd-4024-9266-15d3a2d5f996)

17. Add a 443 HTTPS listener to the Elastic Load Balancer.
18. Build artifacts with backend information.
19. ![image](https://github.com/user-attachments/assets/745ed473-8fc4-41f0-a3ee-7d2792d60160)

20. Deploy artifacts to Beanstalk.
21. ![Screenshot 2024-09-28 041200](https://github.com/user-attachments/assets/f9477e31-5afc-4a1a-987b-08cdfaf28445)

22. Create an entry in GoDaddy DNS Zones for domain management.
23. ![Screenshot 2024-09-28 030232](https://github.com/user-attachments/assets/fd497a57-fb92-490c-83a1-a961cedd7412)


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
