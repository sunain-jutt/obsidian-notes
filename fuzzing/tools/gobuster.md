

| `Command`                                                           | `Description`                                    |
| ------------------------------------------------------------------- | ------------------------------------------------ |
| `gobuster dir -u http://example.com -w wordlist.txt`                | Directory fuzzing using a wordlist.              |
| `gobuster dir -u http://example.com -w wordlist.txt -x .php,.html`  | Fuzz with specific extensions.                   |
| `gobuster dir -u http://example.com -w wordlist.txt -s 200`         | Filter results by status code (e.g., 200).       |
| `gobuster dir -u http://example.com -w wordlist.txt -t 50`          | Set the number of concurrent threads (e.g., 50). |
| `gobuster dir -u http://example.com -w wordlist.txt -o results.txt` | Output results to a file.                        |
| `gobuster dns -d example.com -w subdomains.txt`                     | Fuzz DNS subdomains using a wordlist.            |
| `gobuster dns -d example.com -w subdomains.txt -i`                  | Show IP addresses of discovered subdomains.      |
| `gobuster dns -d example.com -w subdomains.txt -z`                  | Silent mode; suppress output except for results. |