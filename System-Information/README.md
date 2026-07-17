# 🖥️ System Information

Collect and analyze essential information about an Ubuntu Server before performing any administration tasks.

---

## 🎯 Objective

This lab demonstrates how to gather important system information using standard Linux commands.

Topics covered:

- Hostname
- Current User
- Operating System
- Kernel Version
- CPU Information
- Memory Information
- Disk Usage
- Network Configuration
- Routing Table
- System Date & Time

---

## 📋 Lab Tasks

### 1. Check Hostname

**Command**

```bash
hostname
```

**Description**

Displays the current hostname of the system.

**Output**

> Replace this image with your own screenshot.

![Hostname](./screenshots/hostname.png)

---

### 2. Display Detailed Host Information

**Command**

```bash
hostnamectl
```

**Description**

Displays detailed information about the operating system, hostname, architecture, and kernel.

**Output**

![Hostnamectl](./screenshots/hostnamectl.png)

---

### 3. Display Current User

**Command**

```bash
whoami
```

**Description**

Shows the username of the currently logged-in user.

**Output**

![Whoami](./screenshots/whoami.png)

---

### 4. Display User Information

**Command**

```bash
id
```

**Description**

Displays the user's UID, GID, and group memberships.

**Output**

![ID](./screenshots/id.png)

---

### 5. Display Ubuntu Version

**Command**

```bash
cat /etc/os-release
```

**Description**

Displays detailed information about the installed Ubuntu operating system.

**Output**

![Ubuntu Version](./screenshots/os-release.png)

---

### 6. Display Kernel Version

**Command**

```bash
uname -r
```

**Description**

Displays the running Linux kernel version.

**Output**

![Kernel Version](./screenshots/kernel.png)

---

### 7. Display CPU Information

**Command**

```bash
lscpu
```

**Description**

Displays processor architecture, cores, threads, virtualization support, and CPU model.

**Output**

![CPU Information](./screenshots/lscpu.png)

---

### 8. Display Memory Information

**Command**

```bash
free -h
```

**Description**

Displays RAM and swap memory usage.

**Output**

![Memory Information](./screenshots/free-h.png)

---

### 9. Display Disk Usage

**Command**

```bash
df -h
```

**Description**

Displays mounted file systems and available disk space.

**Output**

![Disk Usage](./screenshots/df-h.png)

---

### 10. Display Network Interfaces

**Command**

```bash
ip addr
```

**Description**

Displays network interfaces and assigned IP addresses.

**Output**

![IP Address](./screenshots/ip-addr.png)

---

### 11. Display Routing Table

**Command**

```bash
ip route
```

**Description**

Displays the routing table and default gateway.

**Output**

![Routing Table](./screenshots/ip-route.png)

---

### 12. Display Date & Time

**Command**

```bash
date
```

**Description**

Displays the current system date and time.

**Output**

![Date](./screenshots/date.png)

---

# 📂 Directory Structure

```
01-system-information/
├── README.md
└── screenshots/
    ├── hostname.png
    ├── hostnamectl.png
    ├── whoami.png
    ├── id.png
    ├── os-release.png
    ├── kernel.png
    ├── lscpu.png
    ├── free-h.png
    ├── df-h.png
    ├── ip-addr.png
    ├── ip-route.png
    └── date.png
```

---

# ✅ Skills Practiced

- Linux System Information
- Ubuntu Server Administration
- User Identification
- Hardware Inspection
- Memory Monitoring
- Disk Monitoring
- Network Configuration
- Routing Information
- Basic Linux Commands

---

# 📖 Key Takeaways

- Learned how to inspect a newly deployed Ubuntu Server.
- Collected hardware and operating system information.
- Verified network and storage configuration.
- Understood the importance of documenting server details before making changes.
