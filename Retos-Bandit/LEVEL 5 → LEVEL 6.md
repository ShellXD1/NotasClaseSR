# LEVEL 5 → LEVEL 6

# Objetivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable
# Datos de acceso al nivel
```
ssh bandit5@bandit.labs.overthewire.org -p 2220
bandit5
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```
# Solución
```
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere04  maybehere08  maybehere12  maybehere16
maybehere01  maybehere05  maybehere09  maybehere13  maybehere17
maybehere02  maybehere06  maybehere10  maybehere14  maybehere18
maybehere03  maybehere07  maybehere11  maybehere15  maybehere19
bandit5@bandit:~/inhere$ find -type f -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ^C
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```
# Notas Adicionales
ls → muestra los archivos dentro del directorio
cat → muestra lo que contiene un archivo
cd → comando para ingresar dentro de un directorio
find → encontrar un directorio o archivo según sus propiedades
# Referencias