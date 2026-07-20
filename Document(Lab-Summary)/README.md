# 🐧 Linux Administration Lab

> A comprehensive hands-on Linux Administration project built on **Ubuntu Server**, covering essential system administration tasks commonly performed by Linux System Administrators, Cloud Engineers, and DevOps Engineers.

---

# 📋 Lab Summary

| 🖥️ Component | 📌 Details |
|-------------|-----------|
| **Operating System** | Ubuntu 20.04 LTS |
| **Kernel Version** | Linux 5.15.0-139-generic |
| **Hostname** | webserver01 |
| **IP Address** | 192.168.16.128 |
| **Web Server** | Nginx |
| **Firewall** | UFW |
| **Automation** | Cron Jobs |
| **Backup Tool** | tar + gzip |

---

# 🖥️ 1. System Information

| Property | Value |
|----------|-------|
| Operating System | Ubuntu 20.04 LTS |
| Kernel | Linux 5.15.0-139-generic |
| Hostname | webserver01 |
| IP Address | 192.168.16.128 |

---

# 👥 2. Users & Groups

### Users Created

- 👤 alice
- 👤 bob
- 👤 john

### Groups Created

- 👥 developers
- 👥 sysadmins

### Administrative User

- 🔑 john (Added to the **sudo** group)

---

# 🔐 3. Directory Permissions

| Item | Configuration |
|------|---------------|
| Shared Directory | `/home/abhi/company/projects/website` |
| Owner | alice |
| Group | developers |
| Permissions | `770 (rwxrwx---)` |
| Special Permission | SGID Enabled |

---

# 🌐 4. Web Server Configuration

| Component | Status |
|-----------|--------|
| Web Server | Nginx |
| Service | ✅ Active (Running) |
| HTTP Port | TCP 80 |
| Firewall | UFW Enabled |
| Allowed Rule | HTTP (Port 80) |

---

# 💾 5. Backup & Restore

| Item | Details |
|------|---------|
| Backup Directory | `/home/abhi/company/backups/` |
| Backup File | `website-backup.tar.gz` |
| Compression | gzip |
| Restore Test | ✅ Successfully Verified |

---

# 🛠️ 6. Troubleshooting

## Problems Encountered

- Package manager (APT) lock
- Nginx installation issues
- Missing OpenSSH profile in UFW
- User home directory creation
- File permission errors
- GitHub README image path issues
- Cron editor selection
- Network connectivity verification

---

## Diagnostic Tools Used

```bash
systemctl
journalctl
ps
ss
ip addr
ip route
df -h
du -h
ls -l
ping
```

---

## Solutions Implemented

- ✔ Cleared package manager lock after verifying no running process.
- ✔ Installed and configured Nginx successfully.
- ✔ Added firewall rules manually using UFW.
- ✔ Created and verified user home directories.
- ✔ Corrected ownership and permissions using `chown` and `chmod`.
- ✔ Fixed GitHub image paths using relative links.
- ✔ Configured automated Cron Jobs.
- ✔ Verified network connectivity using `ping` and `ss`.

---

# 📊 Final Validation

| Check | Status |
|--------|--------|
| Website Accessible | ✅ YES |
| Nginx Running | ✅ YES |
| Nginx Enabled at Boot | ✅ YES |
| Firewall Configured | ✅ YES |
| Backup Created | ✅ YES |
| Restore Tested | ✅ YES |
| Cron Jobs Configured | ✅ YES |
| Network Connectivity Verified | ✅ YES |

---

# 🚀 Skills Demonstrated

- 🐧 Linux System Administration
- 👥 User & Group Management
- 🔐 Linux File Permissions
- 📦 Package Management
- ⚙️ Service Management
- 🔥 Firewall Configuration (UFW)
- 📈 Process Monitoring
- 💽 Disk & Storage Monitoring
- 📜 Log Monitoring
- 🌐 Networking & Connectivity
- 🗜️ Archiving & Backup
- 🔄 Output Redirection
- ⏰ Cron Job Automation
- 🔍 Linux Troubleshooting

---

# 📂 Modules Completed

| Module | Status |
|---------|--------|
| 01 - System Information | ✅ |
| 02 - User & Group Administration | ✅ |
| 03 - Directory & Permission Management | ✅ |
| 04 - Package Management | ✅ |
| 05 - Service Management | ✅ |
| 06 - Firewall Configuration | ✅ |
| 07 - Process Monitoring | ✅ |
| 08 - System Monitoring | ✅ |
| 09 - Network Monitoring | ✅ |
| 10 - Disk & Storage Monitoring | ✅ |
| 11 - Archiving & Backup | ✅ |
| 12 - Log Monitoring | ✅ |
| 13 - Networking & Connectivity | ✅ |
| 14 - Redirection & Cron Jobs | ✅ |

---

# 🎉 Project Completion

This project demonstrates practical Linux Administration skills through hands-on configuration, monitoring, troubleshooting, automation, networking, and backup tasks.

It reflects real-world system administration practices and serves as a portfolio project showcasing proficiency in Linux environments used by **System Administrators**, **Cloud Engineers**, and **DevOps Engineers**.

> **Project Status:** ✅ **Completed Successfully**
