

| `echo hackthebox \| base64`                        | base64 encode |
| -------------------------------------------------- | ------------- |
| `echo ENCODED_B64 \| base64 -d`                    | base64 decode |
| `echo hackthebox \| xxd -p`                        | hex encode    |
| `echo ENCODED_HEX \| xxd -p -r`                    | hex decode    |
| `echo hackthebox \| tr 'A-Za-z' 'N-ZA-Mn-za-m'`    | rot13 encode  |
| `echo ENCODED_ROT13 \| tr 'A-Za-z' 'N-ZA-Mn-za-m'` | rot13 decode  |
