# LEVEL 3 → LEVEL 4

# Objetivo
The password for the next level is stored in a hidden file in the **inhere** directory.
# Datos de acceso al nivel
```
bandit3
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```
# Solución
```
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```
# Notas Adicionales
ls → muestra los archivos dentro del directorio
cat → muestra lo que contiene un archivo
cd → comando para ingresar dentro de un directorio
# Referencias