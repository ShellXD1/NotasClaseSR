# LEVEL 9 → LEVEL 10
# Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
# Datos de acceso al nivel
```
bandit9
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```
# Solución
```
bandit9@bandit:~$ cat data.txt | strings | grep ==
4========== the#
========== password
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
# Notas Adicionales
cat → muestra lo que contiene un archivo
# Referencias