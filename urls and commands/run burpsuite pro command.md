```
/usr/lib/jvm/java-21-openjdk-amd64/bin/java --add-opens=java.desktop/javax.swing=ALL-UNNAMED --add-opens=java.base/java.lang=ALL-UNNAMED --add-opens=java.base/jdk.internal.org.objectweb.asm=ALL-UNNAMED --add-opens=java.base/jdk.internal.org.objectweb.asm.tree=ALL-UNNAMED --add-opens=java.base/jdk.internal.org.objectweb.asm.Opcodes=ALL-UNNAMED -javaagent:/home/sunain/softwares/Burpsuite-Professional/Burpsuite-Professional/loader.jar -noverify -jar /home/sunain/softwares/Burpsuite-Professional/Burpsuite-Professional/burpsuite_pro_v2025.jar
```
## recommended
copy the command from the processes. 
- click on the processes at the top of kali machine 
- find the running burpsuitepro running process
- right click and copy the command.
---
## create shortcut 

copy the above command and paste it into ~/.bashrc or ~/.zshrc by creating alias like this:
```
alias burpsuitepro='/usr/lib/jvm/java-21-openjdk-amd64/bin/java --add-opens=java.desktop/javax.swing=ALL-UNNAMED --add-opens=java.base/java.lang=ALL-UNNAMED --add-opens=java.base/jdk.internal.org.objectweb.asm=ALL-UNNAMED --add-opens=java.base/jdk.internal.org.objectweb.asm.tree=ALL-UNNAMED --add-opens=java.base/jdk.internal.org.objectweb.asm.Opcodes=ALL-UNNAMED -javaagent:/home/sunain/softwares/Burpsuite-Professional/Burpsuite-Professional/loader.jar -noverify -jar /home/sunain/softwares/Burpsuite-Professional/Burpsuite-Professional/burpsuite_pro_v2025.jar'
```

---
restart terminal using this command
```
source ~/.bashrc
```
 if using zshrc than 
```
source ~/.zshrc
```

---
create an named ==burpsuitepro== without an extension. and copy this into the file:
```
sudo tee /usr/local/bin/burpsuitepro > /dev/null <<'EOF'
#!/bin/bash
exec /usr/lib/jvm/java-21-openjdk-amd64/bin/java \
  --add-opens=java.desktop/javax.swing=ALL-UNNAMED \
  --add-opens=java.base/java.lang=ALL-UNNAMED \
  --add-opens=java.base/jdk.internal.org.objectweb.asm=ALL-UNNAMED \
  --add-opens=java.base/jdk.internal.org.objectweb.asm.tree=ALL-UNNAMED \
  --add-opens=java.base/jdk.internal.org.objectweb.asm.Opcodes=ALL-UNNAMED \
  -javaagent:/home/sunain/softwares/Burpsuite-Professional/Burpsuite-Professional/loader.jar \
  -noverify -jar /home/sunain/softwares/Burpsuite-Professional/Burpsuite-Professional/burpsuite_pro_v2025.jar "$@"
EOF

sudo chmod +x /usr/local/bin/burpsuitepro
```
