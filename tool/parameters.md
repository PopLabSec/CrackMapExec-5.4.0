---
cover: ../.gitbook/assets/GitBook Covers (1).png
coverY: 0
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 🟢 Parameters

{% code overflow="wrap" %}
```
usage: crackmapexec [-h] [-t THREADS] [--timeout TIMEOUT] [--jitter INTERVAL] [--darrell] [--verbose] {smb,rdp,ftp,ssh,ldap,winrm,mssql} ...
```
{% endcode %}

```
options:
  -h, --help            show this help message and exit
  -t THREADS            set how many concurrent threads to use (default: 100)
  --timeout TIMEOUT     max timeout in seconds of each thread (default: None)
  --jitter INTERVAL     sets a random delay between each connection (default: None)
  --darrell             give Darrell a hand
  --verbose             enable verbose output
```

```
protocols:
  available protocols

  {smb,rdp,ftp,ssh,ldap,winrm,mssql}
    smb                 own stuff using SMB
    rdp                 own stuff using RDP
    ftp                 own stuff using FTP
    ssh                 own stuff using SSH
    ldap                own stuff using LDAP
    winrm               own stuff using WINRM
    mssql               own stuff using MSSQL
```
