# production-ready-aws-vpc
A hands-on AWS networking project to build a secure, multi-AZ VPC with public/private subnets, routing, NAT Gateway, and basic connectivity testing.
# production-ready-aws-vpc

A hands-on AWS networking project to build a secure, multi-AZ VPC with public/private subnets, routing, NAT Gateway, and connectivity testing.

## Overview

This project demonstrates the deployment of a production-ready AWS Virtual Private Cloud (VPC) using a secure and highly available architecture.

The infrastructure is designed across multiple Availability Zones with public and private subnet separation.

## Architecture Components

- Custom VPC
- 2 Public Subnets
- 2 Private Subnets
- Multi-AZ Deployment
- Internet Gateway
- NAT Gateway
- ## Project Architecture

### Public Layer
- Internet-facing resources
- Public IP enabled
- Routed through Internet Gateway

### Private Layer
- Isolated internal resources
- No direct internet exposure
- Outbound internet access through NAT Gateway

## Network Design

| Resource | CIDR |
|---|---|
| VPC | 10.0.0.0/16 |
| Public-Subnet-A | 10.0.1.0/24 |
| Public-Subnet-B | 10.0.2.0/24 |
| Private-Subnet-A | 10.0.3.0/24 |
| Private-Subnet-B | 10.0.4.0/24 |

## Tasks Completed

### VPC Setup
- Created a custom VPC
- Configured DNS support and hostnames

### Subnet Configuration
- Created 2 public subnets
- Created 2 private subnets
- Distributed resources across 2 Availability Zones

### Internet Connectivity
- Attached an Internet Gateway
- Configured a NAT Gateway in the public subnet

### Route Table Configuration
- Public route table connected to Internet Gateway
- Private route table connected to NAT Gateway

### Monitoring & Logging
- Enabled VPC Flow Logs
- Sent logs to CloudWatch Logs
- Stored logs in Amazon S3

### EC2 Deployment
- Launched EC2 instances in all subnets
- Validated:
  - SSH connectivity
  - HTTP access
  - Private subnet outbound internet access through NAT

## Validation Performed

- SSH access to public EC2 instances
- HTTP testing from browser
- Private EC2 internet access validation
- Route table verification
- Flow log generation verification

## Technologies Used

- AWS VPC
- EC2
- NAT Gateway
- Internet Gateway
- Route Tables
- CloudWatch Logs
- Amazon S3

## Learning Outcome

This project demonstrates practical knowledge of:

- AWS networking fundamentals
- High availability architecture
- Public/private subnet segregation
- Secure internet access design
- AWS monitoring and logging
- Production-grade cloud infrastructure deployment
