# Cloud Post System

## Project Overview
**Cloud Post System** is a web-based post publishing platform hosted on AWS Cloud. It allows users to register, log in, create posts, and publish them publicly. The system is backed by a cloud-hosted database and served via a public web server, demonstrating a complete 3-tier web architecture.

This project was developed as part of a **Cloud Computing** course to simulate real-world cloud architecture, deployment automation, and web application hosting scenarios.

### Key Features
- **User Authentication**: Secure account creation and login functionality.
- **Post Management**: Users can create, publish, and manage text-based posts.
- **Cloud Persistence**: All data is securely stored in a cloud-hosted MariaDB database.
- **Public Access**: The application is accessible via a public web server hosted on AWS EC2.

---

## Cloud Architecture
The system is deployed on **Amazon Web Services (AWS)** using a robust and scalable architecture:
- **Compute**: AWS EC2 (Elastic Compute Cloud) instance hosting the web server.
- **Web Server**: Apache HTTP Server + PHP for serving dynamic content.
- **Database**: MariaDB (MySQL compatible) for relational data storage.
- **Network Security**: AWS Security Groups configured for strict network access control.
- **Automation**: EC2 User Data scripts for automated provisioning and configuration.

### Architecture Diagram
![System Architecture Diagram](architecture/system-architecture-diagram.png)

---

## Deployment Automation
The project utilizes Infrastructure as Code (IaC) principles via an **EC2 User Data bootstrap script**. This script automates the entire server setup process, ensuring consistency and reducing manual configuration.

**Script Location:** `deployment/ec2-userdata.sh`

### Automated Steps:
1.  **System Update**: Updates the Amazon Linux package repositories.
2.  **Dependency Installation**: Installs Apache, PHP, Git, and MariaDB.
3.  **Application Deployment**: Clones the source code from the GitHub repository.
4.  **Database Configuration**: Initializes the database and imports the schema/tables.
5.  **Permissions**: Sets appropriate file ownership and permissions for the web server.
6.  **Service Management**: Starts and enables Apache and MariaDB services to run on boot.

---

## Project Structure
The repository is organized as follows:
```
Cloud-Post-System/
├── documentation/     # Contains the full project report
├── architecture/      # Contains system design diagrams
├── deployment/        # Contains EC2 automated setup script
└── README.md          # Project overview and instructions
```

---

## Technologies Used
- **Cloud Provider**: AWS EC2
- **Web Server**: Apache HTTP Server
- **Server-Side Language**: PHP
- **Database**: MariaDB
- **OS**: Linux (Amazon Linux)
- **Version Control**: Git

---

## Skills Demonstrated
This project highlights competency in the following areas:
- **Cloud Infrastructure Deployment**: Provisioning and managing EC2 instances.
- **Web Application Hosting**: Configuring LAMP stack (Linux, Apache, MySQL/MariaDB, PHP).
- **Database Configuration**: Setting up and securing a relational database in the cloud.
- **Linux Server Administration**: Managing packages, services, and file permissions via CLI.
- **Automated Provisioning**: Writing shell scripts for automated server setup (User Data).
- **Basic DevOps Practices**: Integrating version control and automation into the deployment workflow.

---

## Academic Context
This project was completed as part of a university **Cloud Computing** course. It was developed in a team environment to simulate real-world cloud deployment scenarios, emphasizing collaboration, version control, and system integration.

---

> **Note**: The live AWS environment used for this project may no longer be active. However, this documentation, along with the architecture diagrams and deployment scripts, fully describes how the system was designed, built, and deployed.
