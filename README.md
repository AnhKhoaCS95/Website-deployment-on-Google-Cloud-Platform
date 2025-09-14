🌐 Secure Dynamic Website Deployment on Google Cloud Platform

![Image](https://github.com/user-attachments/assets/8cc375cc-e53e-419c-9519-c711fdf57c93)

📖 Overview

This project demonstrates how to deploy, secure, and automate a dynamic web application using Google Cloud Platform (GCP) services.
It covers VM provisioning, web hosting with Nginx, intrusion detection, automated backups, cloud database integration, and secure domain management with SSL.

The system also includes a dedicated admin portal to manage products, featuring domain and subdomain configurations for separation between the public-facing website and the admin panel.

🛠 Features
1. Google Cloud Platform Infrastructure

Created and configured Virtual Machine instances using Google Compute Engine.

Managed VPC networking, firewall rules, and DNS configuration for secure traffic flow.

2. Web Hosting with Nginx

Installed and configured Nginx on the VM to host the dynamic website.

Configured reverse proxy rules to support domain and subdomain hosting.

3. Intrusion Detection System (IDS) with Suricata

Installed Suricata IDS on the VM to:

Monitor network traffic.

Detect port scanning (e.g., Nmap).

Detect suspicious activities such as DoS or packet floods.

Enhanced system security and visibility by logging and alerting on intrusion attempts.

4. Automated Backups with Crontab

Implemented automated backup scripts using Crontab to:

Back up website files.

Schedule regular database backups from Google Cloud SQL (MySQL).

Reduce manual workload and improve data reliability.

5. Google Cloud SQL (MySQL)

Set up Google Cloud SQL with MySQL as the backend database.

Connected the dynamic website and admin portal to Cloud SQL for:

Product management.

Secure and scalable data storage.

6. Domain & SSL Configuration

Registered a free domain from Freenom.

Configured custom domain and subdomain:

Domain → Public-facing website.

Subdomain → Admin portal.

Secured both with SSL/TLS certificates using Let's Encrypt, ensuring encrypted HTTPS connections.

7. Admin Portal (AdminJS)

Built an admin dashboard using AdminJS for managing products.

Key functions:

Add new products.

Delete products.

Accessible only through a secure subdomain.

🗂 System Architecture
flowchart LR
    A[User] --> B[Custom Domain (Freenom) + SSL]
    B --> C[Nginx Web Server on GCP VM]
    C --> D[Public Website]
    C --> I[Admin Portal - Subdomain (AdminJS)]
    D --> E[Google Cloud SQL (MySQL)]
    I --> E
    C --> F[Suricata IDS for Intrusion Detection]
    G[Crontab Automation] --> E
    G --> D

💻 Tech Stack
Component	Technology
Cloud Platform	Google Cloud Platform (GCP)
VM Service	Google Compute Engine
Web Server	Nginx
Database	Google Cloud SQL (MySQL)
Security & Monitoring	Suricata IDS, GCP Firewall Rules
Automation	Crontab
Domain & SSL	Freenom, Let's Encrypt
Admin Panel	AdminJS
🔑 Highlights

Fully cloud-native deployment on GCP.

Secure and scalable architecture with SSL, Suricata IDS, and automated backups.

Dynamic website connected to managed MySQL database (Cloud SQL).

Separation of concerns with public site and admin portal on different domains/subdomains.

Reduced operational workload via Crontab automation.

🚀 Future Improvements

Implement load balancing with Google Cloud Load Balancer.

Add monitoring and alerting using Google Cloud Monitoring.

Improve admin panel with role-based access control (RBAC).

📜 Summary

This project demonstrates deploying a secure, production-ready dynamic website with:

GCP VM hosting using Nginx.

Suricata IDS for intrusion detection.

Crontab automation for database and file backups.

Google Cloud SQL (MySQL) for data management.

Custom domain and subdomain management with SSL encryption.

AdminJS portal for managing products efficiently.


Demo:
https://www.youtube.com/playlist?list=PLFb35DC5uB-r2ZV7YCIdYs_uF-aEAkNRo
