# Linux Day 02 — File Permissions, Users and Groups

## What I Learned Today

Today I learned how Linux controls access to files and folders using permissions, users, and groups.
Linux security mainly works on three things:

* User (Owner)
* Group
* Others

Each file and directory has specific permissions that define who can read, write, or execute it.

---

# File Permissions in Linux

## Permission Types

| Symbol | Meaning |
| ------ | ------- |
| r      | Read    |
| w      | Write   |
| x      | Execute |

Example:

```bash
-rwxr-xr--
```

Explanation:

* Owner → rwx
* Group → r-x
* Others → r--

---

# Numeric Permission System

Linux also uses numbers for permissions.

| Number | Permission | Meaning                |
| ------ | ---------- | ---------------------- |
| 7      | rwx        | Read + Write + Execute |
| 6      | rw-        | Read + Write           |
| 5      | r-x        | Read + Execute         |
| 4      | r--        | Read only              |
| 0      | ---        | No permission          |

## Common Examples

| Command             | Meaning                                  |
| ------------------- | ---------------------------------------- |
| chmod 755 file.txt  | Owner full access, others read + execute |
| chmod 644 file.txt  | Owner read/write, others read only       |
| chmod 700 script.sh | Only owner has full access               |

---

# chmod Command

Used to change file permissions.

Example:

```bash
chmod 755 script.sh
```

Check permissions:

```bash
ls -l
```

---

# chown Command

Used to change file ownership.

Example:

```bash
sudo chown sneha file.txt
```

---

# Users and Groups

Linux is a multi-user operating system.

## User

A person/account that can log into the system.

## Group

A collection of users with similar access permissions.

Groups help in managing permissions easily.

---

# Important Files

## /etc/passwd

Stores user account information.

```bash
cat /etc/passwd
```

## /etc/group

Stores group information.

```bash
cat /etc/group
```

---

# Practical Tasks Performed

## Created Users

```bash
sudo useradd user1
sudo useradd user2
sudo useradd user3
```

## Set Passwords

```bash
sudo passwd user1
sudo passwd user2
sudo passwd user3
```

---

# Created Group

```bash
sudo groupadd developers
```

---

# Added Users to Group

```bash
sudo usermod -aG developers user1
```

---

# Created Files

```bash
touch notes.txt
touch script.sh
```

---

# Changed Permissions

```bash
chmod 644 notes.txt
chmod 755 script.sh
```

---

# Key Takeaways

x* Linux permissions are very important for system security.
* chmod changes permissions.
* chown changes ownership.
* Users and groups help manage access control efficiently.
* Numeric permissions like 755 and 644 are commonly used in real systems.

---
