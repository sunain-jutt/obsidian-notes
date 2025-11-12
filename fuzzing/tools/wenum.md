
**parameter fuzzing**

|`Command`|`Description`|
|---|---|
|`wenum -c -w wordlist.txt --hc 404 -u http://example.com/FUZZ`|Basic fuzzing excluding 404 responses.|
|`wenum -c -w wordlist.txt -d 'username=FUZZ&password=secret' -u http://example.com/login`|Fuzz POST data in a form.|
|`wenum -c -w wordlist.txt -b 'session=12345' -u http://example.com/FUZZ`|Use a specific cookie for requests.|
|`wenum -c -w wordlist.txt -H 'User-Agent: Wenum' -u http://example.com/FUZZ`|Add a custom header to requests.|
|`wenum -c -w wordlist.txt -t 50 -u http://example.com/FUZZ`|Set the number of threads (e.g., 50) for faster fuzzing.|
|`wenum -c -w wordlist.txt -X PUT -u http://example.com/FUZZ`|Fuzz using a specific HTTP method (e.g., PUT).|
|`wenum -c -w wordlist.txt --hs 50 -u http://example.com/FUZZ`|Filter responses by content length (e.g., 50 bytes).|
