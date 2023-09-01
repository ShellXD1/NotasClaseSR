# LEVEL 8 → LEVEL 9
# Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
# Datos de acceso al nivel
```
bandit8
TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```
# Solución
```
bandit8@bandit:~$ cat data.txt |sort| uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```
# Notas Adicionales
cat → muestra lo que contiene un archivo

# Referencias
[Piping and Redirection](https://ryanstutorials.net/linuxtutorial/piping.php)