# Linux Day 01 — Linux Basics and Terminal Commands

# What I Learned Today

Today I started my Linux journey by learning the fundamentals of Linux, terminal basics, and essential commands used in daily system operations.

I also explored the Linux filesystem structure, popular Linux distributions, and basic command-line navigation using Ubuntu on WSL2.

---

# What is Linux?

Linux is an open-source operating system kernel used to build different operating systems called distributions (distros).

It is widely used in:

* Servers
* Cloud platforms
* DevOps environments
* Networking systems
* Cybersecurity
* Automation

Linux is known for:

* Stability
* Security
* Performance
* Flexibility

---

# Popular Linux Distributions

| Distribution                    | Purpose                               |
| ------------------------------- | ------------------------------------- |
| Ubuntu                          | Beginner-friendly and widely used     |
| CentOS                          | Enterprise server environments        |
| RHEL (Red Hat Enterprise Linux) | Commercial enterprise Linux           |
| Debian                          | Stable and lightweight systems        |
| Kali Linux                      | Cybersecurity and penetration testing |

---

# Linux Filesystem Structure

Linux follows a hierarchical filesystem structure.

## Important Directories

| Directory | Purpose                                    |
| --------- | ------------------------------------------ |
| /home     | Stores user files and personal directories |
| /etc      | Configuration files                        |
| /var      | Logs and variable data                     |
| /bin      | Essential system commands                  |
| /usr      | User applications and utilities            |
| /tmp      | Temporary files                            |

---

# WSL2 Setup

Installed:

* WSL2 (Windows Subsystem for Linux)
* Ubuntu on Windows

This allows Linux commands and tools to run directly on Windows.

---

# Basic Linux Commands

## pwd

Displays current working directory.

```bash id="v5x2ow"
pwd
```

Example Output:

```text id="m8r1kp"
/home/sneha
```

---

## ls

Lists files and folders.

```bash id="u3p7zd"
ls
```

---

## cd

Used to change directory.

```bash id="x9m4vq"
cd Documents
```

---

## mkdir

Creates a new directory.

```bash id="j2u8kr"
mkdir linux-notes
```

---

## touch

Creates an empty file.

```bash id="t6v1ow"
touch day01.md
```

---

## rm

Removes files or directories.

```bash id="r4m9xp"
rm file.txt
```

---

## cp

Copies files or folders.

```bash id="p8u2vk"
cp file1.txt file2.txt
```

---

## mv

Moves or renames files.

```bash id="w1x5qd"
mv old.txt new.txt
```

---

## cat

Displays file content.

```bash id="e7m3ow"
cat day01.md
```

---

## echo

Prints text output.

```bash id="q2v8kr"
echo "Hello Linux"
```

---

# Key Takeaways

* Linux is heavily used in cloud and DevOps environments.
* The terminal is a powerful way to interact with Linux systems.
* Understanding filesystem structure is important for system administration.
* Basic commands like `pwd`, `ls`, and `cd` are used frequently in daily workflows.
* WSL2 makes Linux practice easy on Windows systems.

---

# Practical Tasks Performed

* Installed Ubuntu using WSL2
* Navigated directories using terminal commands
* Created folders and files
* Practiced file management commands
* Initialized first GitHub repository for Linux notes

Linux is case sensitive.
-
--

