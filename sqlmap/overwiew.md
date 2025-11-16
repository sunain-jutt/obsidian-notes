
sqlmap is an opensource python based tool to exploit and detect and sql injection flaws.
--risk increases the level of payloads and level increases the places to check in.

```
sqlmap -u "<example.com/file.php?id=1>"
```

for automated scanning or dumping use these flags

```
sqlmap -u <example.com/file.php> --batch --dump
```

if doing a post request enumeration then

```
sqlmap -u <example/file.php> --data='id=1'
```

if including session id or token then 

```
sqlmap -u <example.com/file.php> cookie='value' 
```

to include the session cookie enumeration add this flag

```
sqlmap -u <example.com/file.php> cookie='value' --level2
```

copy the curl into a file and us it 

```
sqlmap -r req.txt
```


