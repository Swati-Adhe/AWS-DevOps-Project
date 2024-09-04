# AppleBite Co. CI/CD Project

## Project Overview

This project is designed for AppleBite Co., which aims to enhance their software delivery process by implementing Continuous Integration (CI) and Continuous Deployment (CD) using modern DevOps practices. The solution leverages tools such as Git for version control, Jenkins for CI/CD automation, Docker for containerization, and Ansible for configuration management.

### Objective

The main objectives of this project are:
- To automate the build, test, and deployment process of a PHP application.
- To enable faster and more reliable software updates through a streamlined CI/CD pipeline.
- To facilitate collaboration among different development teams and third-party vendors by using modular components and multiple frameworks.

## Technologies Used

- **Git**: Version control system for tracking changes in the code.
- **Jenkins**: Automation server for building, testing, and deploying applications.
- **Docker**: Containerization platform for packaging applications and their dependencies.

## Objectives

- Automatically provision a test server upon code push to the Git master branch.
- Containerize the application and deploy it to the test server.
- Automatically build and push the application to the production server.
- Ensure all processes are triggered from GitHub repository actions.

## Execution Steps

1. Set up a Master VM for Jenkins, Ansible, and Git.
2. Create a fresh instance for the Jenkins Slave Node (Test Server).
3. Configure Jenkins with the Build Pipeline.
4. Manually install OpenSSH server, and Git on the slave node.
5. Use the `devopsedu/webapp` Docker image to host the PHP application, utilizing a Dockerfile.
6. Automate the following tasks through Jenkins pipeline:
   - Install and configure the Puppet agent on the slave node (Job 1).
   - Deploy Ansible configuration on the test server to install Docker (Job 2).
   - Pull the PHP application and Dockerfile from the Git repository, then build and deploy the Docker container (Job 3).
   - If Job 3 fails, automatically delete the running container on the test server.

## Repository Link

- Sample PHP application: [PHP Application GitHub Repository](https://github.com/edureka-devops/projCert.git)

