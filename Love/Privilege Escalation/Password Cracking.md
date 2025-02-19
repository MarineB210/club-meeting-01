***
**rockyou.txt**
```
hashcat -m 5600 phoebe-ntlmv2 /usr/share/seclists/Passwords/Leaked-Databases/rockyou.txt
```

```
Session..........: hashcat                                
Status...........: Exhausted
Hash.Mode........: 5600 (NetNTLMv2)
Hash.Target......: PHOEBE::LOVE:1122334455667788:400a77c2936b8c9c54787...000000
Time.Started.....: Tue Feb 18 10:35:36 2025 (17 secs)
Time.Estimated...: Tue Feb 18 10:35:53 2025 (0 secs)
Kernel.Feature...: Pure Kernel
Guess.Base.......: File (/usr/share/seclists/Passwords/Leaked-Databases/rockyou.txt)
Guess.Queue......: 1/1 (100.00%)
Speed.#1.........:   857.6 kH/s (0.85ms) @ Accel:512 Loops:1 Thr:1 Vec:4
Recovered........: 0/1 (0.00%) Digests (total), 0/1 (0.00%) Digests (new)
Progress.........: 14344384/14344384 (100.00%)
Rejected.........: 0/14344384 (0.00%)
Restore.Point....: 14344384/14344384 (100.00%)
Restore.Sub.#1...: Salt:0 Amplifier:0-1 Iteration:0-1
Candidate.Engine.: Device Generator
Candidates.#1....: $HEX[206b6d3831303838] -> $HEX[042a0337c2a156616d6f732103]
Hardware.Mon.#1..: Util: 37%
```

**rockyou.txt + OneRuleToRuleThemAll**
```
hashcat -m 5600 phoebe-ntlmv2 /usr/share/seclists/Passwords/Leaked-Databases/rockyou.txt -r ~/Downloads/OneRuleToRuleThemAll.rule
```


