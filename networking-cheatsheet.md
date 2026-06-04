# Linux Networking Cheat Sheet

# Purpose

This cheat sheet contains commonly used Linux networking commands for troubleshooting, connectivity testing, DNS verification, route analysis, and service validation.

---

# Check Connectivity

## ping

Used to verify whether a host is reachable.

```bash
ping google.com
```

Common Use Cases:

* Verify internet connectivity
* Check server reachability
* Measure latency

---

# HTTP Requests

## curl

Transfers data from or to a server.

```bash
curl https://google.com
```

View HTTP headers:

```bash
curl -I https://google.com
```

Common Use Cases:

* API testing
* HTTP header inspection
* Connectivity validation

---

## wget

Download files from the internet.

```bash
wget https://example.com/file.zip
```

Common Use Cases:

* Download packages
* Retrieve files from remote servers

---

# Route Analysis

## traceroute

Displays the path packets take to reach a destination.

```bash
traceroute google.com
```

Common Use Cases:

* Identify routing issues
* Network path troubleshooting

---

# Socket and Port Analysis

## netstat

Displays network connections and listening ports.

```bash
netstat -tulnp
```

Common Use Cases:

* Check listening services
* Verify open ports

---

## ss

Modern replacement for netstat.

```bash
ss -tulnp
```

Options:

| Option | Meaning             |
| ------ | ------------------- |
| t      | TCP                 |
| u      | UDP                 |
| l      | Listening           |
| n      | Numeric output      |
| p      | Process information |

Common Use Cases:

* Verify application ports
* Identify active listeners

---

# DNS Troubleshooting

## nslookup

Resolve domain names.

```bash
nslookup google.com
```

Common Use Cases:

* DNS verification
* Name resolution troubleshooting

---

## dig

Advanced DNS query tool.

```bash
dig google.com
```

Useful Record Types:

```bash
dig google.com A
dig google.com MX
dig google.com NS
```

Common Use Cases:

* DNS troubleshooting
* Mail server validation
* DNS record inspection

---

# Interface Information

## ip addr

Displays IP addresses and interfaces.

```bash
ip addr
```

Common Use Cases:

* Check assigned IP address
* Verify interface status

---

# Routing Information

## ip route

Displays routing table.

```bash
ip route
```

Example Output:

```text
default via 192.168.1.1 dev eth0
```

Common Use Cases:

* Verify default gateway
* Troubleshoot routing issues

---

# Practical Troubleshooting Workflow

## Step 1: Verify Connectivity

```bash
ping google.com
```

## Step 2: Verify DNS

```bash
nslookup google.com
```

## Step 3: Check Interface

```bash
ip addr
```

## Step 4: Verify Routes

```bash
ip route
```

## Step 5: Check Open Ports

```bash
ss -tulnp
```

## Step 6: Test HTTP Connectivity

```bash
curl -I https://google.com
```

---

# Commands I Practiced

```bash
ping
curl
wget
traceroute
netstat
ss
nslookup
dig
ip addr
ip route
```

---

# Key Takeaways

* ping validates connectivity.
* curl is useful for HTTP testing and API verification.
* traceroute identifies packet paths across networks.
* ss helps identify listening ports and active connections.
* nslookup and dig assist in DNS troubleshooting.
* ip addr displays interface details.
* ip route displays routing information.

This cheat sheet serves as a quick reference for Linux networking and troubleshooting tasks.
