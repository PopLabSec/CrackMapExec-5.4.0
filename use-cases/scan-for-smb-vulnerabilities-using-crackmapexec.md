---
description: Scan for Samba vulnerabilities with CrackMapExec
---

# 🔥 Scan for SMB Vulnerabilities using CrackMapExec

### ZeroLogon

Module to check if the DC is vulnerable to Zerologon aka CVE-2020-1472

```
crackmapexec smb <ip> -u '' -p '' -M zerologo
```

### PetitPotam

Module to check if the DC is vulnerable to PetitPotam, credit to @topotam

```
crackmapexec smb <ip> -u '' -p '' -M petitpotam
```

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

### noPAC

Check if the DC is vulnerable to CVE-2021-42278 and CVE-2021-42287 to impersonate DA from standard domain user

```
crackmapexec smb <ip> -u 'user' -p 'pass' -M nopac
```
