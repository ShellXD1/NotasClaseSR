# LEVEL 2 → LEVEL 3

# Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory
# Datos de acceso al nivel
```
ssh bandit2@bandit.labs.overthewire.org -p 2220
bandit2
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```
# Solución
```
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```
# Notas Adicionales
ls → muestra los archivos dentro del directorio
cat → muestra lo que contiene un archivo
# Referencias
[Google Search for “spaces in filename”](https://www.google.com/search?q=spaces+in+filename)