# Secure-WordPress-Deployment-on-AWS-Cloud-Security-Project-

This project demonstrates the secure deployment of a WordPress application on an AWS EC2 instance using the LAMP stack (Linux, Apache, MariaDB, and PHP). The main objective of the project was to implement cloud security best practices while deploying and monitoring a functional WordPress environment.

The project includes infrastructure hardening, application security, monitoring, logging, and vulnerability assessment using both AWS-native and third-party security tools.


## Objectives

- Deploy a WordPress website on AWS EC2
- Configure a LAMP stack on Ubuntu 24.04
- Implement infrastructure and application-level security
- Monitor system activity and detect threats
- Perform vulnerability assessment and security testing
- Gain practical experience in cloud security and web application hardening

## Architecture

The application was hosted on an AWS EC2 Ubuntu instance with the LAMP stack installed manually. WordPress was configured on top of the stack, and multiple security and monitoring services were integrated into the environment.

AWS EC2 Instance
│
├── Apache Web Server
├── MariaDB Database
├── PHP
└── WordPress
     ├── Wordfence Security Plugin
     ├── Two-Factor Authentication
     └── Brute Force Protection

Security & Monitoring
├── AWS CloudWatch
├── AWS CloudTrail
├── AWS GuardDuty
└── Datadog

Security Implementations
~Infrastructure Security
~Configured AWS Security Groups
~Restricted inbound traffic to required ports only
~Used SSH key-based authentication
~Applied Linux hardening techniques
~Managed file and directory permissions securely

WordPress Security
~Installed and configured Wordfence
~Enabled brute-force protection
~Enabled two-factor authentication
~Performed malware scanning
~Restricted access to sensitive directories

Monitoring and Logging
~CloudWatch for resource monitoring and alerts
~CloudTrail for activity logging and auditing
~GuardDuty for threat detection
~Datadog for real-time infrastructure monitoring

Security Testing
Nmap: Used for port scanning and identifying exposed services.
Nessus: Used for vulnerability assessment and identifying server misconfigurations.
WPScan: Used to test WordPress-specific vulnerabilities and weak configurations.


Key Findings
Finding	Risk Level
XML-RPC Enabled	Medium
Directory Listing Enabled	Medium
Admin Username Enumeration	Medium
No HTTPS/SSL Configuration	High
Server Information Disclosure	Low
