
**for recursive fuzzing**

| `Command`                                                          | `Description`                                      |
| ------------------------------------------------------------------ | -------------------------------------------------- |
| `feroxbuster -u http://example.com -w wordlist.txt`                | Basic URL fuzzing with a wordlist.                 |
| `feroxbuster -u http://example.com -w wordlist.txt -e`             | Include specified file extensions in fuzzing.      |
| `feroxbuster -u http://example.com -w wordlist.txt -x 404`         | Exclude responses with status code 404.            |
| `feroxbuster -u http://example.com -w wordlist.txt -t 50`          | Set the number of concurrent threads (e.g., 50).   |
| `feroxbuster -u http://example.com -w wordlist.txt --depth 3`      | Set maximum recursion depth (e.g., 3 levels deep). |
| `feroxbuster -u http://example.com -w wordlist.txt -o results.txt` | Save output to a file.                             |
| `feroxbuster -u http://example.com -w wordlist.txt --no-recursion` | Disable recursion into discovered directories.     |
| `feroxbuster -u http://example.com -w wordlist.txt --url-redirect` |                                                    |