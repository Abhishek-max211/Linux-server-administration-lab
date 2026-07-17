# 👥 User & Group Administration

> **Module 02** of the Linux Administration Lab

## 📖 Overview

User and Group Administration is one of the core responsibilities of a Linux System Administrator. It involves creating users and groups, assigning permissions, managing user accounts, and controlling administrative access to maintain a secure multi-user environment.

---

## 🎯 Objectives

In this lab, you will learn how to:

- Create users
- Create groups
- Assign primary and secondary groups
- Set user passwords
- Modify user accounts
- Verify user information
- Grant administrative privileges
- Delete users and groups

---

## 💼 Scenario

As a Linux Administrator at **TechNova Pvt. Ltd.**, you have been asked to onboard new employees from different departments. Your task is to create user accounts, organize them into groups, assign administrative privileges where required, and verify the configuration.

---

# 📋 Commands Used

```bash
# Create Groups
sudo groupadd developers
sudo groupadd sysadmins

# Create Users
sudo useradd -m -g developers alice
sudo useradd -m -g developers bob
sudo useradd -m -g sysadmins john

# Set Passwords
sudo passwd alice
sudo passwd bob
sudo passwd john

# Add User to Secondary Group
sudo usermod -aG developers john

# Grant Administrative Privileges
sudo usermod -aG sudo john

# Verify User Information
id alice
id bob
id john

groups john

# Display User Details
getent passwd alice
getent group developers

# Delete User
sudo userdel -r alice

# Delete Group
sudo groupdel developers
```

---

# 📸 Lab Execution

## Screenshot 1 – Create Users & Groups

The following tasks were completed:

- Created groups
- Created users
- Assigned primary groups
- Set passwords

![Create Users & Groups](./screenshots/user-group-1.png)

---

## Screenshot 2 – User Verification

Verified:

- User ID
- Group Membership
- User Information

Commands used:

```bash
id alice
id bob
id john
groups john
```

![User Verification](./screenshots/user-group-2.png)

---

## Screenshot 3 – Administrative Privileges

Granted sudo access and verified user details.

Commands used:

```bash
sudo usermod -aG sudo john

groups john

id john
```

![Administrative Access](./screenshots/user-group-3.png)

---

## Screenshot 4 – User & Group Cleanup

Removed unnecessary users and groups.

Commands used:

```bash
sudo userdel -r alice

sudo groupdel developers
```

![Cleanup](./screenshots/user-group-4.png)

---

# ✅ Outcome

After completing this lab, I successfully:

- Created Linux users
- Created Linux groups
- Assigned primary and secondary groups
- Set passwords
- Granted administrative privileges
- Verified user information
- Managed user accounts
- Deleted users and groups

---

# 📁 Directory Structure

```text
02-user-group-administration/
├── README.md
└── screenshots/
    ├── user-group-1.png
    ├── user-group-2.png
    ├── user-group-3.png
    └── user-group-4.png
```

---

# 📚 Commands Practiced

```bash
groupadd
groupdel
useradd
userdel
usermod
passwd
id
groups
getent
```

---

# 🎓 Skills Practiced

- Linux User Management
- Linux Group Management
- User Account Administration
- Administrative Access Management
- User Verification
- Linux Security Fundamentals

---

# 📌 Key Takeaways

- Learned how to create and manage Linux users.
- Organized users using primary and secondary groups.
- Assigned administrative privileges using the `sudo` group.
- Verified user and group configurations.
- Practiced managing user accounts in a multi-user Linux environment.

---

## 🚀 Next Module

➡️ **03 - File & Directory Management**
