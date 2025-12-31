# HTB – MonitorsFour

**Difficulty:** Easy  
**OS:** Windows  
**Attack Chain:** Web → API → App → Container → Host

---

## Overview
This write-up documents the exploitation of the HTB *MonitorsFour* machine.
The engagement demonstrates how multiple misconfigurations and logic flaws
can be chained to achieve full host compromise.

---

## Attack Summary
1. Web enumeration revealed exposed configuration files
2. API authentication bypass via PHP type juggling
3. User data disclosure and MD5 hash cracking
4. Authenticated RCE in Cacti (CVE-2025-24367)
5. Initial shell inside Docker container
6. Docker API abuse (port 2375)
7. Host filesystem mount → root access

---

## Key Vulnerabilities
- Exposed `.env` file
- API authentication logic flaw
- Weak password hashing (MD5)
- Vulnerable Cacti version
- Unauthenticated Docker API

---

## Tools Used
Nmap, Dirsearch, FFUF, curl, Hashcat, Netcat, Bash, Docker API

---

## Lessons Learned
- Containers are not a security boundary
- API logic flaws can be more dangerous than missing auth
- Small misconfigurations compound into full compromise

---

## Mitigations
- Restrict access to sensitive configuration files such as `.env`
- Use strict comparison (`===`) for authentication logic
- Implement strong password hashing (bcrypt or argon2)
- Keep third-party software (Cacti) fully patched
- Disable unauthenticated Docker API access (port 2375)
- Enforce container isolation and network segmentation

---

## Skills Demonstrated
- Web & API Enumeration
- Authentication Logic Flaw Exploitation
- Password Hash Cracking
- Authenticated Remote Code Execution
- Container Escape Techniques
- Docker API Abuse

---

## Disclaimer
This write-up is for educational purposes only.
All testing was performed in a controlled HTB lab environment.

