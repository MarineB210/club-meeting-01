***
> [!NOTE]  
> When enumerating, always good to use multiple wordlists. If stuck, try to use different tools too!
### Gobuster

**subdomains-top1million-20000.txt**
```
gobuster vhost -u love.htb -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-20000.txt --append-domain
```

```
Found: staging.love.htb Status: 200 [Size: 5357]
```

