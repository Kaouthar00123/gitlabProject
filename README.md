# CI/CD Pipeline with GitLab CI for Spring Boot Application

This project demonstrates the implementation of Continuous Integration and Continuous Delivery (CI/CD) using GitLab CI. The application is a simple Spring Boot Java application, and the CI/CD pipeline is defined in the `.gitlab-ci.yml` file located in the root directory.

## Project Overview

The `.gitlab-ci.yml` script automates the following processes:
- **Build**: Compiles the application.
- **Test**: Runs automated tests.
- **Deploy**: Deploys the application to the desired environment.

## Pipeline Configuration

### Triggers
The pipeline is triggered based on specific events, such as:
- Pushing to a particular branch.
- Specific events defined in the `rules` section of the script.

### Global Variables
The script includes global variables that are used throughout the pipeline. These variables include:
- Docker image name.
- Docker image tag.

### Jobs
Each job in the pipeline is associated with a specific stage, defined under the `stage` keyword. The stages include:
- **Build**: Compiles the application.
- **Test**: Runs automated tests.
- **Deploy**: Deploys the application.

Each stage specifies:
- The Docker image to be used for execution.
- The script to be executed within that stage.

### Secure Credentials
The pipeline uses secure credentials to access external accounts, such as Docker Hub, for image pushing and pulling operations.