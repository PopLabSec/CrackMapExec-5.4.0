---
description: >-
  CrackMapExec can use different types to define our target, we can use IPs,
  domains, CIDRs, Ranges, or a files containing all hosts.
cover: ../.gitbook/assets/GitBook Covers (1).png
coverY: 0
---

# 🟢 Target Definition - CME

### Scan a subnet

```
crackmapexec <protocol> 192.168.10.0/24
```

### Use a domain

```
crackmapexec <protocol> ms.poplabsec.com
```

### Define multiple IP Ranges

```
crackmapexec <protocol> 192.168.2.0-28 192.168.10.1-67
```

### Import IPs from a text File

```
crackmapexec <protocol> ~/hosts.txt
```

### Use a Nmap output File

### Use Nessus output file
