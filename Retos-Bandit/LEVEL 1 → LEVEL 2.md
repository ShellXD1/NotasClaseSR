# LEVEL 1 → LEVEL 2

# Objetivo
The password for the next level is stored in a file called **-** located in the home directory
# Datos de acceso al nivel
```
ssh bandit1@bandit.labs.overthewire.org -p 2220
bandit1
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```
# Solución
```
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```
# Notas Adicionales
ls → muestra los archivos dentro del directorio
cat → muestra lo que contiene un archivo
# Referencias
- [Google Search for “dashed filename”](https://www.google.com/search?q=dashed+filename)
- [Advanced Bash-scripting Guide - Chapter 3 - Special Characters](http://tldp.org/LDP/abs/html/special-chars.html)