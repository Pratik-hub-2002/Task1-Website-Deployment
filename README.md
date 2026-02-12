# Task1-Website-Deployment
Internship Task 1 - Website deployment on Linux server, managing file permissions, and creating ZIP backup using Apache on EC2.
## 1. Create a Directory and Upload Website Files

### Create Website Directory

sudo mkdir -p /var/www/html/Task1

### Upload Files from Local PC to Server

scp -i key.pem website_demo.zip
ec2-user@`<server-ip>`{=html}:/var/www/html/Task1

### Navigate to Directory

cd /var/www/html/Task1

### Extract Website Files

sudo unzip website_demo.zip

------------------------------------------------------------------------

## 2. Change File Ownership and Permissions

### Change Ownership to Apache User

sudo chown -R apache:apache /var/www/html/Task1

### Set File Permissions

sudo chmod -R 755 /var/www/html/Task1

Explanation: - chmod → Modifies file and directory permissions - chown →
Changes file owner and group - 755 → Owner has full access, group and
others have read & execute access

------------------------------------------------------------------------

## 3. Create ZIP Backup and Extract in Another Location

### Create Backup Directory

sudo mkdir -p /backup

### Create ZIP Backup

sudo zip -r Task1-backup.zip Task1

### Move Backup to Backup Directory

sudo mv Task1-backup.zip /backup/

### Extract Backup

cd /backup sudo unzip Task1-backup.zip -d extracted_Task1

------------------------------------------------------------------------

## 4. Purpose of Commands

  Command   Purpose
  --------- -----------------------------------------------
  chmod     Modifies file and directory permissions
  chown     Changes file owner and group
  zip       Compresses files/directories into ZIP archive
  unzip     Extracts files from ZIP archive

------------------------------------------------------------------------

## 5. Output of Permission Settings (ls -l)

Command Used: ls -l /var/www/html/Task1

[ec2-user@ip-172-31-2-154 backup]$ 1s -1 /var/www/html/Task1
total 28

-rwxr-xr-x. 1 apache apache 40  Feb 8  05:04 bootstrap.min.css

-rw-r--r--. 1 root root     252 Feb 12 08:36 db.php

-rwxr-xr-x. 1 apache apache 525 Feb 12 08:39 index.html

-rw-r--r--. 1 root root     636 Feb 12 08:36 save_contact.php

-rwxr-xr-x. 1 apache apache 43 Feb 8 05:04 script.js

-rwxr-xr-x. 1 apache apache 380 Feb 12 08:43 style.css

-rwxr-xr-x. 1 apache apache 1441 Feb 12 07:39 website_demo.zip

Permission Breakdown: - r → Read - w → Write - x → Execute - First 3
characters → Owner permissions - Next 3 → Group permissions - Last 3 →
Others permissions

------------------------------------------------------------------------

## Result

-   Website successfully deployed under /var/www/html/Task1
-   Ownership and permissions configured correctly
-   ZIP backup created and restored successfully
-   Permission verification completed using ls -l

------------------------------------------------------------------------

## Internship Details

Intern Name: Pratik Raut Task: Website Deployment & File Management
Environment: Amazon Linux (EC2 Instance) Web Server: Apache (httpd)
