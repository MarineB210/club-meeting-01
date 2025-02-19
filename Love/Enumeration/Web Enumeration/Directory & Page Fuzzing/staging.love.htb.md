***
> [!TIP]  
> When enumerating, always good to use multiple wordlists. If stuck, try to use different tools too!

>[!CAUTION]  
> Try to use tools that limit the rate so to not overload the webserver! 
> e.g. with fuff the `--rate` parameter can control the number of request per second.
#### Fuff
**directory-list-2.3-medium.txt**
```
ffuf -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-medium.txt -u http://staging.love.htb/FUZZ --rate 1
```

```
[Status: 200, Size: 5357, Words: 1543, Lines: 192, Duration: 29ms]
```

**directory-list-2.3-medium.txt**
```
ffuf -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-medium.txt  -u http://staging.love.htb/FUZZ.php --rate 1
```

```
index [Status: 200, Size: 5357, Words: 1543, Lines: 192, Duration: 37ms]
beta [Status: 200, Size: 4997, Words: 1248, Lines: 212, Duration: 30ms]
```

**raft-large-directories-lowercase.txt**
```
ffuf -w /usr/share/seclists/Discovery/Web-Content/raft-large-directories-lowercase.txt  -u http://staging.love.htb/FUZZ.php --rate 1

```

```
beta                    [Status: 200, Size: 4997, Words: 1248, Lines: 212, Duration: 39ms]
index                   [Status: 200, Size: 5357, Words: 1543, Lines: 192, Duration: 33ms]
index                   [Status: 200, Size: 5357, Words: 1543, Lines: 192, Duration: 37ms
```