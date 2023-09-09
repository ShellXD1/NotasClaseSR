# LEVEL 13 → LEVEL 14

# Objetivo
The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on
# Datos de acceso al nivel
```
ssh bandit13@bandit.labs.overthewire.org -p 2220
bandit13
wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```
# Solución
```
bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost -p 2220
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
...
...
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
```
# Notas Adicionales
_cat_ → muestra lo que contiene un archivo

_ssh_ → ofrece comunicación encriptada y segura entre dos sistemas sobre una red no segura.
# Referencias
[SSH/OpenSSH/Keys](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)