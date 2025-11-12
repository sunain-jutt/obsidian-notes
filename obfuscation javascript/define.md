
Code deobfuscation is an important skill to learn if we want to be skilled in code analysis and reverse engineering. During red/blue team exercises, we often come across obfuscated code that wants to hide certain functionalities, like malware that utilizes obfuscated JavaScript code to retrieve its main payload. Without understanding what this code is doing, we may not know what exactly the code is doing, and hence may not be able to complete the red/blue team exercise.

Obfuscation is a technique used to make a script more difficult to read by humans but allows it to function the same from a technical point of view, though performance may be slower.

## tool for obfuscation

```
https://beautifytools.com/javascript-obfuscator.php
```

## tip 

if you are seeing the obfuscated code, decode it using the above tool and copy it to this tool
```
jsnice.org
```

## to minify the code

```
https://javascript-minifier.com/
```


## advance obfuscation

```
https://obfuscator.io/
```

check all these before obfuscating, it will make it more difficult to read
- [ ] string array 
- [ ] rotating string array
- [ ] shuffle string array

