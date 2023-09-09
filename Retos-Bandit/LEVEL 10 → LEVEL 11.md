# LEVEL 10 → LEVEL 11

# Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
# Datos de acceso al nivel
```
ssh bandit10@bandit.labs.overthewire.org -p 2220
bandit10
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
# Solución
```
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```
# Notas Adicionales
cat → muestra lo que contiene un archivo
# Referencias
[Base64 on Wikipedia](https://en.wikipedia.org/wiki/Base64)