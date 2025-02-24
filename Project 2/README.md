# Project Description

This project creates a basic testing setup in AWS using CloudFormation. It sets up a network (VPC), an EC2 instance (virtual server), security rules, and other resources.

### What it does:
- Sets up AWS resources automatically
- Creates a secure environment for testing
- Installs useful software like Git, Python, Apache, and Wamerican

---

# Diagram

![AWS Architecture Diagram](./aws-architecture-diagram.png)  

---

# Diagram Explanation

1. **VPC**: The main network where everything is.
2. **Subnet**: A smaller part of the VPC where the EC2 instance is located.
3. **Security Group**: A firewall controlling access to the EC2 instance.
4. **EC2 Instance**: A virtual machine running Ubuntu and software.
5. **Elastic IP**: A fixed IP address for the EC2 instance to connect to the internet.
6. **Route Table**: Directs internet traffic to the EC2 instance.
7. **Network ACL**: Extra security for controlling traffic in and out of the subnet.

---

