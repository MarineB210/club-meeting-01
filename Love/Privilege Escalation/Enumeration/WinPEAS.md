***
> [!NOTE]  
> WinPEAS output can be quite hard to understand with the amount of information. Always nice to have somewhere notes on potential thing to look up for from this output.

```
����������͹ Checking AlwaysInstallElevated
�  https://book.hacktricks.wiki/en/windows-hardening/windows-local-privilege-escalation/index.html#alwaysinstallelevated
    AlwaysInstallElevated set to 1 in HKLM!
    AlwaysInstallElevated set to 1 in HKCU!

```

```
����������͹ PowerShell Settings
    PowerShell v2 Version: 2.0
    PowerShell v5 Version: 5.1.19041.1
    PowerShell Core Version: 
    Transcription Settings: 
    Module Logging Settings: 
    Scriptblock Logging Settings: 
    PS history file: C:\Users\Phoebe\AppData\Roaming\Microsoft\Windows\PowerShell\PSReadLine\ConsoleHost_history.txt
    PS history size: 51B

```

```
    Directory "c:\administration" Permissions: Phoebe [AllAccess],Authenticated Users [WriteData/CreateFiles]
```

```
����������͹ Logged users
    LOVE\Administrator
    LOVE\Phoebe

```

```
    mysqld(2544)[c:\xampp\mysql\bin\mysqld.exe] -- POwn: Phoebe
    Permissions: Authenticated Users [WriteData/CreateFiles]
    Possible DLL Hijacking folder: c:\xampp\mysql\bin (Authenticated Users [WriteData/CreateFiles])

```

```
Protocol   Local Address         Local Port    Remote Address        Remote Port     State             Process ID      Process Name

  TCP        0.0.0.0               80            0.0.0.0               0               Listening         6820            c:\xampp\apache\bin\httpd.exe
  TCP        0.0.0.0               135           0.0.0.0               0               Listening         868             svchost
  TCP        0.0.0.0               443           0.0.0.0               0               Listening         6820            c:\xampp\apache\bin\httpd.exe
  TCP        0.0.0.0               445           0.0.0.0               0               Listening         4               System
  TCP        0.0.0.0               3306          0.0.0.0               0               Listening         2544            c:\xampp\mysql\bin\mysqld.exe
  TCP        0.0.0.0               5000          0.0.0.0               0               Listening         6820            c:\xampp\apache\bin\httpd.exe
  TCP        0.0.0.0               5040          0.0.0.0               0               Listening         4888            svchost
  TCP        0.0.0.0               5985          0.0.0.0               0               Listening         4               System
  TCP        0.0.0.0               5986          0.0.0.0               0               Listening         4               System
  TCP        0.0.0.0               7680          0.0.0.0               0               Listening         3872            svchost
  TCP        0.0.0.0               47001         0.0.0.0               0               Listening         4               System
  TCP        0.0.0.0               49664         0.0.0.0               0               Listening         672             lsass
  TCP        0.0.0.0               49665         0.0.0.0               0               Listening         516             wininit
  TCP        0.0.0.0               49666         0.0.0.0               0               Listening         1096            svchost
  TCP        0.0.0.0               49667         0.0.0.0               0               Listening         1452            svchost
  TCP        0.0.0.0               49668         0.0.0.0               0               Listening         2268            spoolsv
  TCP        0.0.0.0               49669         0.0.0.0               0               Listening         652             services
  TCP        0.0.0.0               49670         0.0.0.0               0               Listening         2648            svchost
  TCP        10.10.10.239          80            10.10.14.13           36342           Established       6820            c:\xampp\apache\bin\httpd.exe
  TCP        10.10.10.239          80            10.10.14.13           40594           Close Wait        6820            c:\xampp\apache\bin\httpd.exe
  TCP        10.10.10.239          80            10.10.14.13           44596           Close Wait        6820            c:\xampp\apache\bin\httpd.exe
  TCP        10.10.10.239          80            10.10.14.13           50164           Established       6820            c:\xampp\apache\bin\httpd.exe
  TCP        10.10.10.239          139           0.0.0.0               0               Listening         4               System
  TCP        10.10.10.239          62680         10.10.14.13           443             Close Wait        6964            C:\xampp\apache\bin\httpd.exe
  TCP        10.10.10.239          62682         10.10.14.13           80              Established       5852            C:\WINDOWS\system32\curl.exe
  TCP        10.10.10.239          62683         10.10.14.13           443             Established       6964            C:\xampp\apache\bin\httpd.exe
  TCP        127.0.0.1             135           127.0.0.1             62386           Established       868             svchost
  TCP        127.0.0.1             135           127.0.0.1             62392           Established       868             svchost
  TCP        127.0.0.1             62384         127.0.0.1             62385           Established       6964            C:\xampp\apache\bin\httpd.exe
  TCP        127.0.0.1             62385         127.0.0.1             62384           Established       6964            C:\xampp\apache\bin\httpd.exe
  TCP        127.0.0.1             62386         127.0.0.1             135             Established       6964            C:\xampp\apache\bin\httpd.exe
  TCP        127.0.0.1             62390         127.0.0.1             62391           Established       6964            C:\xampp\apache\bin\httpd.exe
  TCP        127.0.0.1             62391         127.0.0.1             62390           Established       6964            C:\xampp\apache\bin\httpd.exe
  TCP        127.0.0.1             62392         127.0.0.1             135             Established       6964            C:\xampp\apache\bin\httpd.exe

```

```
  Version: NetNTLMv2
  Hash:    Phoebe::LOVE:1122334455667788:400a77c2936b8c9c547877c03ba14835:01010000000000005ef76980f281db01e2c3c4f386c8758e000000000800300030000000000000000000000000200000e8c1fe67e30f03e073f8f8b5bff406b7a60714bfa6396d4c169cf552b5a64a710a00100000000000000000000000000000000000090000000000000000000000
```