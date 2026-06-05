# Linux Day 05 — Logs, grep and Vim Basics

# What I Learned Today

Today I learned how Linux stores logs, how to search log files efficiently using grep, monitor logs in real time using tail, view system logs using journalctl, and edit files using Vim.

These tools are commonly used for troubleshooting and system administration.

---

# Linux Log Files

Linux stores logs inside:

```bash
/var/log
```

Common log locations:

| Log File                  | Purpose             |
| ------------------------- | ------------------- |
| /var/log/syslog           | General system logs |
| /var/log/auth.log         | Authentication logs |
| /var/log/kern.log         | Kernel logs         |
| /var/log/nginx/access.log | Nginx access logs   |
| /var/log/nginx/error.log  | Nginx error logs    |

---

# tail Command

Displays the last lines of a file.

```bash
tail /var/log/syslog
```

---

# tail -f

Monitors logs in real time.

```bash
tail -f /var/log/nginx/access.log
```

Common Use Cases:

* Monitor live traffic
* Troubleshoot applications
* Watch logs as they are generated

---

# grep Command

Used to search text patterns inside files.

Basic Example:

```bash
grep nginx /var/log/syslog
```

---

# grep Cheat Sheet

## grep -i

Case-insensitive search.

```bash
grep -i error file.log
```

Matches:

* ERROR
* Error
* error

---

## grep -n

Displays matching lines with line numbers.

```bash
grep -n error file.log
```

---

## grep -v

Displays lines that do NOT match.

```bash
grep -v error file.log
```

---

## grep -r

Recursive search inside directories.

```bash
grep -r nginx /var/log
```

---

# Searching Specific IP Addresses

Example:

```bash
grep 192.168.1.10 access.log
```

Used to find activity from a particular IP address.

---

# journalctl

Used to view systemd logs.

Display all logs:

```bash
journalctl
```

---

# View Service Logs

Example:

```bash
journalctl -u nginx
```

Displays logs related to the nginx service.

---

# Recent Critical Logs

```bash
journalctl -xe
```

Useful for troubleshooting system issues.

---

# Vim Basics

Vim is a command-line text editor widely used in Linux administration.

Open a file:

```bash
vim test.txt
```

---

# Insert Mode

Press:

```text
i
```

Start typing content.

---

# Save and Exit

Press:

```text
ESC
```

Then:

```text
:wq
```

Press Enter.

Meaning:

* Write
* Quit

---

# Exit Without Saving

Press:

```text
ESC
```

Then:

```text
:q!
```

Press Enter.

---

# Common Vim Workflow

```bash
vim file.txt
```

Press:

```text
i
```

Edit file.

Press:

```text
ESC
```

Then:

```text
:wq
```

Save and exit.

---

# Practical Tasks Performed

* Explored log files under /var/log
* Viewed logs using tail
* Monitored logs in real time using tail -f
* Searched logs using grep
* Filtered log entries using grep flags
* Viewed nginx logs using journalctl
* Edited files using Vim

---

# Key Takeaways

* Logs are essential for troubleshooting Linux systems.
* grep is one of the most important commands for searching log files.
* tail -f allows real-time log monitoring.
* journalctl helps investigate service and system events.
* Vim is a powerful editor commonly used on Linux servers.
* Most production troubleshooting starts by checking logs.

---
