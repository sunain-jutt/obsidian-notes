
# simple fuzzling 

for simple fuzzling:

```
ffuf -u http://example.com/FUZZ -w wordlist.txt
```

# recursion

```
feroxbuster -u http://example.com -w wordlist.txt
```

# vhost fuzzling

```
gobuster vhost -u http://inlanefreight.htb:81 -w /usr/share/seclists/Discovery/Web-Content/common.txt --append-domain
```

# api fuzzling

```
python3 api_fuzzer.py http://IP:PORT
```


