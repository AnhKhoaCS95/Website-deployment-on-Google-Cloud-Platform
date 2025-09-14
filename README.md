🚀 Project Overview

This project demonstrates the deployment and management of a secure dynamic website on Google Cloud Platform (GCP) with robust monitoring and automation.

Key Features

VM Creation & Configuration: Created and configured multiple Virtual Machines (VMs) on GCP.

Website Deployment: Hosted a dynamic website using Nginx as the web server.

Secure Deployment: Configured a custom domain with SSL/TLS certificates for secure access (HTTPS).

Set up Google Cloud SQL with MySQL for secure, scalable, and managed database services.

Cloud Networking & DNS Management: Implemented provisioning, DNS configuration, and network setup for reliable connectivity.

Intrusion Detection & Monitoring: Integrated Suricata for intrusion detection and real-time monitoring.

Automation: Set up automated backups using Crontab, reducing manual workload and improving operational efficiency.

Tech Stack

Cloud Platform: Google Cloud Platform (GCP)

Web Server: Nginx

Databases: Cloud SQL, Firestore

Monitoring & Security: Suricata, Firewall Rules

Backup: Crontab

Domain & SSL: buy or get it free on some free domain websites and they also provide free ssl 

Architecture
flowchart LR
    A[User] --> B[Custom Domain + SSL]
    B --> C[Nginx Web Server on GCP VM]
    C --> D[Dynamic Website Backend]
    D --> E[Cloud SQL / Firestore Database]
    C --> F[Suricata IDS for Monitoring]
    G[Crontab Automation] --> E

Highlights

Enhanced security with IDS (Suricata) and HTTPS encryption.

Streamlined operations with automated backups and reduced manual intervention.

Built a scalable cloud architecture ready for production use.
