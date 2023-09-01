# LEVEL 6 → LEVEL 7
# Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size
# Datos de acceso al nivel
```
bandit6
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```
# Solución
```
bandit6@bandit:~$ find / -readable -user bandit7 -group bandit6 -size 33c
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```
# Notas Adicionales
ls → muestra los archivos dentro del directorio
cat → muestra lo que contiene un archivo
find → encontrar un directorio o archivo según sus propiedades
# Referencias