---
cover: ../../.gitbook/assets/CrackMapExec - LDAP Modules.png
coverY: 84.58149779735683
---

# 2⃣ LDAP CrackMapExec

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

```
crackmapexec ldap <IP> -u <User> -p <Password> --kdcHost <Host> --admin-count
crackmapexec ldap <IP> -u <User> -p <Password> --kdcHost <Host>  --asreproast ASREPROAST
crackmapexec ldap <IP> -u <User> -p <Password> --kdcHost <Host>  --groups
crackmapexec ldap'<IP> -u <User> -p <Password> --kdcHost <Host>  --kerberoasting KERBEROASTING
crackmapexec ldap <IP> -u <User> -p <Password> --kdcHost <Host>  --password-not-required
crackmapexec ldap <IP> -u <User> -p <Password> --kdcHost <Host>  --trusted-for-delegation
crackmapexec ldap <IP> -u <User> -p <Password> --kdcHost <Host>  --users

# Modules
crackmapexec ldap <IP> -u <User> -p <Password> --kdcHost <Host> -M get-desc-users
crackmapexec ldap <IP> -u <User> -p <Password> --kdcHost <Host> -M laps
crackmapexec ldap <IP> -u <User> -p <Password> --kdcHost <Host> -M ldap-signing
```
