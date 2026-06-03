# Linux Day 03 — Processes, Services and systemctl

# What I Learned Today

Today I learned how Linux manages running programs using processes and services.

A process is simply a running program. Linux constantly runs multiple processes in the background for system operations.

I also learned how to monitor processes, stop them, and manage services using `systemctl`.

---

# Process Management Commands

## ps Command

Used to display currently running processes.

```bash id="v3u8kp"
ps
```

---

## ps aux

Displays detailed information about all running processes.

```bash id="f6m2ow"
ps aux
```

### Important Columns

| Column  | Meaning          |
| ------- | ---------------- |
| USER    | Owner of process |
| PID     | Process ID       |
| %CPU    | CPU usage        |
| %MEM    | Memory usage     |
| COMMAND | Running command  |

---

# PID (Process ID)

Every running process in Linux has a unique Process ID.

Example:

```text id="r8x1vq"
722
```

This ID is used to manage or terminate processes.

---

# top Command

Used for real-time system monitoring.

```bash id="j4p7zd"
top
```

It shows:

* CPU usage
* Memory usage
* Running processes
* System load

Exit top:

```text id="m2v9kr"
q
```

---

# htop Command

A more interactive and user-friendly version of `top`.

## Installation

```bash id="u7n3xp"
sudo apt install htop
```

## Run

```bash id="k5r1ow"
htop
```

Exit:

```text id="t9x4mq"
q
```

---

# kill Command

Used to terminate a process using PID.

Example:

```bash id="e1u7vk"
kill 722
```

---

# pkill Command

Used to terminate a process using process name.

Example:

```bash id="c6m8zp"
pkill nginx
```

---

# Services in Linux

Services are background programs that continuously run and support system operations.

Examples:

* nginx
* ssh
* docker

---

# systemctl Command

Used to manage Linux services.

Common operations:

* start
* stop
* restart
* status

---

# Installing nginx

```bash id="s2v8ow"
sudo apt update
sudo apt install nginx
```

---

# Starting nginx

```bash id="n4m7xp"
sudo systemctl start nginx
```

---

# Checking Service Status

```bash id="y1u5kr"
sudo systemctl status nginx
```

If the service is running properly, Linux shows:

```text id="d7p2vq"
active (running)
```

---

# Restarting nginx

```bash id="x6r9ow"
sudo systemctl restart nginx
```

---

# Stopping nginx

```bash id="f3u1zp"
sudo systemctl stop nginx
```

---

# Finding nginx Process

```bash id="q8m4vk"
ps aux | grep nginx
```

This command filters and displays nginx-related processes.

---

# Key Difference Between Commands

| Command   | Purpose                 |
| --------- | ----------------------- |
| ps        | Process snapshot        |
| top       | Real-time monitoring    |
| htop      | Interactive monitoring  |
| kill      | Stop process using PID  |
| pkill     | Stop process using name |
| systemctl | Manage services         |

---

# Practical Tasks Performed

* Viewed running processes using `ps`
* Monitored system resources using `top`
* Installed and tested `htop`
* Installed nginx web server
* Started and stopped nginx service
* Checked nginx status using `systemctl`
* Verified nginx process using `ps aux`

---

# Key Takeaways

* Every running program in Linux is a process.
* PID uniquely identifies each process.
* `top` and `htop` help monitor system performance.
* `kill` and `pkill` are used for process management.
* `systemctl` is essential for managing Linux services.
* nginx is commonly used as a web server and reverse proxy.

---
