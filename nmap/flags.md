
| flags         | features                                    |
| ------------- | ------------------------------------------- |
| -sV           | to identify tcp ports and their services    |
| -p-           | to identify all ports                       |
| -p ```port``` | specific port                               |
| -f            | speed up the scan                           |
| -sc           | defaut                                      |
| --min-rate    | minimum numbers of packets nmap should send |
```
nmap -sV -sc --min-rate 1000 
```
