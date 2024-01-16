---
description: >-
  Explore our detailed article on CrackMapExec RDP, an essential tool for
  network admins and cybersecurity specialists. Learn its uses, features, and
  benefits. Your ultimate guide on CrackMapExec RDP.
cover: ../.gitbook/assets/GitBook Covers (1).png
coverY: 0
---

# RDP CrackMapExec



```bash
crackmapexec rdp [-h] [-id CRED_ID [CRED_ID ...]] [-u USERNAME [USERNAME ...]] [-p PASSWORD [PASSWORD ...]] [-k] [--use-kcache] [--export EXPORT [EXPORT ...]]
[--aesKey AESKEY [AESKEY ...]] [--kdcHost KDCHOST] [--gfail-limit LIMIT | --ufail-limit LIMIT | --fail-limit LIMIT] [-M MODULE]
[-o MODULE_OPTION [MODULE_OPTION ...]] [-L] [--options] [--server {http,https}] [--server-host HOST] [--server-port PORT] [--connectback-host CHOST]
[-H HASH [HASH ...]] [--no-bruteforce] [--continue-on-success] [--port PORT] [--rdp-timeout RDP_TIMEOUT] [--nla-screenshot] [-d DOMAIN | --local-auth]
[--screenshot] [--screentime SCREENTIME] [--res RES]
[target ...]
```

```bash
 --port PORT           Custom RDP port
  --rdp-timeout RDP_TIMEOUT
                        RDP timeout on socket connection
  --nla-screenshot      Screenshot RDP login prompt if NLA is disabled
  -d DOMAIN             domain to authenticate to
  --local-auth          authenticate locally to each target

Screenshot:
  Remote Desktop Screenshot

  --screenshot          Screenshot RDP if connection success
  --screentime SCREENTIME
                        Time to wait for desktop image
  --res RES             Resolution in "WIDTHxHEIGHT" format. Default: "1024x768"
```
