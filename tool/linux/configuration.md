---
description: >-
  Learn how to optimize your CrackMapExec tool using custom certificates, third
  party integrations.
cover: ../../.gitbook/assets/GitBook Covers (1).png
coverY: 0
---

# Configuration

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

### CME Configuration folder

```bash
┌──(rfs㉿local-c2)-[~]
└─$ cd ~/.cme
```

### Change CrackMapExec certificate

```
┌──(kali㉿local-c2)-[~/.cme]
└─$ vi ~/.cme/cme.conf
```

{% code overflow="wrap" %}
```bash
openssl req -newkey rsa:2048 -new -nodes -x509 -days 3650 -keyout key.pem -out cert.pem
```
{% endcode %}
