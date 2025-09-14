# 🌐 Secure Dynamic Website Deployment on Google Cloud Platform

![Deployment Architecture](https://github.com/user-attachments/assets/4a46f005-35e7-4186-8f41-5da8e89472a4)

---

## 📖 Overview
This project demonstrates how to **deploy, secure, and automate** a dynamic web application using **Google Cloud Platform (GCP)** services.  
It covers **VM provisioning**, **web hosting with Nginx**, **intrusion detection**, **automated backups**, **cloud database integration**, and **secure domain management with SSL**.

The system also includes a **dedicated admin portal** to manage products, with **separate domain and subdomain** for the public-facing website and admin panel.

---

## 🛠 Features

### **1. Google Cloud Platform Infrastructure**
- Provisioned and configured **Virtual Machines (VMs)** using **Google Compute Engine**.  
- Managed **VPC networking**, **firewall rules**, and **DNS configuration** to ensure secure connectivity.

---

### **2. Web Hosting with Nginx**
- Installed and configured **Nginx** to serve the dynamic website.  
- Configured **reverse proxy rules** to support hosting on both **domain** and **subdomain**.

---

### **3. Intrusion Detection System (IDS) with Suricata**
- Installed **Suricata IDS** on the VM to:
  - Monitor network traffic.  
  - Detect **port scanning** (e.g., Nmap).  
  - Identify suspicious activities such as **DoS attacks** or **packet floods**.  
- Improved **security visibility** with real-time logs and alerts.

---

### **4. Automated Backups with Crontab**
- Configured **Crontab scripts** to automatically:
  - Back up **website files**.  
  - Schedule **regular database backups** from **Google Cloud SQL (MySQL)**.  
- Reduced **manual workload** and improved **data reliability**.

---

### **5. Google Cloud SQL (MySQL)**
- Deployed **Google Cloud SQL (MySQL)** as the backend database.  
- Connected both the **public website** and **admin portal** to Cloud SQL for:
  - Product management.  
  - Scalable and secure data storage.

---

### **6. Domain & SSL Configuration**
- Registered a **free domain** in https://freedomain.one/. 
- Configured **domain** and **subdomain**:  
  - **Domain** → Public-facing website.  
  - **Subdomain** → Admin portal.  
- Secured both using **SSL/TLS certificates** from **Let's Encrypt** for **HTTPS** encryption.

---

### **7. Admin Portal (AdminJS)**
- Built an **AdminJS dashboard** for product management.  
- **Key features**:
  - Add new products.  
  - Delete products.  
- Accessible only via a **secure subdomain**.

---

## 🗂 System Architecture
```mermaid
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
```
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

Fully cloud-native deployment built entirely on GCP.

Enhanced security with Suricata IDS and SSL encryption.

Automated backups for data safety and reduced operational overhead.

Clear separation of services:

Public-facing website → Domain.

Admin portal → Subdomain.

Scalable and production-ready infrastructure.

🚀 Future Improvements

Implement Google Cloud Load Balancer for load balancing and redundancy.

Add Google Cloud Monitoring for real-time alerts and performance tracking.

Enhance AdminJS with role-based access control (RBAC) for improved security.

📜 Summary

This project demonstrates deploying a secure, production-ready dynamic website with:

GCP VM hosting using Nginx.

Suricata IDS for real-time intrusion detection.

Crontab automation for regular database and file backups.

Google Cloud SQL (MySQL) for backend data management.

Custom domain and subdomain with SSL encryption.

AdminJS portal for efficient product management.

🎥 Demo

![Image](https://github.com/user-attachments/assets/154d120d-4e75-4bc5-affb-ae5f78ca0fd4)

https://www.youtube.com/playlist?list=PLFb35DC5uB-r2ZV7YCIdYs_uF-aEAkNRo
