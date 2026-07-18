# Linux System Administration Lab (Ubuntu Server)

> A hands-on Linux System Administration project demonstrating real-world server management, security, networking, and troubleshooting using **Ubuntu Server**.

![Ubuntu](https://img.shields.io/badge/Ubuntu-Server-E95420?logo=ubuntu)
![Linux](https://img.shields.io/badge/Linux-System%20Administration-blue?logo=linux)
![Nginx](https://img.shields.io/badge/Nginx-Web%20Server-green?logo=nginx)
![Bash](https://img.shields.io/badge/Bash-Shell-black?logo=gnu-bash)

---

# Project Overview

This project simulates the day-to-day responsibilities of a **Linux System Administrator**.

Starting from a fresh Ubuntu Server installation, the server was configured, secured, and managed as an internal web server for a fictional company called **TechNova Pvt. Ltd.**

The project demonstrates practical Linux administration skills including user management, permissions, networking, web server deployment, backups, and troubleshooting.

---

# Architecture

```text
                   Ubuntu Server VM
                          │
        ┌─────────────────┼─────────────────┐
        │                 │                 │
   User Management     Nginx Server      Networking
        │                 │                 │
 Permissions        Website Hosting     UFW Firewall
        │                 │                 │
 Backup & Restore   systemd Services   Troubleshooting
```

---

# Lab Environment

| Component        | Details                 |
| ---------------- | ----------------------- |
| Operating System | Ubuntu Server 24.04 LTS |
| Virtualization   | VMware Workstation      |
| Shell            | Bash                    |
| Package Manager  | APT                     |
| Web Server       | Nginx                   |
| Firewall         | UFW                     |
| Service Manager  | systemd                 |

---

# Project Objectives

* Configure Ubuntu Server
* Manage users and groups
* Configure secure permissions
* Deploy an Nginx web server
* Configure networking
* Manage Linux services
* Configure the firewall
* Monitor processes
* Monitor storage
* Create backups
* Restore backups
* Troubleshoot common Linux issues

---

# Skills Demonstrated

* Linux Administration
* Ubuntu Server Management
* User & Group Management
* File Permissions
* SGID
* Package Management (APT)
* Service Management (systemd)
* Nginx Administration
* UFW Firewall
* Networking
* Process Management
* Storage Monitoring
* Backup & Restore
* Log Analysis
* Troubleshooting

---

# Repository Structure

```text
linux-administration-lab/
│
├── README.md                      # Main project overview
├── LICENSE
│
├── 01-system-information/
│   ├── README.md
│   └── screenshots/
│       ├── hostname.png
│       ├── os-release.png
│       ├── lscpu.png
│       ├── free-h.png
│       ├── df-h.png
│       └── ip-addr.png
│
├── 02-hostname-configuration/
│   ├── README.md
│   └── screenshots/
│       └── hostname-change.png
│
├── 03-user-group-management/
│   ├── README.md
│   └── screenshots/
│       ├── groupadd.png
│       ├── useradd.png
│       ├── passwd.png
│       ├── id.png
│       └── groups.png
│
├── 04-directory-management/
│   ├── README.md
│   └── screenshots/
│
├── 05-file-permissions/
│   ├── README.md
│   └── screenshots/
│
├── 06-shared-directory-sgid/
│   ├── README.md
│   └── screenshots/
│
├── 07-file-management/
│   ├── README.md
│   └── screenshots/
│
├── 08-package-management/
│   ├── README.md
│   └── screenshots/
│
├── 09-service-management/
│   ├── README.md
│   └── screenshots/
│
├── 10-nginx-web-server/
│   ├── README.md
│   └── screenshots/
│
├── 11-firewall-ufw/
│   ├── README.md
│   └── screenshots/
│
├── 12-process-management/
│   ├── README.md
│   └── screenshots/
│
├── 13-storage-management/
│   ├── README.md
│   └── screenshots/
│
├── 14-backup-and-restore/
│   ├── README.md
│   └── screenshots/
│
├── 15-networking/
│   ├── README.md
│   └── screenshots/
│
├── 16-log-analysis/
│   ├── README.md
│   └── screenshots/
│
└── 17-troubleshooting/
    ├── README.md
    └── screenshots/
```

---

# Task 1 — System Information

## Objective

Collect important information about the Linux server before configuration.

## Commands Used

```bash
hostnamectl
hostname
whoami
cat /etc/os-release
uname -r
lscpu
free -h
df -h
ip addr
date
```

## Information Collected

* Current Hostname
* Logged-in User
* Ubuntu Version
* Kernel Version
* CPU Information
* Memory Information
* Disk Usage
* IP Address
* Current Date & Time

## Screenshots

| Screenshot     | File                                          |
| -------------- | --------------------------------------------- |
| Hostname       | screenshots/system-information/hostname.png   |
| Ubuntu Version | screenshots/system-information/os-release.png |
| CPU            | screenshots/system-information/lscpu.png      |
| RAM            | screenshots/system-information/free-h.png     |
| Disk           | screenshots/system-information/df-h.png       |
| IP Address     | screenshots/system-information/ip-addr.png    |

---

# Task 2 — Hostname Configuration

## Objective

Change the server hostname.

## Commands

```bash
sudo hostnamectl set-hostname webserver01
hostnamectl
```

## Result

Hostname successfully changed to:

```text
webserver01
```

## Screenshot

```
screenshots/hostname/hostname.png
```

---

# Task 3 — User & Group Management

## Objective

Create users and groups for the organization.

### Groups

* developers
* sysadmins

### Users

| User  | Role                 |
| ----- | -------------------- |
| alice | Developer            |
| bob   | Developer            |
| john  | System Administrator |

## Commands

```bash
sudo groupadd developers
sudo groupadd sysadmins

sudo useradd -m -G developers alice
sudo useradd -m -G developers bob
sudo useradd -m -G sysadmins john

sudo passwd alice
sudo passwd bob
sudo passwd john
```

### Administrative Access

```bash
sudo usermod -aG sudo john
```

### Verification

```bash
id john
groups john
```

## Screenshots

* User Creation
* Group Creation
* User Information
* Sudo Verification

---

# Task 4 — Directory Structure

## Objective

Create the company directory structure.

```text
/company
├── projects
│   └── website
├── backups
└── logs
```

## Commands

```bash
sudo mkdir -p /company/projects/website
sudo mkdir -p /company/backups
sudo mkdir -p /company/logs
```

## Screenshot

Directory Structure

---

# Task 5 — Ownership & Permissions

## Objective

Configure secure ownership and permissions.

## Commands

```bash
sudo chown alice:developers /company/projects/website

sudo chmod 2770 /company/projects/website
```

## Verification

```bash
ls -ld /company/projects/website
```

Expected permissions:

```text
drwxrws---
```

## Screenshot

Permissions

---

# Task 6 — Shared Directory (SGID)

## Objective

Allow developers to collaborate using the same project directory.

## Testing

Create files as:

* alice
* bob

Verify:

```bash
ls -l /company/projects/website
```

## Screenshot

Shared Directory

---

# Task 7 — File Management

Completed operations:

* Create files
* Copy files
* Move files
* Rename files
* Delete files
* Search using find
* Search using grep

## Screenshot

File Management

---

# Task 8 — Package Management

## Commands

```bash
sudo apt update

sudo apt install nginx -y

dpkg -l nginx
```

## Screenshot

Package Installation

---

# Task 9 — Service Management

## Commands

```bash
sudo systemctl start nginx
sudo systemctl stop nginx
sudo systemctl restart nginx
sudo systemctl reload nginx
sudo systemctl enable nginx

systemctl status nginx
```

## Verification

```bash
systemctl is-enabled nginx

systemctl is-active nginx
```

## Screenshot

Nginx Service

---

# Task 10 — Web Server Configuration

Configured a custom Nginx web page.

## Testing

```bash
curl http://localhost
```

Verified from another machine using the server IP.

## Screenshot

Website Running

---

# Task 11 — Firewall Configuration (UFW)

## Commands

```bash
sudo ufw status

sudo ufw allow 80/tcp

sudo ufw enable

sudo ufw reload
```

## Verification

```bash
sudo ufw status
```

## Screenshot

Firewall Rules

---

# Task 12 — Process Management

Commands practiced:

```bash
ps aux

top

pgrep nginx

kill
```

Created and terminated background processes.

## Screenshot

Processes

---

# Task 13 — Storage Management

Commands

```bash
df -h

du -sh /company

du -h
```

## Screenshot

Storage Usage

---

# Task 14 — Backup & Restore

Created compressed backups using tar.

```bash
tar -czvf website-backup.tar.gz /company/projects/website
```

Restore

```bash
tar -xzvf website-backup.tar.gz
```

Verified successful restoration.

## Screenshot

Backup & Restore

---

# Task 15 — Networking

Commands

```bash
ip addr

ip route

ss -tulnp

ping

curl
```

Verified:

* IP Address
* Default Gateway
* DNS
* Listening Ports

## Screenshot

Networking

---

# Task 16 — Log Analysis

Commands

```bash
journalctl

journalctl -u nginx

sudo nginx -t
```

## Screenshot

Logs

---

# Task 17 — Troubleshooting

Simulated and resolved:

* Nginx service failure
* Permission denied
* Firewall blocking HTTP
* Invalid Nginx configuration
* DNS issues
* Disk space investigation

## Screenshot

Troubleshooting

---

# Frequently Used Commands

```text
hostnamectl
whoami
id
groupadd
useradd
usermod
passwd
mkdir
touch
cp
mv
rm
find
grep
chmod
chown
ls
cat
tar
apt
dpkg
systemctl
ufw
ps
top
kill
df
du
journalctl
ip
ss
curl
```

---

# Key Learnings

* Configured Ubuntu Server from scratch.
* Managed Linux users, groups, and permissions.
* Implemented SGID for collaborative directories.
* Installed and configured an Nginx web server.
* Managed services using systemd.
* Configured UFW firewall rules.
* Monitored storage, processes, and networking.
* Created and restored backups.
* Diagnosed and resolved common Linux administration issues.

---

# Future Improvements

* Bash automation scripts
* Cron jobs
* SSH hardening
* Log rotation
* Docker deployment
* Ansible automation
* Monitoring with Prometheus & Grafana

---

# Author

**Abhishek Pundir**

Aspiring Cloud & DevOps Engineer

* GitHub: https://github.com/Abhishek-max211
* LinkedIn: https://www.linkedin.com/in/abhishek-pundir-334473314

---
