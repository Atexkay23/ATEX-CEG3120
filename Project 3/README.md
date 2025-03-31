# Project 3: CloudFormation Web Server with HAProxy Load Balancer

## Overview
This project involves deploying a web application using **AWS CloudFormation**, setting up **nginx** or **apache2** as a web server, and configuring **HAProxy** as a load balancer. The project is hosted on **AWS EC2 instances** and uses a **CloudFormation template** for deployment automation.

# Folder Structure:


## Prerequisites
- An **AWS account** with EC2 access.
- **AWS CLI** installed and configured.
- **CloudFormation permissions** in AWS IAM.
- **SSH access** to EC2 instances.
- Basic knowledge of Linux commands and AWS networking.

## Deployment Steps
```bash
git clone https://github.com/Atexkay23/ATEX-CEG3120/Project3
cd Project3

aws cloudformation create-stack --stack-name Project3Stack \
    --template-body file://cloudformation-template.yaml \
    --capabilities CAPABILITY_IAM

chmod +x webserver-setup.sh
./webserver-setup.sh

ssh -i your-key.pem ubuntu@<WebServer-Public-IP>
chmod +x haproxy-setup.sh
./haproxy-setup.sh
