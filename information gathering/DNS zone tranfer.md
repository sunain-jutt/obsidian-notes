
when secondary DNS server request the primary DNS server for the entire/updated DNS records, this is called DNS zone tranfer.

## risk ??

imagine someone replict the secondary DNS server and request the primary DNS server for the entire records and it gave.

- axfr : used with dig to request the full records 

```
 dig axfr @nsztm1.digi.ninja zonetransfer.me
```

