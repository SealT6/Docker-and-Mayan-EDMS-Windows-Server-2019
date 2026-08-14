# 🐳 Docker + Mayan EDMS | Windows Server 2019 Lab Environment

## 📌 Project Overview

This project documents the deployment of **Mayan EDMS (Electronic Document Management System)** using **Docker Compose** within a virtualized lab environment associated with my Windows Server 2019 infrastructure work.

The project demonstrates practical experience with:

* Virtualized lab environments
* Linux administration
* Docker installation and container management
* Docker Compose
* Application deployment
* Web-based application validation
* Document management infrastructure
* Security-relevant document integrity features

> **Environment Note:** The screenshots in this project show the Docker/Mayan EDMS workload running inside an Ubuntu virtual machine managed through the lab virtualization environment. The project is part of my broader Windows Server 2019 infrastructure portfolio.

---

## 🎯 Objectives

* Prepare a virtualized environment for application deployment
* Install Docker
* Obtain the Mayan EDMS Docker Compose configuration
* Deploy Mayan EDMS and its supporting containers
* Validate the deployment through a web browser
* Log in to the Mayan EDMS administrative interface
* Evaluate security-relevant document management capabilities

---

## 🧰 Technologies & Tools

| Technology              | Purpose                                          |
| ----------------------- | ------------------------------------------------ |
| **Windows Server 2019** | Infrastructure/lab environment                   |
| **Ubuntu Linux**        | Docker host shown in deployment screenshots      |
| **Docker**              | Container platform                               |
| **Docker Compose**      | Multi-container application deployment           |
| **Mayan EDMS**          | Electronic Document Management System            |
| **Virtualization**      | Lab environment and VM management                |
| **Firefox**             | Web-based application validation                 |
| **cURL / wget**         | Downloading installation and configuration files |

---

## 🏗️ Environment

The deployment was performed in a virtualized lab environment.

### High-Level Architecture

```text
Windows Server 2019 Lab Environment
            │
            ▼
      Virtualized Linux VM
            │
            ▼
         Docker
            │
            ▼
     Docker Compose
            │
            ▼
        Mayan EDMS
            │
            ▼
     Web Browser / HTTP
```

---

## 🔧 Deployment Process

### 1. Prepare the Environment

The first stage was preparing the Linux virtual machine for the Mayan EDMS deployment.

<img width="640" height="420" alt="01-environment" src="https://github.com/user-attachments/assets/4ab3d272-3165-4738-a884-93b453f872ba" />


---

### 2. Install Docker

Docker was installed using the documented installation command:

```bash
wget -qO- https://get.docker.com/ | sh
```

The installation was verified from the Linux terminal.
<img width="720" height="455" alt="03-docker-compose-launch" src="https://github.com/user-attachments/assets/9d8e9b7a-bac3-4685-a316-cca5994f0b55" />



---

### 3. Obtain the Mayan EDMS Docker Compose Files

The Mayan EDMS Docker Compose configuration and environment file were downloaded using `curl`.

If `curl` is not installed, it can be installed with:

```bash
sudo apt install curl
```

The project documentation used:

```bash
curl https://gitlab.com/mayan-edms/mayan-edms/-/raw/master/docker/docker-compose.yml -O
```

```bash
curl https://gitlab.com/mayan-edms/mayan-edms/-/raw/master/docker/.env -O
```

These files provide the configuration required to deploy the Mayan EDMS container environment.
<img width="715" height="465" alt="02-docker-install" src="https://github.com/user-attachments/assets/95be7457-2068-4506-bf31-679f589f2f20" />

---

### 4. Deploy Mayan EDMS with Docker Compose

The Mayan EDMS environment was launched using Docker Compose:

```bash
sudo docker compose up --detach
```

The terminal output was monitored to verify that the required images were pulled and the containers were created and started.

<img width="720" height="455" alt="03-docker-compose-launch" src="https://github.com/user-attachments/assets/899212a8-5e44-499d-88d4-eb1e91437c66" />


---

## ✅ Deployment Validation

After the containers were started, the Mayan EDMS web interface was accessed through the local machine:

```text
http://localhost/
```

The successful web interface confirmed that the application was running and accessible from the host environment.

<img width="650" height="405" alt="04-mayan-edms-web-ui" src="https://github.com/user-attachments/assets/aca4a1c4-26a9-4141-ae6e-9957dc30018a" />


---

## 🔐 Administrative Access

The deployment generated administrative credentials that were used to access the Mayan EDMS interface.

<img width="640" height="370" alt="05-mayan-edms-dashboard" src="https://github.com/user-attachments/assets/2c71b403-9ed1-46b8-beff-e7fba98652db" />


The dashboard provided access to core document management functionality and confirmed successful application deployment.

---

## 🔒 Security-Relevant Features

Although this project primarily focused on deployment and infrastructure configuration, Mayan EDMS provides several capabilities that are relevant to secure document management.

### Document Versioning

Mayan EDMS assigns versions to documents as they are uploaded or modified. Version history can help maintain an auditable record of document changes and reduce the risk of losing previous versions.

### Digital Signatures

Mayan EDMS supports digital signatures for document authenticity and integrity. A digital signature can provide an indication that a signed document has been altered after signing.

### Workflow Automation

The platform includes workflow functionality that can help organizations standardize document-processing activities.

### Metadata Extraction & OCR

Mayan EDMS supports automatic metadata extraction and OCR processing. OCR converts text contained in document images into machine-readable text, which can improve document searchability and reduce manual data entry.

---

## 🧪 Validation Performed

| Test                         | Result                       |
| ---------------------------- | ---------------------------- |
| Docker installation          | ✅ Successful                 |
| Docker Compose configuration | ✅ Downloaded                 |
| Docker Compose deployment    | ✅ Containers created/started |
| Mayan EDMS web interface     | ✅ Accessible                 |
| Administrative login         | ✅ Successful                 |
| Mayan EDMS dashboard         | ✅ Verified                   |

---

## 🛡️ Security Considerations & Future Improvements

The deployment demonstrates application installation and validation, but a production deployment would require additional security controls.

Potential next steps include:

* [ ] Replace HTTP with HTTPS/TLS
* [ ] Implement a reverse proxy
* [ ] Restrict exposed network ports
* [ ] Apply least-privilege access controls
* [ ] Secure and rotate application credentials
* [ ] Protect Docker configuration and environment files
* [ ] Implement regular backups
* [ ] Establish a patching/update process
* [ ] Monitor container and application logs
* [ ] Perform a vulnerability assessment against the deployment
* [ ] Document recovery procedures

These improvements would extend the project from a deployment lab into a more complete **secure application infrastructure project**.

---

## 📚 Skills Demonstrated

### Infrastructure

* Virtual machine administration
* Linux administration
* Windows Server infrastructure
* Application deployment

### Containerization

* Docker installation
* Docker Compose
* Container lifecycle management
* Multi-container application deployment

### Cybersecurity

* Secure document management concepts
* Document integrity
* Digital signatures
* Version control
* Security hardening considerations

### Troubleshooting

* Package/dependency troubleshooting
* Command-line administration
* Application validation
* Container deployment verification

---

## 💡 What I Learned

This project provided hands-on experience deploying a multi-container application rather than simply installing a standalone application. I learned how Docker and Docker Compose can simplify application deployment and how a web-based application can be validated after its supporting containers are initialized.

The project also demonstrated how document-management platforms can incorporate security-relevant capabilities such as document versioning and digital signatures. These features are particularly important when managing documents that require integrity, traceability, and controlled workflows.

---

## 🚀 Future Expansion

I plan to build on this project by applying additional security controls and incorporating it into a broader cybersecurity lab.

Potential future work includes:

1. Place Mayan EDMS behind a TLS-enabled reverse proxy.
2. Implement network segmentation and firewall restrictions.
3. Perform a Nessus vulnerability assessment.
4. Monitor Docker and application logs with a SIEM such as Splunk.
5. Document identified vulnerabilities and remediation steps.
6. Create backup and recovery procedures.
7. Perform post-hardening validation.

---

## 📁 Project Evidence

The screenshots included in this repository document the deployment from initial environment preparation through successful Mayan EDMS access.

**Project progression:**

`Virtual Lab → Docker Installation → Docker Compose Deployment → Web Validation → Mayan EDMS Dashboard`

---

## 👤 Author

**Sean Redding**

Cybersecurity | Security Operations | Vulnerability Management | Security Engineering

[GitHub](https://github.com/SealT6) • [LinkedIn](https://www.linkedin.com/in/sean-redding-aa503a293/)
