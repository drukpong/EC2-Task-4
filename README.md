# AWS EC2 Task 4 — Install and Verify Docker

## Overview

This task involved installing Docker on an Ubuntu EC2 instance running on AWS and verifying that Docker could successfully run a container.

## Objectives

- Launch an AWS EC2 Ubuntu instance.
- Connect to the instance using SSH.
- Install Docker.
- Start and enable the Docker service.
- Verify the Docker installation.
- Run a test Docker container.

## Steps Taken

### 1. Launched an EC2 Instance

Created a new Ubuntu EC2 instance for Task 4.

The Security Group was configured to allow:

- SSH — TCP port 22 — My IP

HTTP and HTTPS were not required because this task focused on Docker installation and verification.

### 2. Connected to the EC2 Instance

Connected to the Ubuntu EC2 instance using SSH and the existing EC2 key pair.

### 3. Updated the Server

Updated the Ubuntu package lists using:

```bash
sudo apt update

### 4. Installed Docker

Installed Docker using:

sudo apt install docker.io -y

### 5. Started Docker

Started the Docker service:

sudo systemctl start docker

Enabled Docker to start automatically after a reboot:

sudo systemctl enable docker

### 6. Verified Docker Service

Checked the Docker service status using:

sudo systemctl status docker

Docker was confirmed to be:

Active: active (running)

### 7. Verified Docker Version

Checked the installed Docker version using:

docker --version

Docker returned its installed version successfully.

### 8. Tested Docker with a Container

Ran the Docker Hello World container:

sudo docker run hello-world

Docker successfully downloaded and ran the test image.

The output included:

Hello from Docker!

This confirmed that Docker was installed correctly and could successfully create and run containers.

### Difficulty Faced

No major technical difficulty was encountered during the Docker installation.

The installation, service configuration, version check, and container test were completed successfully.

### What I Learned
How to install Docker on Ubuntu.
How to start and enable the Docker service using systemctl.
How to verify the Docker service status.
How to check the installed Docker version.
How to run a Docker container.
How the hello-world image can be used to verify a Docker installation.

### Verification

Docker was successfully installed and configured on the AWS EC2 Ubuntu instance.

The Docker service was running, and the hello-world container executed successfully.

### Conclusion

Task 4 was successfully completed. Docker was installed on an AWS EC2 Ubuntu instance, configured to start automatically, verified, and tested by successfully running a Docker container.
