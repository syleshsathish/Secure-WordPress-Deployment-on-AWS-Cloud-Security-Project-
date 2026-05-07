# Secure WordPress Deployment on AWS

## Overview

This project demonstrates the secure deployment of a WordPress application on an AWS EC2 instance using the LAMP stack (Linux, Apache, MariaDB, and PHP). The main focus of the project was to implement cloud security best practices while configuring, monitoring, and testing a secure WordPress environment.

The project includes infrastructure setup, application hardening, monitoring, logging, and vulnerability assessment using both AWS-native and third-party security tools.

---

## Objectives

- Deploy WordPress on AWS EC2
- Configure a LAMP stack on Ubuntu 24.04
- Implement infrastructure and application-level security
- Monitor and audit system activities
- Perform vulnerability assessments and security testing
- Gain practical experience in cloud and web application security

---

## Technologies and Tools Used

- AWS EC2
- Ubuntu 24.04
- Apache2
- MariaDB
- PHP
- WordPress
- AWS CloudWatch
- AWS CloudTrail
- AWS GuardDuty
- Datadog
- Wordfence
- Nmap
- Nessus
- WPScan
- Kali Linux

---

## Security Implementations

### Infrastructure Security

- Configured AWS Security Groups
- Restricted inbound traffic to required ports only
- Enabled SSH key-based authentication
- Applied Linux server hardening techniques
- Managed secure file and directory permissions

### WordPress Security

- Installed and configured Wordfence
- Enabled brute-force protection
- Configured two-factor authentication
- Performed malware scanning
- Restricted access to sensitive directories

### Monitoring and Logging

- Configured CloudWatch for system monitoring
- Enabled CloudTrail for activity logging
- Enabled GuardDuty for threat detection
- Integrated Datadog for real-time monitoring

---

## Security Testing

### Nmap

Used for:
- Port scanning
- Service detection
- Firewall validation

### Nessus

Used for:
- Vulnerability assessment
- Server exposure analysis

### WPScan

Used for:
- WordPress vulnerability scanning
- Identifying weak configurations

---

## Key Findings

- XML-RPC was enabled and could be exploited for brute-force attacks
- Directory listing was enabled in some WordPress directories
- Admin username enumeration was possible
- HTTPS/SSL was not configured
- Apache server information was exposed in headers

---

## Setup Process

### Connect to EC2 Instance

```bash id="7mxtvj"
ssh -i "Wkey.pem" ubuntu@<public-ip>
