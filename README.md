# DevOps-Project-1
Built using Java Swing for the GUI and JDBC for database connectivity.
# Deploy Java Application on AWS 3-Tier Architecture

---
# Project Overview

## Introduction

This project demonstrates the deployment of a production-grade Java web application using AWS's robust 3-tier architecture. The implementation follows cloud-native best practices, ensuring high availability, scalability, and security across all application tiers.

### Key Features

- **High Availability**: Multi-AZ deployment with automated failover
- **Auto Scaling**: Dynamic resource allocation based on demand
- **Security**: Defense-in-depth approach with multiple security layers
- **Monitoring**: Comprehensive logging and monitoring setup
- **Cost Optimization**: Efficient resource utilization and management

## Architecture Overview

### Infrastructure Components

1. **Presentation Tier (Frontend)**
   - Nginx web servers in Auto Scaling Group
   - Public-facing Network Load Balancer
   - CloudFront Distribution for static content

2. **Application Tier (Backend)**
   - Apache Tomcat servers in Auto Scaling Group
   - Internal Network Load Balancer
   - Session management with Amazon ElastiCache

3. **Data Tier**
   - Amazon RDS MySQL in Multi-AZ configuration
   - Automated backups and point-in-time recovery
   - Read replicas for read-heavy workloads

### Network Architecture

- **VPC Design**
  - Two separate VPCs (192.168.0.0/16 and 172.32.0.0/16)
  - Public and private subnets across multiple AZs
  - Transit Gateway for inter-VPC communication
