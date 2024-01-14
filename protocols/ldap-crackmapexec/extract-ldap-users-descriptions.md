---
description: Use crackmapexec to extract LDAP user descriptions.
cover: ../../.gitbook/assets/GitBook Covers (1).png
coverY: 0
---

# 🟠 Extract LDAP users descriptions



```
crackmapexec ldap rfs.lab -u 'username' -p 'password' -M user-desc
```

{% code overflow="wrap" %}
```
crackmapexec ldap 10.0.2.11 -u 'username' -p 'password' --kdcHost 10.0.2.11 -M get-desc-users
```
{% endcode %}

{% code overflow="wrap" %}
```
GET-DESC... 10.0.2.11       389    dc01    [+] Found following users: 
GET-DESC... 10.0.2.11       389    dc01    User: Guest description: Built-in account for guest access to the computer/domain
GET-DESC... 10.0.2.11       389    dc01    User: krbtgt description: Key Distribution Center Service Account
```
{% endcode %}
