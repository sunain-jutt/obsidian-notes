this fuzzing not just focused on the level that you have mentioned. it focus on every level.
it begins with the top level which is mainly ("/"), finds a new level and create a new branch on which a fresh fuzzing starts.

1. `Directory Discovery and Expansion`:
    - When a valid directory is found, the fuzzer doesn't just note it down. It creates a new branch for that directory, essentially appending the directory name to the base URL.
    - For example, if the fuzzer finds a directory named `admin` at the root level, it will create a new branch like `http://localhost/admin/`.
    - This new branch becomes the starting point for a fresh fuzzing process. The fuzzer will again iterate through the wordlist, appending each entry to the new branch's URL (e.g., `http://localhost/admin/FUZZ`).

## example ffuf usage 
```
sunain@htb[/htb]$ ffuf -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-medium.txt -ic -v -u http://IP:PORT/FUZZ -e .html -recursion 
```

**-ic** :  this flag intelligently removes commented lines .
