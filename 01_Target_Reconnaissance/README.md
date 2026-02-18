# Target Reconnaissance & Service Enumeration Report

## Objective

Conduct structured passive and active reconnaissance against target host 192.168.220.113 to identify exposed services, validate connectivity, and assess the attack surface.

---

## Target Overview

- Hostname: ohio.stream.stream
- IP Address: 192.168.220.113

---

## Passive Reconnaissance

- ICMP Ping Test – Confirmed host availability
- Reverse DNS Lookup – No external DNS resolution
- WHOIS Lookup – Failed due to internal network isolation

TLS Inspection:
- Port 443 running HTTPS (Caddy Web Server)
- TLS Version: 1.3
- Cipher: TLS_CHACHA20_POLY1305_SHA256
- ECC 256-bit certificate
- Self-signed certificate identified

---

## Active Reconnaissance

### Full Port Scan
Executed:
nmap -p- 192.168.220.113

Identified exposed services including:
- SSH
- DNS
- HTTP/HTTPS
- SMB (Samba)
- PostgreSQL
- LLMNR
- Additional administrative services

### Service Fingerprinting
Executed:
nmap -sV -sC -O 192.168.220.113

Findings:
- Caddy web server
- Samba SMB service
- PostgreSQL 15.x
- Linux OS fingerprint (Proxmox-managed environment)

---

## Web Application Analysis

- HTTP header validation via curl
- WhatWeb fingerprinting (HTML5 / Caddy server)
- Netcat raw HTTP validation (400 Bad Request confirms service responsiveness)

---

## Attack Surface Summary

The host presents multiple exposed services across networking, database, file sharing, and web services. While TLS encryption is enabled, the presence of numerous open ports increases the potential attack surface.

---

## Skills Demonstrated

- Passive Reconnaissance
- Active Reconnaissance
- Full TCP Port Scanning
- TLS Certificate Analysis
- Service Fingerprinting
- OS Detection
- Web Application Enumeration
- Attack Surface Documentation
