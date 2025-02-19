***
### Resume
##### Open ports
- 80/443 http(s)
- 135 RPC
- 139/445 SMB
- 3306 MySQL MariaDB
- 5000 
#### SMB
- Guest session accepted
#### Domain
- www.love.htb
- staging.love.htb
### Nmap

**Scanning top 1000 ports + version + default scripts**
```
sudo nmap -sV -sC 10.10.10.239
```

```
Nmap scan report for 10.10.10.239

PORT     STATE SERVICE      VERSION
80/tcp   open  http         Apache httpd 2.4.46 ((Win64) OpenSSL/1.1.1j PHP/7.3.27)
| http-cookie-flags: 
|   /: 
|     PHPSESSID: 
|_      httponly flag not set
|_http-title: Voting System using PHP
|_http-server-header: Apache/2.4.46 (Win64) OpenSSL/1.1.1j PHP/7.3.27
135/tcp  open  msrpc        Microsoft Windows RPC
139/tcp  open  netbios-ssn  Microsoft Windows netbios-ssn
443/tcp  open  ssl/http     Apache httpd 2.4.46 (OpenSSL/1.1.1j PHP/7.3.27)
|_http-server-header: Apache/2.4.46 (Win64) OpenSSL/1.1.1j PHP/7.3.27
|_http-title: 403 Forbidden
| ssl-cert: Subject: commonName=staging.love.htb/organizationName=ValentineCorp/stateOrProvinceName=m/countryName=in
| Not valid before: 2021-01-18T14:00:16
|_Not valid after:  2022-01-18T14:00:16
|_ssl-date: TLS randomness does not represent time
| tls-alpn: 
|_  http/1.1
445/tcp  open  microsoft-ds Windows 10 Pro 19042 microsoft-ds (workgroup: WORKGROUP)
3306/tcp open  mysql?
| fingerprint-strings: 
|   Help, JavaRMI, LANDesk-RC, NCP, NotesRPC, RTSPRequest, TerminalServer, TerminalServerCookie, afp, giop, oracle-tns: 
|_    Host '10.10.14.13' is not allowed to connect to this MariaDB server
5000/tcp open  http         Apache httpd 2.4.46 (OpenSSL/1.1.1j PHP/7.3.27)
|_http-title: 403 Forbidden
|_http-server-header: Apache/2.4.46 (Win64) OpenSSL/1.1.1j PHP/7.3.27
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port3306-TCP:V=7.94SVN%I=7%D=2/17%Time=67B39864%P=x86_64-pc-linux-gnu%r
SF:(RTSPRequest,4A,"F\0\0\x01\xffj\x04Host\x20'10\.10\.14\.13'\x20is\x20no
SF:t\x20allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(He
SF:lp,4A,"F\0\0\x01\xffj\x04Host\x20'10\.10\.14\.13'\x20is\x20not\x20allow
SF:ed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(TerminalServ
SF:erCookie,4A,"F\0\0\x01\xffj\x04Host\x20'10\.10\.14\.13'\x20is\x20not\x2
SF:0allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(LANDes
SF:k-RC,4A,"F\0\0\x01\xffj\x04Host\x20'10\.10\.14\.13'\x20is\x20not\x20all
SF:owed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(TerminalSe
SF:rver,4A,"F\0\0\x01\xffj\x04Host\x20'10\.10\.14\.13'\x20is\x20not\x20all
SF:owed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(NCP,4A,"F\
SF:0\0\x01\xffj\x04Host\x20'10\.10\.14\.13'\x20is\x20not\x20allowed\x20to\
SF:x20connect\x20to\x20this\x20MariaDB\x20server")%r(NotesRPC,4A,"F\0\0\x0
SF:1\xffj\x04Host\x20'10\.10\.14\.13'\x20is\x20not\x20allowed\x20to\x20con
SF:nect\x20to\x20this\x20MariaDB\x20server")%r(JavaRMI,4A,"F\0\0\x01\xffj\
SF:x04Host\x20'10\.10\.14\.13'\x20is\x20not\x20allowed\x20to\x20connect\x2
SF:0to\x20this\x20MariaDB\x20server")%r(oracle-tns,4A,"F\0\0\x01\xffj\x04H
SF:ost\x20'10\.10\.14\.13'\x20is\x20not\x20allowed\x20to\x20connect\x20to\
SF:x20this\x20MariaDB\x20server")%r(afp,4A,"F\0\0\x01\xffj\x04Host\x20'10\
SF:.10\.14\.13'\x20is\x20not\x20allowed\x20to\x20connect\x20to\x20this\x20
SF:MariaDB\x20server")%r(giop,4A,"F\0\0\x01\xffj\x04Host\x20'10\.10\.14\.1
SF:3'\x20is\x20not\x20allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x2
SF:0server");
Service Info: Hosts: www.example.com, LOVE, www.love.htb; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required
| smb-os-discovery: 
|   OS: Windows 10 Pro 19042 (Windows 10 Pro 6.3)
|   OS CPE: cpe:/o:microsoft:windows_10::-
|   Computer name: Love
|   NetBIOS computer name: LOVE\x00
|   Workgroup: WORKGROUP\x00
|_  System time: 2025-02-17T12:35:00-08:00
|_clock-skew: mean: 3h01m32s, deviation: 4h37m09s, median: 21m31s
| smb2-time: 
|   date: 2025-02-17T20:35:02
|_  start_date: N/A
| smb-security-mode: 
|   account_used: guest
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
```

**Scanning ALL ports**
```
sudo nmap -sV -sC -p- 10.10.10.239
```

```
PORT      STATE SERVICE      VERSION
80/tcp    open  http         Apache httpd 2.4.46 ((Win64) OpenSSL/1.1.1j PHP/7.3.27)
| http-cookie-flags: 
|   /: 
|     PHPSESSID: 
|_      httponly flag not set
|_http-title: Voting System using PHP
|_http-server-header: Apache/2.4.46 (Win64) OpenSSL/1.1.1j PHP/7.3.27
135/tcp   open  msrpc        Microsoft Windows RPC
139/tcp   open  netbios-ssn  Microsoft Windows netbios-ssn
443/tcp   open  ssl/http     Apache httpd 2.4.46 (OpenSSL/1.1.1j PHP/7.3.27)
| tls-alpn: 
|_  http/1.1
|_http-server-header: Apache/2.4.46 (Win64) OpenSSL/1.1.1j PHP/7.3.27
| ssl-cert: Subject: commonName=staging.love.htb/organizationName=ValentineCorp/stateOrProvinceName=m/countryName=in
| Not valid before: 2021-01-18T14:00:16
|_Not valid after:  2022-01-18T14:00:16
|_http-title: 403 Forbidden
|_ssl-date: TLS randomness does not represent time
445/tcp   open  microsoft-ds Windows 10 Pro 19042 microsoft-ds (workgroup: WORKGROUP)
3306/tcp  open  mysql?
| fingerprint-strings: 
|   FourOhFourRequest, GetRequest, Help, LDAPSearchReq, NULL, RPCCheck, SIPOptions, SMBProgNeg, SSLSessionReq, TerminalServerCookie, X11Probe: 
|_    Host '10.10.14.13' is not allowed to connect to this MariaDB server
5000/tcp  open  http         Apache httpd 2.4.46 (OpenSSL/1.1.1j PHP/7.3.27)
|_http-title: 403 Forbidden
|_http-server-header: Apache/2.4.46 (Win64) OpenSSL/1.1.1j PHP/7.3.27
5040/tcp  open  unknown
5985/tcp  open  http         Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
|_http-server-header: Microsoft-HTTPAPI/2.0
5986/tcp  open  ssl/http     Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
| ssl-cert: Subject: commonName=LOVE
| Subject Alternative Name: DNS:LOVE, DNS:Love
| Not valid before: 2021-04-11T14:39:19
|_Not valid after:  2024-04-10T14:39:19
|_ssl-date: 2025-02-17T20:43:35+00:00; +21m32s from scanner time.
|_http-title: Not Found
| tls-alpn: 
|_  http/1.1
7680/tcp  open  pando-pub?
47001/tcp open  http         Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
49664/tcp open  msrpc        Microsoft Windows RPC
49665/tcp open  msrpc        Microsoft Windows RPC
49666/tcp open  msrpc        Microsoft Windows RPC
49667/tcp open  msrpc        Microsoft Windows RPC
49668/tcp open  msrpc        Microsoft Windows RPC
49669/tcp open  msrpc        Microsoft Windows RPC
49670/tcp open  msrpc        Microsoft Windows RPC
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port3306-TCP:V=7.94SVN%I=7%D=2/17%Time=67B399BD%P=x86_64-pc-linux-gnu%r
SF:(NULL,4A,"F\0\0\x01\xffj\x04Host\x20'10\.10\.14\.13'\x20is\x20not\x20al
SF:lowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(GetReques
SF:t,4A,"F\0\0\x01\xffj\x04Host\x20'10\.10\.14\.13'\x20is\x20not\x20allowe
SF:d\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(RPCCheck,4A,"
SF:F\0\0\x01\xffj\x04Host\x20'10\.10\.14\.13'\x20is\x20not\x20allowed\x20t
SF:o\x20connect\x20to\x20this\x20MariaDB\x20server")%r(Help,4A,"F\0\0\x01\
SF:xffj\x04Host\x20'10\.10\.14\.13'\x20is\x20not\x20allowed\x20to\x20conne
SF:ct\x20to\x20this\x20MariaDB\x20server")%r(SSLSessionReq,4A,"F\0\0\x01\x
SF:ffj\x04Host\x20'10\.10\.14\.13'\x20is\x20not\x20allowed\x20to\x20connec
SF:t\x20to\x20this\x20MariaDB\x20server")%r(TerminalServerCookie,4A,"F\0\0
SF:\x01\xffj\x04Host\x20'10\.10\.14\.13'\x20is\x20not\x20allowed\x20to\x20
SF:connect\x20to\x20this\x20MariaDB\x20server")%r(SMBProgNeg,4A,"F\0\0\x01
SF:\xffj\x04Host\x20'10\.10\.14\.13'\x20is\x20not\x20allowed\x20to\x20conn
SF:ect\x20to\x20this\x20MariaDB\x20server")%r(X11Probe,4A,"F\0\0\x01\xffj\
SF:x04Host\x20'10\.10\.14\.13'\x20is\x20not\x20allowed\x20to\x20connect\x2
SF:0to\x20this\x20MariaDB\x20server")%r(FourOhFourRequest,4A,"F\0\0\x01\xf
SF:fj\x04Host\x20'10\.10\.14\.13'\x20is\x20not\x20allowed\x20to\x20connect
SF:\x20to\x20this\x20MariaDB\x20server")%r(LDAPSearchReq,4A,"F\0\0\x01\xff
SF:j\x04Host\x20'10\.10\.14\.13'\x20is\x20not\x20allowed\x20to\x20connect\
SF:x20to\x20this\x20MariaDB\x20server")%r(SIPOptions,4A,"F\0\0\x01\xffj\x0
SF:4Host\x20'10\.10\.14\.13'\x20is\x20not\x20allowed\x20to\x20connect\x20t
SF:o\x20this\x20MariaDB\x20server");
Service Info: Hosts: www.example.com, LOVE, www.love.htb; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| smb-security-mode: 
|   account_used: guest
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
| smb2-time: 
|   date: 2025-02-17T20:43:24
|_  start_date: N/A
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required
| smb-os-discovery: 
|   OS: Windows 10 Pro 19042 (Windows 10 Pro 6.3)
|   OS CPE: cpe:/o:microsoft:windows_10::-
|   Computer name: Love
|   NetBIOS computer name: LOVE\x00
|   Workgroup: WORKGROUP\x00
|_  System time: 2025-02-17T12:43:26-08:00
|_clock-skew: mean: 2h21m33s, deviation: 4h00m03s, median: 21m31s

```

### SSRF Enumeration 
![[ssrf-enumeration.png]]
-> Taking a long time, stopping so that we don't burden the web server too much