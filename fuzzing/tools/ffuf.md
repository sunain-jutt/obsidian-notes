| `Command`                                                                  | `Description`                                                                       |
| -------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `ffuf -u http://example.com/FUZZ`                                          | Basic fuzzing of a URL path.                                                        |
| `ffuf -u http://example.com/FUZZ -w wordlist.txt`                          | Fuzz with a specific wordlist.                                                      |
| `ffuf -u http://example.com/FUZZ -w wordlist.txt -ic`                      | Fuzz with a specific wordlist, automatically ignoring any comments in the wordlist. |
| `ffuf -u http://example.com/FUZZ -w wordlist.txt -c`                       | Colorize the output for better readability.                                         |
| `ffuf -u http://example.com/FUZZ -w wordlist.txt -mc 200`                  | Filter results by status code (e.g., 200).                                          |
| `ffuf -u http://example.com/FUZZ -w wordlist.txt -mr "Welcome"`            | Filter results by matching a regex pattern.                                         |
| `ffuf -u http://example.com/FUZZ -w wordlist.txt -e .php,.html`            | Add extensions to each wordlist entry.                                              |
| `ffuf -u http://example.com/FUZZ -w wordlist.txt -t 50`                    | Set the number of threads (e.g., 50) for faster fuzzing.                            |
| `ffuf -u http://example.com/FUZZ -w wordlist.txt -x http://127.0.0.1:8080` | Use a proxy for requests.                                                           |
| `ffuf -u http://example.com/FUZZ -w wordlist.txt -fc 400`                  | exclude the specific status code                                                    |
|                                                                            |                                                                                     |
