***
**Guest session**
```
 nxc smb 10.10.10.239 -u "Meowmeow" -p ""                                                              
SMB         10.10.10.239    445    LOVE             [*] Windows 10 / Server 2019 Build 19041 x64 (name:LOVE) (domain:Love) (signing:False) (SMBv1:True)
SMB         10.10.10.239    445    LOVE             [-] Love\Meowmeow: STATUS_LOGON_FAILURE 
```

```
nxc smb 10.10.10.239 -u "Random" -p "" 
SMB         10.10.10.239    445    LOVE             [*] Windows 10 / Server 2019 Build 19041 x64 (name:LOVE) (domain:Love) (signing:False) (SMBv1:True)
SMB         10.10.10.239    445    LOVE             [-] Love\Random: STATUS_LOGON_FAILURE 
```

**Guest account**
```
nxc smb 10.10.10.239 -u "Guest" -p ""   
SMB         10.10.10.239    445    LOVE             [*] Windows 10 / Server 2019 Build 19041 x64 (name:LOVE) (domain:Love) (signing:False) (SMBv1:True)
SMB         10.10.10.239    445    LOVE             [-] Love\Guest: STATUS_ACCOUNT_DISABLED 
```

**Null session**
```
nxc smb 10.10.10.239 -u "" -p ""     
SMB         10.10.10.239    445    LOVE             [*] Windows 10 / Server 2019 Build 19041 x64 (name:LOVE) (domain:Love) (signing:False) (SMBv1:True)
SMB         10.10.10.239    445    LOVE             [-] Love\: STATUS_ACCESS_DENIED 
```



