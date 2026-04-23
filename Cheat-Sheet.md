# Cyber Security Ethical Hacking Cheat Sheet

## Quick Ports

| Port | Service |
|------|---------|
| 21 | FTP |
| 22 | SSH |
| 23 | Telnet |
| 25 | SMTP |
| 53 | DNS |
| 80 | HTTP |
| 110 | POP3 |
| 139 | NetBIOS |
| 143 | IMAP |
| 443 | HTTPS |
| 445 | SMB |
| 3306 | MySQL |
| 3389 | RDP |

## Linux Quick Commands

```bash
pwd
ls -la
cd /path/to/dir
cat file.txt
grep -R "keyword" .
find . -name "*.txt"
chmod +x script.sh
ps aux
ss -tulnp
```

## Windows Quick Commands

```powershell
ipconfig /all
whoami
systeminfo
tasklist
netstat -ano
net user
Get-Process
Get-Service
```

## Recon Workflow

1. Identify the target scope.
2. Collect public information.
3. Resolve domains and subdomains.
4. Identify live hosts.
5. Scan ports and services.
6. Enumerate exposed services.
7. Document findings.

## Nmap Quick Notes

- host discovery: find live systems
- port scan: find open ports
- service detection: identify running services
- version detection: estimate service versions
- OS detection: guess operating system
- NSE: scripts for additional checks

## Common Nmap Commands

```bash
nmap 192.168.1.10
nmap -sV 192.168.1.10
nmap -O 192.168.1.10
nmap -sS 192.168.1.10
nmap -p 1-1000 192.168.1.10
nmap -A 192.168.1.10
```

## Nmap Port States

- `open`
- `closed`
- `filtered`
- `unfiltered`

## Web Testing Checklist

- Inspect requests and responses
- Check authentication and session handling
- Test input validation
- Look for missing access controls
- Review file upload behavior
- Look for exposed admin endpoints
- Record proof clearly

## Burp Suite Quick Notes

- Proxy: intercept browser traffic
- Repeater: resend and modify one request at a time
- Intruder: automate repeated input testing
- Decoder: encode/decode data
- Comparer: compare responses and requests
- Target: map discovered endpoints

## Burp Suite Workflow

1. Turn on Burp Proxy.
2. Configure browser proxy settings.
3. Capture request.
4. Send request to Repeater.
5. Modify parameter, cookie, header, or body value.
6. Compare response changes.
7. Save screenshots and notes.

## Common HTTP Status Codes

- `200` - success
- `301/302` - redirect
- `401` - unauthenticated
- `403` - forbidden
- `404` - not found
- `500` - server error

## Useful Things to Inspect in Burp

- query parameters
- form fields
- cookies
- authorization headers
- hidden fields
- file upload requests
- JSON request bodies

## Password and Auth Notes

- Prefer long passphrases over short complex passwords
- Use MFA where possible
- Store passwords using strong salted hashes
- Enforce lockout or rate limiting
- Never reuse passwords across systems

## Reporting Checklist

- Define scope
- Record timestamps
- Save evidence
- Rate severity
- Explain impact
- Provide remediation steps

## Legal Reminder

Only use these notes in labs, training environments, or systems where you have explicit permission to test.
