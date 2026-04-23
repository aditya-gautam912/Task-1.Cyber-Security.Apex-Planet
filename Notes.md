# Cyber Security Ethical Hacking Notes

## 1. Cyber Security Basics

Cyber security is the practice of protecting systems, networks, applications, and data from unauthorized access, misuse, disruption, or destruction.

### Core security goals

- Confidentiality: data is only accessible to authorized users
- Integrity: data remains accurate and unmodified
- Availability: systems and data remain accessible when needed

### Common terms

- Vulnerability: a weakness in a system
- Threat: something capable of causing harm
- Risk: likelihood and impact of a threat exploiting a vulnerability
- Exploit: a method used to take advantage of a vulnerability
- Patch: a fix that removes or reduces a vulnerability

## 2. Ethical Hacking

Ethical hacking is the legal and authorized process of testing systems to identify weaknesses before attackers do.

### Main phases

1. Reconnaissance
2. Scanning and enumeration
3. Gaining access
4. Privilege escalation
5. Maintaining access
6. Clearing traces
7. Reporting and remediation

### Types of hackers

- White hat: authorized and defensive
- Black hat: malicious and unauthorized
- Gray hat: operates without full authorization, still risky and often illegal

## 3. Networking Basics

### Common protocols

- HTTP/HTTPS: web traffic
- DNS: domain name resolution
- FTP/SFTP: file transfer
- SSH: secure remote shell
- SMTP/IMAP/POP3: email

### Common ports

- 20/21: FTP
- 22: SSH
- 23: Telnet
- 25: SMTP
- 53: DNS
- 80: HTTP
- 110: POP3
- 143: IMAP
- 443: HTTPS
- 445: SMB
- 3306: MySQL
- 3389: RDP

### TCP vs UDP

- TCP is connection-oriented and reliable
- UDP is connectionless and faster but less reliable

## 4. Reconnaissance

Reconnaissance is information gathering about a target.

### Passive recon

- search engines
- public websites
- job posts
- social media
- public DNS and WHOIS data

### Active recon

- ping sweeps
- port scanning
- service detection
- DNS interrogation

## 5. Scanning and Enumeration

### Purpose

- discover live hosts
- identify open ports
- detect running services
- enumerate users, shares, and software versions

### Examples of enumeration targets

- SMB shares
- DNS records
- web directories
- banner information
- exposed admin panels

## 6. Nmap Basics

Nmap is a network scanning tool used to discover hosts, open ports, running services, and operating system clues in authorized environments.

### What Nmap is used for

- host discovery
- port scanning
- service version detection
- operating system detection
- basic network inventory
- security assessment preparation

### Important concepts

- host discovery: checks whether a system is online
- port scanning: identifies open, closed, or filtered ports
- service detection: identifies the application running on a port
- version detection: estimates service version details
- OS detection: guesses the target operating system
- NSE: Nmap Scripting Engine used for additional checks

### Common port states

- open: a service is accepting connections
- closed: the port is reachable but no service is listening
- filtered: a firewall or filter is blocking visibility
- unfiltered: reachable, but exact state is unclear

### Scan types to know conceptually

- TCP connect scan: full TCP connection attempt
- SYN scan: half-open style scan often used for speed
- UDP scan: checks UDP services, usually slower
- version scan: identifies service versions
- OS detection scan: guesses the operating system

### Good practice

- verify scope before scanning
- start with basic discovery before deep scanning
- avoid aggressive scanning unless authorized
- document IPs, ports, and detected services clearly
- use results to guide enumeration, not as final proof alone

## 7. Web Application Basics

### Common issues

- SQL injection
- Cross-Site Scripting (XSS)
- Cross-Site Request Forgery (CSRF)
- file upload flaws
- broken authentication
- insecure direct object references
- security misconfiguration

### Basic testing mindset

- map the application
- inspect requests and responses
- test input validation
- review authentication and session handling
- verify access controls

## 8. Burp Suite Basics

Burp Suite is a web application security testing tool commonly used to inspect, intercept, and modify HTTP/HTTPS traffic during authorized testing.

### Main Burp Suite components

- Proxy: intercepts browser requests and responses
- Target: helps map the application structure
- Repeater: re-sends modified requests manually
- Intruder: automates repeated request testing
- Decoder: converts data between formats
- Comparer: compares two requests or responses

### Common use cases

- inspect request headers, parameters, cookies, and responses
- capture login flows and session tokens
- modify requests to test input validation
- replay requests with changed values
- identify hidden parameters and endpoints
- test authorization behavior by changing IDs, roles, or tokens

### Safe beginner workflow

1. Configure the browser to use Burp Proxy.
2. Visit the target application in scope.
3. Intercept and observe the request.
4. Send interesting requests to Repeater.
5. Modify one input at a time and review the response.
6. Record useful findings and screenshots.

### Concepts to understand

- request methods: `GET`, `POST`, `PUT`, `DELETE`
- headers: metadata such as cookies, content type, and authorization
- query parameters: values passed in the URL
- body parameters: values sent in the request body
- cookies and sessions: identify logged-in state
- status codes: `200`, `302`, `403`, `404`, `500`

### Good practice

- test only in authorized environments
- keep scope limited to approved targets
- change one variable at a time
- save clean evidence for reports
- avoid noisy automated testing unless allowed

## 9. Authentication and Password Security

### Good password practices

- long and unique passwords
- password managers
- multi-factor authentication
- account lockout and rate limiting

### Hashing concepts

- hashing is one-way
- encryption is reversible with a key
- salting makes password hashes harder to crack at scale

## 10. Linux Basics

### Useful commands

- `pwd` - show current directory
- `ls -la` - list files with details
- `cd` - change directory
- `cat` - read file contents
- `grep` - search text
- `find` - locate files
- `chmod` - change permissions
- `ps aux` - list processes
- `netstat -tulnp` or `ss -tulnp` - list listening ports

## 11. Windows Basics

### Useful commands

- `ipconfig`
- `whoami`
- `net user`
- `tasklist`
- `systeminfo`
- `netstat -ano`
- `Get-Process`
- `Get-Service`

## 12. Reporting

The report is one of the most important deliverables in ethical hacking.

### A good report should include

- scope
- methodology
- findings
- severity
- evidence
- business impact
- remediation

### Finding format

- Title
- Description
- Affected asset
- Risk level
- Evidence
- Recommendation

## 13. Defensive Mindset

Security work is not only about finding issues. It also requires reducing risk.

### Defensive actions

- patch systems
- disable unnecessary services
- use least privilege
- segment networks
- monitor logs
- back up data
- enforce MFA

## 14. Legal and Ethical Reminder

Only test systems you are explicitly authorized to assess. Authorization should be written and should clearly define scope, timing, and allowed techniques.
