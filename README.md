# Linux Server Administration Lab

A hands-on Linux Server Administration project designed to practice essential Linux system administration tasks commonly performed by Linux Administrators, System Engineers, and DevOps Engineers.

## 📌 Project Overview

This project simulates the setup and administration of a Linux server for a fictional company. It focuses on managing users, groups, file permissions, ownership, and directory structures while following Linux administration best practices.

---

## 🎯 Objectives

- Practice Linux user management
- Manage Linux groups
- Configure file ownership and permissions
- Organize directories
- Understand Linux security basics
- Gain practical Linux administration experience

---

## 🛠️ Environment

- Operating System: Ubuntu Server
- Virtualization: VirtualBox / VMware
- Terminal: Bash
- User: Root & Standard Users

---

# Project Scenario

A fictional company named **TechCorp** requires a Linux server to manage employees from different departments.

Departments:

- HR
- Developers
- DevOps

Each department should have:

- Its own Linux group
- Dedicated users
- Separate directory
- Proper permissions
- Controlled access

---

# Tasks Performed

## 1. User Management

- Created multiple users
- Assigned passwords
- Verified user accounts
- Locked and unlocked user accounts
- Changed user passwords

---

## 2. Group Management

Created Linux groups:

- hr
- developers
- devops

Added users to their respective groups.

---

## 3. Directory Structure

Created company directories.

```
/company
│
├── hr
├── developers
├── devops
└── shared
```

---

## 4. File Permissions

Configured directory permissions so that:

- HR users can access HR directory
- Developers can access Developers directory
- DevOps users can access DevOps directory
- Shared directory is accessible by all departments

---

## 5. Ownership Management

Configured:

- User ownership
- Group ownership

using Linux ownership commands.

---

## 6. Permission Verification

Verified that:

- Unauthorized users cannot access restricted directories
- Authorized users have proper read/write access

---

# Linux Commands Practiced

## User Management

```
useradd
passwd
usermod
userdel
id
whoami
```

## Group Management

```
groupadd
groupdel
groups
gpasswd
```

## Permissions

```
chmod
chown
chgrp
ls -l
```

## Directory Management

```
mkdir
cp
mv
rm
touch
tree
pwd
```

## System Information

```
hostname
hostnamectl
who
w
uptime
```

---

# Skills Learned

- Linux User Administration
- Linux Group Administration
- Linux File Permissions
- Ownership Management
- Linux Directory Structure
- Access Control
- Linux Security Fundamentals
- System Administration Basics

---

# Screenshots

Add screenshots of:

- Creating users
- Creating groups
- Directory structure
- File permissions
- Ownership changes
- User verification
- Access denied examples
- Successful login examples

Example:

```
screenshots/
├── users.png
├── groups.png
├── permissions.png
├── ownership.png
└── directories.png
```

---

# Learning Outcome

Through this project I learned how Linux administrators manage users, groups, directories, permissions, and ownership to securely organize a Linux server.

This project strengthened my understanding of Linux fundamentals and prepared me for future Cloud and DevOps projects.

---

# Future Improvements

- Bash Automation
- Cron Jobs
- SSH Configuration
- Nginx Deployment
- Log Management
- System Monitoring
- Firewall Configuration
- Docker Deployment

---

# Repository Structure

```
linux-server-administration-lab/

├── README.md
├── screenshots/
│   ├── users.png
│   ├── groups.png
│   ├── permissions.png
│   ├── ownership.png
│   └── directories.png
└── commands.md
```

---

# Author

**Abhishek Pundir**

Cloud & DevOps Learner

Building hands-on Linux, Cloud, and DevOps projects while continuously improving practical skills.

---

## ⭐ If you found this project helpful, consider giving it a star!
