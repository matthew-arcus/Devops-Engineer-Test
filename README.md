# DevOps Technical Test

## Overview
This test project is designed to demonstrate proficiency in DevOps practices, including CI/CD, infrastructure as code, and cloud deployment. The application is a simple Next.js web app that displays a welcome message.

Your task is to set up a EC2 instance on AWS, configure a CI/CD pipeline to automate the deployment of the Next.js application to the EC2 instance, and ensure that the application is accessible via a web browser.

For the purpose of this test, you will be provided with AWS IAM credentials that have the necessary permissions to create and manage EC2 instances and other required resources. These credentials should also be used to configure the CI/CD pipeline.


## Tasks

### 1. Set Up AWS EC2 Instance
- Write all terraform within the `terraform/` directory.
- Create an EC2 instance with the following specifications:
  - Instance Type: t2.micro
  - Operating System: Amazon Linux 2
  - Security Group: Allow inbound HTTP (port 80) and SSH (port 22) traffic.
- Ensure the instance has a public IP address to be accessible from the internet.
- Configure user data to install all necessary dependencies to run the Next.js application.


### 2. Configure CI/CD Pipeline
- Use GitHub Actions to set up a CI/CD pipeline that automates the deployment process.
- The pipeline should trigger on every push to the `main` branch.
- The pipeline should perform the following steps:
  - Checkout the code from the repository.
  - Install dependencies and build the Next.js application.
  - Use SSH to connect to the EC2 instance and deploy the built application.
  - Start the Next.js application on the EC2 instance, ensuring it runs in the background and restarts on failure.

### 3. Application Deployment
- Ensure that the Next.js application is deployed to the EC2 instance and is accessible via a web browser.
- The application should display a welcome message when accessed.