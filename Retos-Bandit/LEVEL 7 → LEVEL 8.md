# LEVEL 7 → LEVEL 8
# Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**
# Datos de acceso al nivel
```
ssh bandit7@bandit.labs.overthewire.org -p 2220
bandit7
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```
# Solución
```
bandit7@bandit:~$ cat data.txt | grep millionth
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```
# Notas Adicionales
cat → muestra lo que contiene un archivo
# Referencias