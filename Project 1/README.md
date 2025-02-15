# Project 1 - Part 1: Build a VPC

## 1. VPC
**Description:**  
A VPC (Virtual Private Cloud) is a logically isolated section of the AWS cloud where you can launch AWS resources in a virtual network. It allows you to define your own IP address range, create subnets, configure route tables, and set up network gateways. A VPC provides control over your network environment, including security settings and connectivity options.

**Screenshot:**  
![VPC Configuration](Project/ScreenShots/VPC.png)  


---

## 2. Subnet
**Description:**  
A subnet is a range of IP addresses within a VPC where you can place groups of isolated resources, such as EC2 instances. Subnets allow you to segment your network and control traffic flow between different parts of your infrastructure.

**Prompt Responses:**  
- **Reserved block for the subnet:** `172.18.0.0/24` (IP range: `172.18.0.0` to `172.18.0.255`).  
- **Remaining block(s) in the VPC:** `172.18.1.0/24` (since the VPC CIDR is `172.18.0.0/23`).

**Screenshot:**  
![Subnet Configuration](Project/ScreenShots/Subnet.png)  


---

## 3. Internet Gateway
**Description:**  
An Internet Gateway (IGW) is a horizontally scaled, redundant, and highly available VPC component that allows communication between resources in your VPC and the internet. It provides a target in your VPC route tables for internet-routable traffic.

**Screenshot:**  
![Internet Gateway Configuration](Project/ScreenShots/GateWay.png)  


---

## 4. Route Table
**Description:**  
A route table contains a set of rules (routes) that determine where network traffic from your subnet is directed. Each subnet in your VPC must be associated with a route table, which controls the traffic flow to and from the subnet.

**Screenshot:**  
![Route Table Configuration](Project/ScreenShots/RouteTable.png)  


---

## 5. Security Group
**Description:**  
A security group acts as a virtual firewall for your EC2 instances to control inbound and outbound traffic. It operates at the instance level and supports allow rules only. Security groups are stateful, meaning that return traffic is automatically allowed regardless of the rules.

**Screenshot:**  
![Security Group Configuration](Project/ScreenShots/SecurityGroup.png)  


---

## 6. Network ACL
**Description:**  
A Network ACL (NACL) is a stateless firewall that controls traffic at the subnet level. It supports both allow and deny rules and evaluates rules in order when deciding whether to allow traffic. Unlike security groups, NACLs are stateless, meaning return traffic must be explicitly allowed.

**Screenshot:**  
![Network ACL Configuration](Project/ScreenShots/NetworkACL.png)  


---

## 7. Key Pair
**Description:**  
A key pair consists of a public key (stored by AWS) and a private key (downloaded by you) used to securely connect to your EC2 instances via SSH. The private key must be kept secure, as it is required to access your instances.

**Prompt Responses:**  
- **Public key:** Stored by AWS.  
- **Private key:** Downloaded by you during key pair creation. AWS does not store the private key.

**Screenshot:**  
![Key Pair Configuration](Project/ScreenShots/KeyPair.png)  


---

## 8. Elastic IP
**Description:**  
An Elastic IP (EIP) is a static, public IPv4 address that you can allocate to your AWS account and associate with an EC2 instance. Unlike a public IP, which changes when the instance is stopped and restarted, an Elastic IP remains the same.

**Prompt Responses:**  
- **Elastic IP:** Persistent public IP address that remains the same even if the instance is stopped and restarted.  
- **Public IP:** Automatically assigned to an instance when launched but changes if the instance is stopped and restarted.

**Screenshot:**  
![Elastic IP Configuration](Project/ScreenShots/ElasticIP.png)  

