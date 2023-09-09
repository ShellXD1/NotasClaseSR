# LEVEL 11 → LEVEL 12

# Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
# Datos de acceso al nivel
```
ssh bandit11@bandit.labs.overthewire.org -p 2220
bandit11
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```
# Solución
```
bandit11@bandit:~$ cat data.txt | tr 'n-za-mN-ZA-M' 'a-zA-Z'
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
```
# Notas Adicionales
cat → muestra lo que contiene un archivo
tr → sirve para desencriptar, es un comando de linux utilizado para traducir o borrar de un input y escribir el resultado en un output.
# Referencias
[Rot13 on Wikipedia](https://en.wikipedia.org/wiki/Rot13)