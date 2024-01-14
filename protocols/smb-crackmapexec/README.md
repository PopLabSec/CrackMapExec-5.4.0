---
description: >-
  This article discusses the use of CrackMapExec 5.4 to attack SMB (Samba)
  protocols. Learn how to use this powerful tool to exploit the weaknesses in
  SMB protocols and gain access to confidential data
cover: ../../.gitbook/assets/CrackMapExec - SMB Modules.png
coverY: 95.85903083700441
---

# 1⃣ SMB CrackMapExec

### Mapping/Enumeration

The SMB Mapping/Enumeration option in CrackMapExec allows the user to scan a network for shares, users, and groups that are accessible via the SMB protocol.&#x20;

This option is useful for reconnaissance and information-gathering purposes, as it provides insight into the structure of a network and the resources that are available to attackers.

{% code overflow="wrap" %}
```
Options for Mapping/Enumerating

  --shares              enumerate shares and access
  --sessions            enumerate active sessions
  --disks               enumerate disks
  --loggedon-users-filter LOGGEDON_USERS_FILTER
                        only search for specific user, works with regex
  --loggedon-users      enumerate logged on users
  --users [USER]        enumerate domain users, if a user is specified than only its information is queried.
  --groups [GROUP]      enumerate domain groups, if a group is specified than its members are enumerated
  --computers [COMPUTER]
                        enumerate computer users
  --local-groups [GROUP]
                        enumerate local groups, if a group is specified then its members are enumerated
  --pass-pol            dump password policy
  --rid-brute [MAX_RID]
                        enumerate users by bruteforcing RID's (default: 4000)
  --wmi QUERY           issues the specified WMI query
  --wmi-namespace NAMESPACE
                        WMI Namespace (default: root\cimv2)
```
{% endcode %}

### Credential Gathering

One of the most powerful features of CrackMapExec, when used with the SMB protocol, is its ability to gather credentials from target systems.&#x20;

This feature can be incredibly valuable for penetration testers and security professionals, as it allows them to identify potential security weaknesses and vulnerabilities within an organization's network.

```
Options for gathering credentials

  --enabled             Only dump enabled targets from DC
  --user USERNTDS       Dump selected user from DC
  --sam                 dump SAM hashes from target systems
  --lsa                 dump LSA secrets from target systems
  --ntds [{drsuapi,vss}] dump the NTDS.dit from target DCs using the
   specifed method (default: drsuapi)
```

### Spidering

The "spider" feature in CrackMapExec (CME) allows users to discover and map the available network shares on a target system.&#x20;

Specifically, the SMB spidering option in CME enables users to enumerate shares, recursively spider directories, and retrieve file information.

```
Options for spidering shares

  --spider SHARE        share to spider
  --spider-folder FOLDER
                        folder to spider (default: root share directory)
  --content             enable file content searching
  --exclude-dirs DIR_LIST
                        directories to exclude from spidering
  --pattern PATTERN [PATTERN ...]
                        pattern(s) to search for in folders, filenames and file content
  --regex REGEX [REGEX ...]
                        regex(s) to search for in folders, filenames and file content
  --depth DEPTH         max spider recursion depth (default: infinity & beyond)
  --only-files          only spider files

```

### Files

```
Options for put and get remote files

  --put-file FILE FILE  Put a local file into remote target, ex: whoami.txt \\Windows\\Temp\\whoami.txt
  --get-file FILE FILE  Get a remote file, ex: \\Windows\\Temp\\whoami.txt whoami.txt
```

### Command Execution

The SMB Command Execution option in CrackMapExec allows users to execute commands on target systems using the Server Message Block (SMB) protocol.&#x20;

This can be a powerful feature for penetration testers and security researchers, as it allows them to execute commands remotely on target systems without having to physically access them or install any additional software.

```
Command Execution:
  Options for executing commands

  --exec-method {wmiexec,smbexec,atexec,mmcexec}
                        method to execute the command. Ignored if in MSSQL mode (default: wmiexec)
  --codec CODEC         Set encoding used (codec) from the target's output (default "utf-8"). If errors are detected, run chcp.com at the target, map the result with
                        https://docs.python.org/3/library/codecs.html#standard-encodings and then execute again with --codec and the corresponding codec
  --force-ps32          force the PowerShell command to run in a 32-bit process
  --no-output           do not retrieve command output
  -x COMMAND            execute the specified command
  -X PS_COMMAND         execute the specified PowerShell command

```

### Powershell Obfuscation

The CrackMapExec tool includes an option for obfuscating PowerShell commands used during SMB exploitation.&#x20;

This option can be useful for avoiding detection by security tools that may be monitoring for suspicious PowerShell activity.

```
Options for PowerShell script obfuscation

  --obfs                Obfuscate PowerShell scripts
  --amsi-bypass FILE    File with a custom AMSI bypass
  --clear-obfscripts    Clear all cached obfuscated PowerShell scripts
```

