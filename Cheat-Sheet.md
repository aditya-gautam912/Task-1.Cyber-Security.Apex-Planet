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

## Web Testing Checklist

- Inspect requests and responses
- Check authentication and session handling
- Test input validation
- Look for missing access controls
- Review file upload behavior
- Look for exposed admin endpoints
- Record proof clearly

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
