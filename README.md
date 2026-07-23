# 🚀 Task 1 - Website Deployment on Linux Server

A hands-on internship project demonstrating **website deployment on an Amazon EC2 (Linux) instance** using the **Apache HTTP Server (httpd)**. This project covers Linux file management, secure file transfer, permission handling, and backup creation using ZIP utilities.

![AWS](https://img.shields.io/badge/AWS-EC2-FF9900?logo=amazon-aws)
![Linux](https://img.shields.io/badge/Linux-Amazon%20Linux-FCC624?logo=linux)
![Apache](https://img.shields.io/badge/Apache-httpd-D22128?logo=apache)
![Bash](https://img.shields.io/badge/Shell-Bash-4EAA25?logo=gnubash)
![GitHub](https://img.shields.io/badge/GitHub-Portfolio-black?logo=github)

---

# 📖 About

This repository contains **Internship Task 1**, where a static website was successfully deployed on an **Amazon Linux EC2 instance** using the **Apache HTTP Server**.

The project demonstrates essential Linux administration skills, including creating directories, uploading files securely using SCP, configuring file ownership and permissions, creating ZIP backups, and restoring website files.

This task helped strengthen my understanding of **Linux system administration, web server configuration, file management, and basic DevOps practices**.

---

# 🎯 Objectives

- Deploy a website on an Amazon EC2 Linux server
- Configure Apache Web Server
- Upload website files using SCP
- Manage Linux file ownership
- Configure file permissions
- Create ZIP backups
- Restore website from backup
- Verify permissions using Linux commands
- Gain practical Linux administration experience

---

# ✨ Features

## 🌐 Website Deployment

- Deploy Website on Apache
- Serve Static Website
- Linux Directory Management
- Website File Extraction

---

## 📂 File Management

- Create Website Directory
- Upload Files via SCP
- Extract ZIP Archive
- Organize Website Files

---

## 🔐 Permission Management

- Change File Ownership
- Configure Directory Permissions
- Secure File Access
- Verify Permission Settings

---

## 💾 Backup & Restore

- Create ZIP Backup
- Store Backup Files
- Restore Website
- Backup Verification

---

## 🖥 Linux Administration

- Apache Web Server
- Linux File System
- Command Line Operations
- File Permission Verification

---

# 🛠 Technologies Used

## Cloud Platform

- Amazon Web Services (AWS)
- Amazon EC2

---

## Operating System

- Amazon Linux

---

## Web Server

- Apache HTTP Server (httpd)

---

## Linux Utilities

- SCP
- ZIP
- Unzip
- chmod
- chown
- ls

---

# 📂 Project Structure

```text
Task1-Website-Deployment/
│
├── website_demo.zip
├── index.html
├── style.css
├── script.js
├── bootstrap.min.css
├── db.php
├── save_contact.php
└── README.md
```

---

# 🚀 Deployment Steps

## 1️⃣ Create Website Directory

```bash
sudo mkdir -p /var/www/html/Task1
```

---

## 2️⃣ Upload Website Files

```bash
scp -i key.pem website_demo.zip ec2-user@<server-ip>:/var/www/html/Task1
```

Navigate into the directory.

```bash
cd /var/www/html/Task1
```

Extract website files.

```bash
sudo unzip website_demo.zip
```

---

## 3️⃣ Configure Ownership & Permissions

Change ownership.

```bash
sudo chown -R apache:apache /var/www/html/Task1
```

Set permissions.

```bash
sudo chmod -R 755 /var/www/html/Task1
```

---

## 4️⃣ Create Website Backup

Create backup directory.

```bash
sudo mkdir -p /backup
```

Create ZIP backup.

```bash
sudo zip -r Task1-backup.zip Task1
```

Move backup.

```bash
sudo mv Task1-backup.zip /backup/
```

Restore backup.

```bash
cd /backup

sudo unzip Task1-backup.zip -d extracted_Task1
```

---

# 📋 Linux Commands Used

| Command | Purpose |
|----------|---------|
| `mkdir` | Create directory |
| `scp` | Securely copy files |
| `cd` | Change directory |
| `zip` | Compress files into ZIP archive |
| `unzip` | Extract ZIP archive |
| `chmod` | Modify file permissions |
| `chown` | Change ownership |
| `ls -l` | View file permissions |

---

# 🔒 Permission Configuration

## Verify Permissions

```bash
ls -l /var/www/html/Task1
```

Example Output

```text
total 28

-rwxr-xr-x 1 apache apache   40 bootstrap.min.css
-rw-r--r-- 1 root   root    252 db.php
-rwxr-xr-x 1 apache apache  525 index.html
-rw-r--r-- 1 root   root    636 save_contact.php
-rwxr-xr-x 1 apache apache   43 script.js
-rwxr-xr-x 1 apache apache  380 style.css
-rwxr-xr-x 1 apache apache 1441 website_demo.zip
```

### Permission Breakdown

| Symbol | Meaning |
|---------|---------|
| `r` | Read |
| `w` | Write |
| `x` | Execute |
| First 3 Characters | Owner Permissions |
| Middle 3 Characters | Group Permissions |
| Last 3 Characters | Others Permissions |

---

# 📚 Project Workflow

```text
Create Directory
        │
        ▼
Upload Website Files
        │
        ▼
Extract ZIP
        │
        ▼
Configure Ownership
        │
        ▼
Set Permissions
        │
        ▼
Deploy Website
        │
        ▼
Create ZIP Backup
        │
        ▼
Restore Backup
        │
        ▼
Verify Permissions
```

---

# 📈 Learning Outcomes

During this task, I gained practical experience with:

- Amazon EC2
- Amazon Linux
- Apache HTTP Server
- Linux File System
- Secure File Transfer (SCP)
- File Ownership Management
- Linux Permissions
- ZIP Backup & Restore
- Basic Server Administration
- Command Line Operations

---

# 🚀 Future Enhancements

- Deploy Dynamic PHP Website
- Configure Virtual Hosts
- SSL using Let's Encrypt
- Domain Name Configuration
- Automated Backup Scripts
- Cron Job Scheduling
- CI/CD Pipeline
- Nginx Deployment
- Docker Containerization
- Monitoring & Logging

---

# 📊 Repository Highlights

- ☁️ Amazon EC2 Deployment
- 🐧 Amazon Linux Administration
- 🌐 Apache Web Server
- 🔐 Linux File Permissions
- 📂 Secure File Transfer
- 💾 ZIP Backup & Restore
- 🖥 Command Line Operations
- 🚀 Internship Project
- 💼 Portfolio Ready

---

# ✅ Result

- Successfully deployed the website under **/var/www/html/Task1**
- Configured ownership and permissions
- Created ZIP backup
- Restored backup successfully
- Verified Linux permissions using **ls -l**

---

# 🤝 Contributions

This repository is part of my internship learning journey and portfolio.

Suggestions, improvements, and feedback are always welcome.

If you found this project useful, consider giving it a ⭐.

---

# 👨‍💻 Author

## Pratik Raut

**Java Developer | Cloud Computing Enthusiast | Building Real-World Projects**

### 📬 Connect with Me

- **GitHub:** https://github.com/Pratik-hub-2002
- **LinkedIn:** https://www.linkedin.com/in/pratik-raut-80b611245
- **Email:** praut3022@gmail.com

---

# 📜 License

This project is available for learning, educational, and portfolio purposes.

---

# ⭐ Support

If you found this project useful, don't forget to **Star ⭐ the repository**.

Happy Learning! 🚀
